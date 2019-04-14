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

Some Screen Shots of the Android App follow.  All these screenshots rely on data obtained from the Photon.   The data on the Photon is currently just random/made-up data (with the exception of commands that actually turn something on/off and changes the equipment status).   Commands sent to the Photon are always done via a handshake.  For example, if a light/pump is turned on, the Android app only updates the status of the light on the Android app when it obtains confirmation from the Photon that the light is actually on.   Same thing for chemical injection, pump/valve commands, etc.

I haven't figured everything out yet, but I think I can get where I want to go.  Developing the user interface first really helped me decide exactly what I wanted to try and do with the project...it doesn't mean that I will actually get there though.  I'll take it a step at a time from here, and modify my goals as the project progresses.   The first step will probably be adding Photon functionality to actually sample PSI and temperature parameters that will be stored in a google spreadsheet.  This doesn't require me to gut my current pool automation control and can simply be added on "top" the existing hardware.  The second step will be to establish chlorine status/injection control...the goal is to be able to manually add chlorine at the push of a few buttons AND to regularly schedule a minimum level that will be adjusted as I gather more data.  The third step will be to move pump/valve/light control under Photon management.  Following that I would probably add acid status/control.  Although I show PH monitoring and ORP monitoring, those are later stages of the project and may or may not be actually implemented.

Currently the pool operation schedule can be viewed in the Android app but not changed.  I don't like the current format and so will make changes to that when I get time and haven't posted a screenshot.



![Alt text](/ScreenShots/Screenshot_stat.jpg?raw=true "Optional Title")
![Alt text](/ScreenShots/Screenshot_Stat_EggTimer.jpg?raw=true "Optional Title")
![Alt text](/ScreenShots/Screenshot_Chem.jpg?raw=true "Optional Title")
![Alt text](/ScreenShots/Screenshot_Chem_Tests.jpg?raw=true "Optional Title")
![Alt text](/ScreenShots/Screenshot_Chem_Recent.jpg?raw=true "Optional Title")
