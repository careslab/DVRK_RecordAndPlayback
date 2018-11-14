DVRK_RecordAndPlayback

# DESCRIPTION

This package is used to record data from the `da Vinci Research Kit`
or play them back to it.


# INSTALLATION

Install in a `catkin` workspace:

1. Clone the package into a catkin workspace:
```
$ git clone https://github.com/careslab/DVRK_RecordAndPlayback.git
```

2. Build using `catkin`:
```
$ catkin build
```

 
# USAGE

Launch an `RViz` simulation and a modified `rqt_bag` window which can
be to record or play the data back into the hardware:

```
$ roslaunch dvrk_record_and_playback record_and_playback.launch
```

The modified rqt_bag window has 2 added buttons:
1. `Rename Topics`:
The topics that are recorded are not the same as the ones that can
be played back. For this reason we need to rename the topics.
Hardware and simulation require different topics. By pressing this 
button 2 new files will be created. One for hardware and one for
simulation. The current window should be closed and reopened.
Then a file may be opened for playback.

2. `Home`:
The hardware needs to be prepared before the data can be played
back into it. The Home button prepares the hardware. Afterwards
the data can be played back.


# USING RQT_BAG

After using the `Rename Topics` and `Home` buttons everything is 
ready for playback. In order to do that simply:
1. Choose the topics that you want to playback and click publish. 
2. Press the play button in the GUI and the messages should play
back and publish into the hardware or simulation


# ABOUT

1. Author : Shahab Eslamian (Shahab.eslamian@wayne.edu)
2. Organization : Careslab, Wayne State University
3. Supervisor : Abhilash Pandya (apandya@indigo.eng.wayne.edu)
