Module 5 placeholder
System building blocks
So far we've mainly used platformio to write c++ code on almost everything, and while there are libraries that use python or graphical interfaces we've found just writing the code ourselves has been the most consistent in actually making progress. 
Pain Points
There are a lot of small real life problems like wire connectivity or 1 character errors that might not show an error but completly break the connection with the broker 
Scaling up
Using node-red has been extremly easy and consistent for our group so far, it really makes connecting systems with mqtt a breeze and the extensions and libraries are easy enough to use that. Haven't hit any real roadblocks with it yet, but maybe that's because we haven't used it for large enough projects.
Device management
IOTEmpower with it's OTA flashing and oneliners has been very useful the times we have got it to work, but it's definetly doable with just platformio as well.
Integration
Neither of us have much experience with IOTKnit but it seems like a decent alternative to node-red, but both of us prefer node-red over it so far.

- Important commands
  mqtt_broker - starts mqtt
  mqtt_listen  - looks for all mqtt posts on the broker
  deploy (serial) - deploys code in setup.cpp
  iot menu - opens graphical menu for the system
  adopt - flashing using a dongle
  iot doc serve - shows the documentation locally
  
