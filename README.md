# roboteq

ROS driver for serial Roboteq motor controller [SDC2160](https://www.roboteq.com/index.php/docman/motor-controllers-documents-and-files/documentation/datasheets/sdc21xx-datasheet/63-sdc21xx-datasheet/file). 

The node works by downloading a MicroBasic script to the driver, which then publishes ASCII sentences at 10Hz and 50Hz with the data corresponding to the Status and per-channel Feedback messages published by the driver.
The MicroBasic and motor configuration specification can be found [here](https://www.roboteq.com/index.php/docman/motor-controllers-documents-and-files/documentation/user-manual/272-roboteq-controllers-user-manual-v17/file)

Particularly changed was the MicroBasic script, in order to adjust the voltage limits, the maximal amount of channels and the current limits to the SDC2160
