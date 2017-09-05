Go precode
Currently the classifierConcurrent() function is identical to classifierSingle(). Your goal is to parallelize it.

First:
Set up Go, and set up your GOPATH properly (instructions: https://golang.org/doc/code.html)
install the gonum (a math package with matrix functionalities) package by following instructions at:
https://github.com/gonum/gonum

september 5. 2017, the matrix package of gonum was changed in a way that broke the precode. A fix is as follows:
1. Navigate to "$GOPATH/src/gonum.org/v1/gonum", we need to rollback the repository to a state that works with the precode
#hard reset the state of the repository to ensure no conflicts when fast forwarding
2. git reset --HARD
#fetch the newest version of the repository
3. git pull --ff
#checkout the last working commit
4. git checkout d7342e6

Then:
Unzip the datasets into this folder, or modify the path in main.
To run the program, type:
go run main.go classifier.go classifier_concurrent.go
