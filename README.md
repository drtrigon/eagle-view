# eagle-viewer-repo
Fork and upload to this repo to generate views of eagle files.

# HowTo Use
1. fork this repo
    * use "Fork" button on github
    * fork it to your private repositories (no organization) - other wise you have to edit the push command at the end of the travis file
2. enable travis CI
    * https://docs.travis-ci.com/user/getting-started#To-get-started-with-Travis-CI
    * on https://travis-ci.org/profile use the "Sync" button to sync to your github account and enable eagle-viewer-repo
    * in https://travis-ci.org/[your-user-name]/eagle-viewer-repo/settings set the Environment Variables GIT_USER (your github username) and GIT_PASS (your github password - mark it as hidden!)
3. upload your eagle files (.sch and .brd) to your fork
    * use "Upload files" button on github
    * upload both files at the same time as each upload triggers a travis run/build
4. wait for travis status to finish: [![Build Status](https://travis-ci.org/drtrigon/eagle-viewer-repo.svg?branch=master)](https://travis-ci.org/drtrigon/eagle-viewer-repo)
5. view and download the results from your repos [result/pcb](tree/result/pcb) branch
    * overview of output in [README.md](tree/result/pcb/README.md) in result/pcb
6. repeat from step 3 for other files

# see also
* https://github.com/drtrigon/eagle
