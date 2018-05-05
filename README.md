# eagle-view
[![Build Status](https://travis-ci.org/drtrigon/eagle-view.svg?branch=test)](https://travis-ci.org/drtrigon/eagle-view/branches)

Fork and upload to this repo and use travis to generate views of eagle files.

Uses eagle 7.7.0 but that can be changed in the config file. KiCAD export can be enabled in the config file as well but will make the run taking about 20 mins longer.

# HowTo Use
1. fork this repo
    * use "Fork" button on github
    * fork it to your private repositories (no organization) - other wise you have to edit the push command at the end of the travis file
2. enable travis CI
    * https://docs.travis-ci.com/user/getting-started#To-get-started-with-Travis-CI
    * on https://travis-ci.org/profile use the "Sync" button to sync to your github account and enable eagle-view repo
    * in https://travis-ci.org/[your-user-name]/eagle-view/settings set the Environment Variables GIT_USER (your github username) and GIT_PASS (your github password - mark it as hidden!) - see [example](https://travis-ci.org/drtrigon/eagle-view/settings)
3. upload your eagle files (.sch and .brd) to your fork
    * use "Upload files" button on github
    * upload both files at the same time as each upload triggers a travis run/build
4. wait for travis status to finish: https://travis-ci.org/[your-user-name]/eagle-view
5. view and download the results (as zip file) from your repos [result/pcb](/../../tree/result/pcb) branch
6. repeat from step 3 for other files

# Alternative Use
Execute the commands given in the [travis config](.travis.yml) file on your local linux (ubuntu, debian) machine.

# Example Results
As an example we use the Arduino Uno files from https://store.arduino.cc/usa/arduino-uno-rev3 see under Documentation and produce this output ([test](/../../tree/test) branch):

## GERBER files
[![GERBER files](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH.zip)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH.zip)

[![GERBER log](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH.gpi)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH.gpi)

[![drill log](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH.dri)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH.dri)

[![GERBER render](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH.png)

[![GERBER render bottom](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_btm.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_btm.png)

[![GERBER render top](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_top.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_top.png)

[![GERBER render all](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_all.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_all.png)

## partlist
[![partlist](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH.txt)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH.txt)

## board and schematic
[![board](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_brd.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_brd.png)

[![schematic](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_sch.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_sch.png)

## erc and drc
[![erc](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_erc.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_erc.png)

[![drc](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_drc.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_drc.png)

## autorouter
[![autorouter](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_auto.png)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_auto.png)

## KiCAD project import
[![KiCAD project](https://raw.githubusercontent.com/drtrigon/eagle-view/example/arduino_Uno_Rev3-02-TH_kicad.zip)](https://github.com/drtrigon/eagle-view/blob/example/arduino_Uno_Rev3-02-TH_kicad.zip)

# See also
* https://github.com/drtrigon/eagle (this is the project where the travis config / bash script originates from)
