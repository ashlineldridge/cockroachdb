Git sub-module example
==================================================

# NAME

  cockroachdb

# SYNOPSIS

Consumer Workflow:
To get the package and sync hello-world dependency:

    kpt pkg get git@github.com:phanimarupaka/cockroachdb.git@v0.1.0 ./ && kpt pkg sync cockroachdb/
    git init && git add . && git commit -am "Initial commit" 
    
To update the package and sync hello-world dependency:
    
    kpt pkg update cockroachdb@v0.2.0 --strategy=resource-merge && kpt pkg sync cockroachdb/
    git add . && git commit -am "Changes" 

To update just the hello-world dependency package:

    update the hello-world dependency version in cockroachdb/Kptfile to v0.2.0
    kpt pkg sync cockroachdb/

For publishers:    
To add a new dependency to cockroachdb module:
    
    kpt pkg sync set git@github.com:someuser/somerepo.git@v0.1.0 cockroachdb/
    # refer 'kpt pkg sync -h' for more help

    



