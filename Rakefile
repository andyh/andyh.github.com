# Taken from http://blog.sorryapp.com/blogging-with-jekyll/2014/01/31/using-jekyll-plugins-on-github-pages.html
# Rquire jekyll to compile the site.
require "jekyll"

# Github pages publishing.
namespace :blog do
  #
  # Because we are using 3rd party plugins for jekyll to manage the asset pipeline
  # and suchlike we are unable to just branch the code, we have to process the site
  # locally before pushing it to the branch to publish.
  #
  # Usaage:
  # bundle exec rake blog:publish
  desc "Publish blog to Github"
  task :publish do
    # Compile the Jekyll site using the config.
    Jekyll::Site.new(Jekyll.configuration({
      "source"      => ".",
      "destination" => "_site",
      "config" => "_config.yml"
    })).process

    # Get the origin to which we are going to push the site.
    origin = `git config --get remote.origin.url`

    # Make a temporary directory for the build before production release.
    # This will be torn down once the task is complete.
    Dir.mktmpdir do |tmp|
      # Copy accross our compiled _site directory.
      cp_r "_site/.", tmp

      # Switch in to the tmp dir.
      Dir.chdir tmp

      # Prepare all the content in the repo for deployment.
      system "git init" # Init the repo.
      system "git add . && git commit -m 'Site updated at #{Time.now.utc}'" # Add and commit all the files.

      # Add the origin remote for the parent repo to the tmp folder.
      system "git remote add origin #{origin}"

      # Push the files to the master branch, forcing an overwrite.
      system "git push origin master --force"
    end

    # Done.
  end
end

task :default => "blog:publish"
