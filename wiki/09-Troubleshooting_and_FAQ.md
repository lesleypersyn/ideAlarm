Troubleshooting and FAQ
=======================

FAQ
----
*How do I reset the alarm Zone status after an alert?*

Just toggle one of the 2 arming mode toggle switches that you have defined
for your alarm zone. That will disarm the zone and it will also reset
the zone's status to "Normal". Sirens will be switched off automatically.

I believe I've found a bug
--------------------------

Please open an issue. In order to be able to help you and to give you
the best support, please include the following information:

  - Copy the text from your configuration file. (Use a code block please)
  - Set the logging level for ideAlarm.lua to LOG_INFO: level = domoticz.LOG_INFO
  - Make the error happen and copy the relevant text from the Domoticz log to your issue report. (Use a code block please)
  - Describe (if relevant) how to reproduce the problem reported.

When there is an alert, I'd like to know what sensor what tripped
-----------------------------------------------------------------

You should modify the custom Helper Function for the event alarmZoneAlert.
There you can define all kinds of alert messages that you'd like to have.

Can the alarm be armed when door or windows are open?
-----------------------------------------------------

This question hasn't been answered yet.

When arming, how much time do you have to leave the house?
----------------------------------------------------------

You can set the exit delay for a zone in the configuration file.

Does ideAlarm trigger when a sensor is closed or turned off?
------------------------------------------------------------

No. Therefore it's also safe to arm and then open a door etc. while the exit
delay is active. Closing the door after the exit delay has passed will
not trigger the alarm. Open it again afterwards will though.

Can I configure a spoken message when a zone is tripped?
--------------------------------------------------------

Yes. That is done in the configuration file. You can define what shall happen
when an alarm zone is tripped in a custom helper function for an alarm event.

I have way too many virtual switches in Domoticz already
--------------------------------------------------------

If you never want to control the arming modes for your ideAlarm zones by using
the Domoticz's GUI, you can hide them from appearing among the Domoticz's
switches. Just put a $-sign in front of their names. For example you can rename
your device named "Toggle Z1 Arm Home" to "$Toggle Z1 Arm Home". It will still
be available in the Domoticz's GUI among the other devices though in case you
need to change it again.

If You do this, you should remember to update the ideAlarm configuration file to
reflect the new names. Otherwise ideAlarm won't work.

Troubleshooting
---------------

  - Check that you have the latest version of ideAlarm. See updating ideAlarm.
  - Do you have dzVents 2.2.0 and if so, did you apply the fix?
  - If you just upgraded from an earlier version, check again that you made the necessary steps according to the release notices
  - Check your configuration file. Are you using the correct device idx numbers and the correct device names?
