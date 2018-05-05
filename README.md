# eagle-view
[![Build Status](https://travis-ci.org/drtrigon/eagle-view.svg?branch=test)](https://travis-ci.org/drtrigon/eagle-view)

Fork and upload to this repo and use travis to generate views of eagle files.

Uses eagle 7.7.0 but that can be changed in the config file. KiCAD export can be enabled in config file as well but will make the run taking about 20 mins longer.

# HowTo Use
1. fork this repo
    * use "Fork" button on github
    * fork it to your private repositories (no organization) - other wise you have to edit the push command at the end of the travis file
2. enable travis CI
    * https://docs.travis-ci.com/user/getting-started#To-get-started-with-Travis-CI
    * on https://travis-ci.org/profile use the "Sync" button to sync to your github account and enable eagle-view repo
    * in https://travis-ci.org/[your-user-name]/eagle-view/settings set the Environment Variables GIT_USER (your github username) and GIT_PASS (your github password - mark it as hidden!)
3. upload your eagle files (.sch and .brd) to your fork
    * use "Upload files" button on github
    * upload both files at the same time as each upload triggers a travis run/build
4. wait for travis status to finish: https://travis-ci.org/[your-user-name]/eagle-view
5. view and download the results from your repos [result/pcb](/../../tree/result/pcb) branch
    * overview of output in [README.md](/../../tree/result/pcb/README.md) in result/pcb
6. repeat from step 3 for other files

# Alternative Use
Execute the commands given in the [travis config](.travis.yml) file on your local linux (ubuntu, debian) machine.

# See also
* https://github.com/drtrigon/eagle (this is the project where the travis conifg / bash script originates from)
