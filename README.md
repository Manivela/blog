# Installation Guide

- Clone this repository:

  `git clone https://github.com/Manivela/blog`

- Change into your new directory:

  `cd blog`

- Using docker-compose, build the site on the preview server:

      `docker-compose up`

- Browse to [http://localhost:4000](http://localhost:4000)

- Use `docker-compose run jekyll bundle update` to update all dependencies.

## OR if you don't want to use docker:

- Download and install [rubyinstaller-2.2.6-x64](https://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.6-x64.exe)

- Make sure bundler is installed:

  `gem install bundler`

- Install these two if you are on ubuntu or the next command will fail:
  ```
  sudo apt-get install ruby-dev
  sudo apt-get install zlib1g-dev
  ```
- Install Jekyll and other dependencies from the GitHub Pages gem:

  `bundle install`

- Build the site on the preview server:

  `bundle exec jekyll serve`

- Browse to [http://localhost:4000](http://localhost:4000)

- Use `bundle update` to update all dependencies.
