# Pool Controller
Pool Controller based on a Particle IO Photon

This project will eventually be a pool controller for my swimming pool.  It is very specific to my pool, but others may find parts of it useful in doing a similar project.   I have obtained inspiration from many other pool projects that have been posted on the web, including some here on GitHub.  Special thanks to Zack Graeber, an awesome programmer (and not that bad of a son-in-law, too) who jump started me on ALL aspects of this program and who probably would have finished the entire project if he had a couple more days to spend on it, haha.  Truthfully, there are sections of code in the Android app that I have not deciphered yet.

There will be a rather slow rollout of this project because almost everything is new to me, AND I am not in a rush.

The project will consist of these parts: 
1) an android app to control pool operation that directly communicates with the Particle Photon.  This is designed with Android Studio and is written in Java.
2) a hardware implementation that includes the Photon, relays, sensors, and supporting chips/components that will interface directly to my swimming pool hardware (pump, valves, sensors)
3) a Google Sheets interface to the Photon that will allow me to log and store all desired data
4) Photon firmware that will implement: all hardware functionality, interfaces to the Android App, and interfaces to the Google spreadsheet. 
    
My goal is to have a completely self contained system that can operate my pool pump/valves for weeks without WiFi, not that it is necessary but in order to be self contained and not dependent on Wifi/internet.  All scheduling will be maintained and implemented on the Photon itself (beside chemicals testing/maintenance).  Scheduling will include the ability to schedule for all four seasons.  

In addition I want it to (with WiFi available):
1) collect and store data (temps, psi’s, Watts, gpm, chem injections, chem readings)
2) send updates, warnings, alerts about the system status
3) allow manual operations including overrides of existing schedule for pump/valves, lights, chemicals, waterfall, tbd
4) everything (within reason) accessible-controllable via phone app


Main Status/SpecialOps Android Screen
![Alt text](/ScreenShots/Screenshot_20190410-180119.jpg?raw=true "Optional Title")
