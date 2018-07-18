# Zumo32U4 library
## Summary

This is a fork of the C++ library for the Arduino IDE that helps access the on-board hardware of the Zumo 32U4 robot.

The purpose of this fork is mostly to make more effective sumo robotics sketches. However, the entire library is forked just in case we ever need to bugfix or offer more functionality that we can contribute back to the original project.

## Installing the library

You can manually install the library:

1. Download the [latest release archive from GitHub](https://github.com/FeedbackRobotics/zumo-32u4-arduino-library), choose the appropriate branch, use the "clone or download" button to download it and decompress it.
2. Rename the folder "zumo-32u4-arduino-library-master" to "Zumo32U4Feedback".
3. Move the "Zumo32U4Feedback" folder into the "libraries" directory inside your Arduino sketchbook directory.  You can view your sketchbook location by opening the "File" menu and selecting "Preferences" in the Arduino IDE.  If there is not already a "libraries" folder in that location, you should make the folder yourself.
4. After installing the library, restart the Arduino IDE.

## Documentation

For complete documentation, see https://pololu.github.io/zumo-32u4-arduino-library.  If you are already on that page, then click on the links in the "Classes and functions" section above.

## Possible Improvements to Sumo AI

Just to get the creative juices flowing here are a few possible improvements to the examples provided by Pololu.

### Simple Changes
- Increase the speed that the robot moves while searching. The hope is to make this as fast as possible without accidentally driving itself off the arena.
- Observe the cases that cause the robot will drive itself off the arena and improve the logic to avoid those cases.
- Create some sort of logic to detect when you are losing and escape.
### Moderate Difficulty Changes
- Use the encoders to implement closed-loop control of speed.
- Use the IMU to implement closed-loop control of turning angle.
- Add logging to the sketch so that the robot's decisions can be debugged in a post-mortem.
### Hard Changes
- Add a bluetooth host board to the robot and write a sketch to control it with a modern video game controller.
- Add a bluetooth slave board to the robot and make a mobile app to help visualize it's current state.
- Use all avaliable sensors (wheel encoders, IMU, line sensors) to create an estimate of the robots current position in the dohyo. Because the dohyo is radially symetric this position wont be an absolute position, but rather a position relative to where the robot started.
- Make predicitons about the location of the enemy. This could be especially useful in having a "safe" searching strategy where the robot does not turn its back on any location that may contain the enemy.
