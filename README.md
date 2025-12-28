# ThingsBoard Weekly Wcheduler
The Weekly Scheduler Widget for ThingsBoard

# Widget features
* Created and tested on ThingsBoard v4.1.0
* Supports **Shared Attributes**
* Data format is a string/text

# Data key format
**[E,SMTWTFS,HH,MM,P,S]**
* **E**: Enable/Disable this scheduler: 1 (Enabled) / 0 (Disabled)
* **SMTWTFS**: Days of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat). Use 1 to select and 0 to deselect
* **HH**: Hour (0-23), 24-hour format
* **MM**: Minute (0-59)
* **P**: Duration in minutes (should not exceed the total minutes in a week)
* **S**: State: 1 (ON) / 0 (OFF)

Example
* [1,0111110,10,00,30,1] - This scheduler is enabled; the entity state is set to ON for 30 minutes at 10:00 on weekdays
* [1,0000010,17,30,10,0] - This scheduler is enabled; the entity state is set to OFF for 10 minutes at 17:30 on Fridays (to power off the device before the weekend)

# Usage
* Import weekly_scheduler.json to the ThingsBoard Widgets library
* Add the widget to a dashboard
* Select the Entity and the Shared Attribute to use as the data key

