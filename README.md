# Battery-App
I used psutil, Psutil is a Python cross-platform library used to access system details and process utilities. It is used to keep track of various resources utilization in the system. Usage of resources like CPU, memory, disks, network, sensors can be monitored. Hence, this library is used for system monitoring, profiling, limiting process resources, and the management of running processes. 
import psutil
for process in psutil.process_iter():
    cmdline = process.cmdline

It is supported in Python versions 2.6, 2.7, and 3.4+ from plyer import notification.

python -c "f = open('/proc/4053/cmdline', 'rt'); print(repr(f.read()))" 

'/opt/python3/bin/python3 /opt/rotek-apps/bin/rpyc_server/rpyc_server.py --[app_startup]b_daemon=False\x00'
proc.cmdline() result was :

>>> proc=psutil.Process(4053)
>>> proc.cmdline()
5: 
>>> x = open('/proc/4053/cmdline', 'rt')
>>> repr(x.read())
2: ("'/opt/python3/bin/python3 /opt/rotek-apps/bin/rpyc_server/rpyc_server.py "
>>> 

Syntax: notify(title=”, message=”, app_name=”, app_icon=”, timeout=10, ticker=”, toast=False)

Parameters:
title (str) – Title of the notification
message (str) – Message of the notification
app_name (str) – Name of the app launching this notification
app_icon (str) – Icon to be displayed along with the message
timeout (int) – time to display the message for, defaults to 10
ticker (str) – text to display on status bar as the notification arrives
toast (bool) – simple Android message instead of full notification

The battery app helps in finding the correct percentage of the battery in the devices, also after every 60 mins the app will show th =e battery percentage.
