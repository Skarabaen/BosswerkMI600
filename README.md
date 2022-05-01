# BosswerkMI600
This little python script will readout quick and dirty the current values of the solar inverter Bosswerk MI600.


1. ping the MI600 IP if the coverter is available
2. use requests to get the HTML code of the web interface of the converter
3. find position of "var webdata_now_p =" / "var webdata_today_e =" / "var webdata_total_e ="
4. find following the next two " and read the values in between
5. check if the values are logical and if yes use a mqtt script to send the values to your mqtt broker
6. after that you can use the mqtt message in openhab or other automation systems 


Note:
Sometimes the converter has a timeout of some seconds or minutes. I do not know what the converter is doing in this time. Maybe there is an upload to Solarman???
