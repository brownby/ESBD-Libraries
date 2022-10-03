# Project ESBD - Libraries
Eagle device libraries for a variety of common components, split into 5 distinct categories:

**esbd-chips** - integrated circuits, including amplifiers, regulators (linear and switching), microcontrollers, and more. 

**esbd-connectors** - board-to-board and board-to-wire connectors

**esbd-passives** - resistors, capacitors, inductors, diodes, LEDs, and crystals

**esbd-transducers** - sensors and actuators, including buttons, microphones, and displays

**esbd-miscellaneous** - as of now only contains a fiducial and a schematic frame

## Using these libraries in Eagle

There are two methods for getting access to these libraries in Eagle. Both of these methods assume that you already have Eagle installed. You can find directions for getting access to a free educational Eagle license and download [here](https://knowledge.autodesk.com/support/eagle/learn-explore/caas/sfdcarticles/sfdcarticles/Eagle-Education.html).

You will also need to locate the home directory for Eagle on your system. It's typically in `~/Documents/EAGLE`, but you can change this in the Eagle Control Panel under `Options->Directories`. Wherever this folder is, it will have the structure like below:

```
EAGLE
└───archive
└───cam
└───design blocks
└───design rules
└───libraries
└───projects
└───scripts
└───spice
└───ulps
```

Naturally, we will be putting these libraries into the `EAGLE/libraries` directory.

### Method 1: Download and extract `.zip`

This method is easier, but you will have to redownload and replace the libraries manually every time we push an update if you want to stay up to date. 

1. Click "Releases" on the right hand side of the [home page for this repository](https://github.com/brownby/ESBD-Libraries). 
1. Download the `.zip` for the latest release by clicking the "Source code (zip)" link under "Assets". 
1. Extract the contents into your `EAGLE/libraries` folder. 
1. The libraries should now show up in your Eagle Control Panel inside a folder called `ESBD-Libraries-X.X.X` (where `X.X.X` represents the version number). Your directory structure should look like:
```
EAGLE
└───archive
└───cam
└───design blocks
└───design rules
└───libraries
    └───ESBD-libraries-X.X.X
        |   esbd-chips.lbr 
        |   esbd-connectors.lbr 
        |   esbd-miscellaneous.lbr 
        |   esbd-passives.lbr 
        |   esbd-transducers.lbr 
└───projects
└───scripts
└───spice
└───ulps
```
5. To make the libraries available in your Eagle projects, right click on each library and click the "Use" box. This will make the libraries appear under the "In Use" tab of the Library Manager window for your projects.

### Method 2: Clone this repository using `git`

This method requires using [`git`](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), which is a bit more complicated than downloading a `.zip`, but you'll be able to keep your libraries up to date by running a single `git pull` command. 

1. Navigate to your `EAGLE/libraries` directory from within whatever terminal you're runnig `git` in
1. Clone the repository
```
git clone git@github.com:brownby/ESBD-Libraries.git
```
3. Your directory structure should look like:
```
EAGLE
└───archive
└───cam
└───design blocks
└───design rules
└───libraries
    └───ESBD-libraries
        └───.git
        |   esbd-chips.lbr 
        |   esbd-connectors.lbr 
        |   esbd-miscellaneous.lbr 
        |   esbd-passives.lbr 
        |   esbd-transducers.lbr 
└───projects
└───scripts
└───spice
└───ulps
```
3. To make the libraries available in your Eagle projects, right click on each library and click the "Use" box. This will make the libraries appear under the "In Use" tab of the Library Manager window for your projects.
4. To update the libraries (as this repository is updated), navigate to the `EAGLE/libraries` in your terminal and run:
```
git pull
```

