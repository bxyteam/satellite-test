# <img style="vertical-align: middle;height:40px; width:40px;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1naXRodWItaWNvbiBsdWNpZGUtZ2l0aHViIj48cGF0aCBkPSJNMTUgMjJ2LTRhNC44IDQuOCAwIDAgMC0xLTMuNWMzIDAgNi0yIDYtNS41LjA4LTEuMjUtLjI3LTIuNDgtMS0zLjUuMjgtMS4xNS4yOC0yLjM1IDAtMy41IDAgMC0xIDAtMyAxLjUtMi42NC0uNS01LjM2LS41LTggMEM2IDIgNSAyIDUgMmMtLjMgMS4xNS0uMyAyLjM1IDAgMy41QTUuNDAzIDUuNDAzIDAgMCAwIDQgOWMwIDMuNSAzIDUuNSA2IDUuNS0uMzkuNDktLjY4IDEuMDUtLjg1IDEuNjUtLjE3LjYtLjIyIDEuMjMtLjE1IDEuODV2NCIvPjxwYXRoIGQ9Ik05IDE4Yy00LjUxIDItNS0yLTctMiIvPjwvc3ZnPg=="> Github Satellites
---

## <img style="vertical-align: middle;height:35px; width:35px;"  src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1zZXR0aW5ncy1pY29uIGx1Y2lkZS1zZXR0aW5ncyI+PHBhdGggZD0iTTEyLjIyIDJoLS40NGEyIDIgMCAwIDAtMiAydi4xOGEyIDIgMCAwIDEtMSAxLjczbC0uNDMuMjVhMiAyIDAgMCAxLTIgMGwtLjE1LS4wOGEyIDIgMCAwIDAtMi43My43M2wtLjIyLjM4YTIgMiAwIDAgMCAuNzMgMi43M2wuMTUuMWEyIDIgMCAwIDEgMSAxLjcydi41MWEyIDIgMCAwIDEtMSAxLjc0bC0uMTUuMDlhMiAyIDAgMCAwLS43MyAyLjczbC4yMi4zOGEyIDIgMCAwIDAgMi43My43M2wuMTUtLjA4YTIgMiAwIDAgMSAyIDBsLjQzLjI1YTIgMiAwIDAgMSAxIDEuNzNWMjBhMiAyIDAgMCAwIDIgMmguNDRhMiAyIDAgMCAwIDItMnYtLjE4YTIgMiAwIDAgMSAxLTEuNzNsLjQzLS4yNWEyIDIgMCAwIDEgMiAwbC4xNS4wOGEyIDIgMCAwIDAgMi43My0uNzNsLjIyLS4zOWEyIDIgMCAwIDAtLjczLTIuNzNsLS4xNS0uMDhhMiAyIDAgMCAxLTEtMS43NHYtLjVhMiAyIDAgMCAxIDEtMS43NGwuMTUtLjA5YTIgMiAwIDAgMCAuNzMtMi43M2wtLjIyLS4zOGEyIDIgMCAwIDAtMi43My0uNzNsLS4xNS4wOGEyIDIgMCAwIDEtMiAwbC0uNDMtLjI1YTIgMiAwIDAgMS0xLTEuNzNWNGEyIDIgMCAwIDAtMi0yeiIvPjxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjMiLz48L3N2Zz4="> Configuration

* ###### Add user name in the .env file, key GITHUB_OWNER 
* ###### Create a new repository
* ###### Add repository name in the .env file, key GITHUB_REPO 
* ###### Go to https://github.com/settings/personal-access-tokens
   - ###### Click generate new token
     * ###### Token settings
       - ###### Choose Only select repositories and pick your repo
       - ###### In Repository permissions select:
         * ###### Commit statuses (Read and Write)
         * ###### Merge queues (Read and Write) 
         * ###### Pull requests (Read and Write)
         * ###### Metadata (Mandatory selected by github)
     * ###### Save changes     
   - ###### Copy token in the .env file, key GITHUB_TOKEN 

## <img style="vertical-align: middle;height:35px; width:35px;"  src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1naXQtYnJhbmNoLWljb24gbHVjaWRlLWdpdC1icmFuY2giPjxsaW5lIHgxPSI2IiB4Mj0iNiIgeTE9IjMiIHkyPSIxNSIvPjxjaXJjbGUgY3g9IjE4IiBjeT0iNiIgcj0iMyIvPjxjaXJjbGUgY3g9IjYiIGN5PSIxOCIgcj0iMyIvPjxwYXRoIGQ9Ik0xOCA5YTkgOSAwIDAgMS05IDkiLz48L3N2Zz4="> Satellites Repository
<hr style="height:.2px">

#### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1mb2xkZXItdHJlZS1pY29uIGx1Y2lkZS1mb2xkZXItdHJlZSI+PHBhdGggZD0iTTIwIDEwYTEgMSAwIDAgMCAxLTFWNmExIDEgMCAwIDAtMS0xaC0yLjVhMSAxIDAgMCAxLS44LS40bC0uOS0xLjJBMSAxIDAgMCAwIDE1IDNoLTJhMSAxIDAgMCAwLTEgMXY1YTEgMSAwIDAgMCAxIDFaIi8+PHBhdGggZD0iTTIwIDIxYTEgMSAwIDAgMCAxLTF2LTNhMSAxIDAgMCAwLTEtMWgtMi45YTEgMSAwIDAgMS0uODgtLjU1bC0uNDItLjg1YTEgMSAwIDAgMC0uOTItLjZIMTNhMSAxIDAgMCAwLTEgMXY1YTEgMSAwIDAgMCAxIDFaIi8+PHBhdGggZD0iTTMgNWEyIDIgMCAwIDAgMiAyaDMiLz48cGF0aCBkPSJNMyAzdjEzYTIgMiAwIDAgMCAyIDJoMyIvPjwvc3ZnPg==" /> Project structure


```bash
.
├── frontend
│   ├── audio
│   ├── dist
│   ├── images
│   ├── sats
│   ├── html
│   └── templates
├── it
│   ├── AboutTime
│   │   └── AboutTime
│   └── illum
├── keps
├── keps_updater
│   └── src
│       └── amsat
└── scripts
```
***Warning! Deleting or renaming files and folders may cause undesired effects on the application or cause it to stop working***

### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1mb2xkZXItb3Blbi1pY29uIGx1Y2lkZS1mb2xkZXItb3BlbiI+PHBhdGggZD0ibTYgMTQgMS41LTIuOUEyIDIgMCAwIDEgOS4yNCAxMEgyMGEyIDIgMCAwIDEgMS45NCAyLjVsLTEuNTQgNmEyIDIgMCAwIDEtMS45NSAxLjVINGEyIDIgMCAwIDEtMi0yVjVhMiAyIDAgMCAxIDItMmgzLjlhMiAyIDAgMCAxIDEuNjkuOWwuODEgMS4yYTIgMiAwIDAgMCAxLjY3LjlIMThhMiAyIDAgMCAxIDIgMnYyIi8+PC9zdmc+"> frontend directory
This directory contains files using in the web.

##### audio
Directory with audio files.

##### dist
Directory with stylesheet, javascripts files used in pass.html template.

```bash
dist/
├── all.js
├── all.json
├── keps.txt 
├── assetsSrcGithub.js
├── assetsSrc.js
├── freq.js
├── orb.css
├── orbz.min.js
└── predictlib1.js
```
#### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1maWxlLWNvZGUtaWNvbiBsdWNpZGUtZmlsZS1jb2RlIj48cGF0aCBkPSJNMTAgMTIuNSA4IDE1bDIgMi41Ii8+PHBhdGggZD0ibTE0IDEyLjUgMiAyLjUtMiAyLjUiLz48cGF0aCBkPSJNMTQgMnY0YTIgMiAwIDAgMCAyIDJoNCIvPjxwYXRoIGQ9Ik0xNSAySDZhMiAyIDAgMCAwLTIgMnYxNmEyIDIgMCAwIDAgMiAyaDEyYTIgMiAwIDAgMCAyLTJWN3oiLz48L3N2Zz4=">  Dist File Description

- all.js
  - Javascript file with tle matrix (file generated by keps updater).
- all.json
  - JSON file with tle matrix (file generated by keps updater). Fetch from server for pass.html.
- keps.txt
  - Txt file with new keps (file generated by keps updater).
- assetsSrcGithub.js
  - Javascript file with a dictionary key, value pairs with image urls hosted in the github repo, used as backup of assetsSrc.js. 
- assetsSrc.js
  - Javascript file with a dictionary key, value pairs with image urls hosted in external server. Load by pass.html with cdn. 
- freq.js
  - Javascript file used by pass.html and load from cdn. Be careful when editing it.
- orb.css
  - Stylesheet file with css properties, used by pass.html and load from cdn.  
- orbz.min.js
  - JavaScript file that handles the entire application, and probably the one you should edit, used by pass.html and load from cdn.
- predictlib1.js
  - Javascript file used by pass.html and load from cdn. Be careful when editing it.

##### images
Directory with satellite images.

##### sats
Directory with html files. Satellites details pages.

##### html
Directory to put new html files

##### templates
Directory with builder html template files

```bash
templates/
└── pass.html
```
#### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1maWxlLWNvZGUtaWNvbiBsdWNpZGUtZmlsZS1jb2RlIj48cGF0aCBkPSJNMTAgMTIuNSA4IDE1bDIgMi41Ii8+PHBhdGggZD0ibTE0IDEyLjUgMiAyLjUtMiAyLjUiLz48cGF0aCBkPSJNMTQgMnY0YTIgMiAwIDAgMCAyIDJoNCIvPjxwYXRoIGQ9Ik0xNSAySDZhMiAyIDAgMCAwLTIgMnYxNmEyIDIgMCAwIDAgMiAyaDEyYTIgMiAwIDAgMCAyLTJWN3oiLz48L3N2Zz4=">  Templates File Description

- pass.html
  - This file render the satellites main page in the web builder.

### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1mb2xkZXItb3Blbi1pY29uIGx1Y2lkZS1mb2xkZXItb3BlbiI+PHBhdGggZD0ibTYgMTQgMS41LTIuOUEyIDIgMCAwIDEgOS4yNCAxMEgyMGEyIDIgMCAwIDEgMS45NCAyLjVsLTEuNTQgNmEyIDIgMCAwIDEtMS45NSAxLjVINGEyIDIgMCAwIDEtMi0yVjVhMiAyIDAgMCAxIDItMmgzLjlhMiAyIDAgMCAxIDEuNjkuOWwuODEgMS4yYTIgMiAwIDAgMCAxLjY3LjlIMThhMiAyIDAgMCAxIDIgMnYyIi8+PC9zdmc+"> it directory

##### it
Directory that contains among others the files to generate new steps using dosbox. The new steps are copied into HTML files. Also contains ilium and About Time directories used by batch files.

```bash
it/
├── .....
├── subepaso.bat
├── subePasoPart1.bat
├── subePasoPart2.bat
├── subePasoPart3.bat
├── subePasoPart4.bat
├── subePasoPart5.bat
├── subePasoPart6.bat
├── subePasoPart7.bat
├── subePasoPart8.bat
├── subePasoPart9.bat
├── subePasoPart10.bat
└── .....

```

### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1mb2xkZXItb3Blbi1pY29uIGx1Y2lkZS1mb2xkZXItb3BlbiI+PHBhdGggZD0ibTYgMTQgMS41LTIuOUEyIDIgMCAwIDEgOS4yNCAxMEgyMGEyIDIgMCAwIDEgMS45NCAyLjVsLTEuNTQgNmEyIDIgMCAwIDEtMS45NSAxLjVINGEyIDIgMCAwIDEtMi0yVjVhMiAyIDAgMCAxIDItMmgzLjlhMiAyIDAgMCAxIDEuNjkuOWwuODEgMS4yYTIgMiAwIDAgMCAxLjY3LjlIMThhMiAyIDAgMCAxIDIgMnYyIi8+PC9zdmc+">  keps directory

#### keps
Directory with txt files used by keps updater application.

```bash
keps
├── addsat.txt
├── localkeps.txt
├── moonkeps.txt
├── omitlist.txt
├── spacetrack1.txt
├── spacetrack2.txt
└── spacetrack.txt

```
### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1mb2xkZXItb3Blbi1pY29uIGx1Y2lkZS1mb2xkZXItb3BlbiI+PHBhdGggZD0ibTYgMTQgMS41LTIuOUEyIDIgMCAwIDEgOS4yNCAxMEgyMGEyIDIgMCAwIDEgMS45NCAyLjVsLTEuNTQgNmEyIDIgMCAwIDEtMS45NSAxLjVINGEyIDIgMCAwIDEtMi0yVjVhMiAyIDAgMCAxIDItMmgzLjlhMiAyIDAgMCAxIDEuNjkuOWwuODEgMS4yYTIgMiAwIDAgMCAxLjY3LjlIMThhMiAyIDAgMCAxIDIgMnYyIi8+PC9zdmc+">  keps_updater directory

#### keps_updater
Directory with java files to update keps and tle matrix. To use this application you need sapcetrack credentials.

```bash
keps_updater/
└── src
    └── amsat
        ├── AddSatProcessor.java
        ├── DateFormatter.java
        ├── KepsUpdateRunner.java
        ├── LocalKepsProcessor.java
        ├── MoonKepsProcessor.java
        ├── OmitListProcessor.java
        ├── SatelliteFileWriter.java
        ├── SatelliteTLEProcessor.java
        ├── SatelliteUpdateProcessor.java
        ├── SpacetrackProcessor.java
        ├── SpaceTrackReader.java
        └── TleCleaner.java
```
### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1mb2xkZXItb3Blbi1pY29uIGx1Y2lkZS1mb2xkZXItb3BlbiI+PHBhdGggZD0ibTYgMTQgMS41LTIuOUEyIDIgMCAwIDEgOS4yNCAxMEgyMGEyIDIgMCAwIDEgMS45NCAyLjVsLTEuNTQgNmEyIDIgMCAwIDEtMS45NSAxLjVINGEyIDIgMCAwIDEtMi0yVjVhMiAyIDAgMCAxIDItMmgzLjlhMiAyIDAgMCAxIDEuNjkuOWwuODEgMS4yYTIgMiAwIDAgMCAxLjY3LjlIMThhMiAyIDAgMCAxIDIgMnYyIi8+PC9zdmc+">  scripts directory

#### scripts
Directory containing bash files executed by the application in a cron job.

```bash
scripts/
├── copy_files.sh
├── run_dosbox.sh
├── run_keps_updater.sh
└── run_pasos_updater.sh
```

#### <img style="vertical-align: middle;" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiMyNGEwZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1maWxlLXRlcm1pbmFsLWljb24gbHVjaWRlLWZpbGUtdGVybWluYWwiPjxwYXRoIGQ9Ik0xNSAySDZhMiAyIDAgMCAwLTIgMnYxNmEyIDIgMCAwIDAgMiAyaDEyYTIgMiAwIDAgMCAyLTJWN1oiLz48cGF0aCBkPSJNMTQgMnY0YTIgMiAwIDAgMCAyIDJoNCIvPjxwYXRoIGQ9Im04IDE2IDItMi0yLTIiLz48cGF0aCBkPSJNMTIgMThoNCIvPjwvc3ZnPg==">  Script Files Description

- copy_files.sh
  - This script copy html / sats / templates files to web directory.
- run_dosbox.sh
  - This script execute the current subpaso*.bat batch file in a dosbox application.
- run_keps_updater.sh 
  - This script copy the last steps generated and copy to web share directory and run keps updater java application to update keps and tle matrix the application build the nasa json file with tle matrix and copy to share folder.
- run_pasos_updater.sh
  - this script execute a loop with a list of steps and call the run_dosbox.sh bash script for each step.         

#### dosbox

The dosbox.conf file is created in memory for each batch file.

###### dosbox.conf
```bash
SCRIPT_NAME="$1"
BAT_FILE="${SCRIPT_NAME}.bat"
CONFIG_FILE="/var/satellite/data/github/it/dosbox.conf"
IT_DIR="/var/satellite/data/github/it"
cat <<EOF > "$CONFIG_FILE"
[sdl]
fullscreen=false
autolock=false
output=surface

[mixer]
nosound=true

[speaker]
pcspeaker=false
tandy=off
disney=false

[sblaster]
sbtype=none

[gus]
gus=false

[dosbox]
captures=${IT_DIR}/captures

[render]
frameskip=1

[cpu]
core=auto
cputype=auto
cycles=150000
cycleup=10
cycledown=20

[autoexec]
mount c ${IT_DIR}
c:
call ${BAT_FILE}
exit
EOF
```

