# Introduction

Build provides you with a consistent, 'dockerized' method of building your
projects. Instead of having each one of your contributors figure out how to
build a project, you can use these scripts to create a dockerized builder that
will let anyone get started building in no time.

# Quick started

1.  Copy the 4 scripts into your project (all the files except this README.md)
2.  `cd your/project/folder`
3.  `./build-script yourname/yourproject-build`
    - the part of `yourname/yourproject-build` is the argument for the image
    that you are creating for the builder
4.  When you are dropped into the Ubuntu container, install the libraries needed
    to build your project.
5.  Verify that you can build your project in the Ubuntu container.
    - You app source code can be found at `/src`
6.  Create a bash script, with the name `start` in your project directory that
    contains all the instructions to build your project. Make sure it works from
    with in the ubuntu container.
    - You can look at the sample `start` in this project to see a super simple
    template
7.  When ready, exit using `exit`
8.  Now from this point onward, you can build your project with the command
    `./build yourname/yourproject-build`
9.  If you push the image `yourname/yourproject-build` to the docker hub, then
    people will be able to clone your repository and the simply run
    `./build yourname/yourproject-build` and it should work like magic
