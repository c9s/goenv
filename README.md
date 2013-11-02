goenv
=====

Usage
---------

    source goenv
    go build app
    go install app

Run `go get`, the packages will be installed into `go/vendor`

Or define your `get.sh` for package dependencies:

    #!/bin/bash
    source goenv
    get github.com/c9s/gatsby   # install github.com/c9s/gatsby
    git_install git@github.com:c9s/gatsby.git gatsby              # install from ssh and install the package as "gatsby"
    git_install git@github.com:c9s/reqschema.git reqschema
    git_install git@github.com:c9s/textwrap.git textwrap
    git_install git@github.com:c9s/jsondata.git jsondata
    git_install git@github.com:c9s/jsonhandler.git jsonhandler

