# fh_optoforce_config
Optoforce configuration

# Setup sensors
In order to setup the Optoforce sensors you should update the yaml configuration located in fh_optoforce_config/config/multi_channel_3_axis_generic_scale.yaml file. 

Insert the USB disc that came with the sensor and navigate to Sensor Datasheet folder. Inside there you can find 3 pdf files 
that include the calibration sensitivity data. Check at the back of sensor board for the labels. Start from the first label from top and make a note of the serial number on it and open the corresponding pdf file. Look for the field Counts/N and use this number to update the last field of the first line in the matrix in multi_channel_3_axis_generic_scale.yaml file. Repeat this for the other two serial numbers and files and update the file accordingly.

# Update serial port number
Go to fh_optoforce_config/launch/optoforce_hand.launch file and update the port argument with the proper port number that is assigined to the device when you connect the optoforce device on your computer. To get this number navigate to /dev/optoforce/ after connecting the device and note the number. Then use this number on the second line of the launch file and replace the port. 
