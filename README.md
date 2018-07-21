# Installation Guide
* Download and install [rubyinstaller-2.2.6-x64](https://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.6-x64.exe)
* Clone this repository:

    `git clone https://github.com/Manivela/blog`
* Change into your new directory:

    `cd blog`
* Install these two if you are on ubuntu or the next command will fail:
    ~~~~
    sudo apt-get install ruby-dev
    sudo apt-get install zlib1g-dev
    ~~~~
* Install Jekyll and other dependencies from the GitHub Pages gem:

    `install bundle `
* Build the site on the preview server:

    `bundle exec jekyll serve`
* Now browse to `http://localhost:4000`
