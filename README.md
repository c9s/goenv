goenv
=====

Usage
---------

    source goenv

When you run `source goenv`, goenv creates the go project directory strucutre for you. the initialized environment is like below:

    src/
    bin/
    pkg/
    vendor/

Then you can put your project package in the `src/` directory. e.g. you have a package named `app`:

    vim src/app/app.go

You can run `build`, `install` or any other commands to operate the local packages:

    go build app
    go install app


Installing Dependency
--------------------

Run `go get`, the packages will be installed into `go/vendor`, e.g.

    go get github.com/c9s/gatsby

Or define your `sync.sh` script to install package dependencies:

    #!/bin/bash
    source goenv
    get github.com/c9s/gatsby   # go get github.com/c9s/gatsby
    git_install git@github.com:c9s/gatsby.git gatsby              # install from ssh and install the package as "gatsby"
    git_install git@github.com:c9s/reqschema.git reqschema
    git_install git@github.com:c9s/textwrap.git textwrap
    git_install git@github.com:c9s/jsondata.git jsondata
    git_install git@github.com:c9s/jsonhandler.git jsonhandler

