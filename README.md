# Personal-Date-Reminder 📅

Remind yourself via pop-up message box of personal events specified in your own Excel spreadsheet.

<img src="/Data/Personal-Date-Reminder.gif" alt="GIF of Personal-Date-Reminder running." width="100%" />

## Running the Automation

1. Download the template "/Data/dates.xlsx" to be used as a starting point by this automation and store it on the machine where you will be running the automation.

2. Update the per-Robot value for the Asset used by this automation to point to the full path where you stored your personal "dates.xlsx" file:

    * **Asset Name** = Personal-Date-Reminder_Workbook-Path
    
    * **Asset Description** = Full path to your personal "dates.xlsx" file. 
    
    * **Asset Per-Robot Value (Example)** = "C:\Users\Michael\Desktop\dates.xlsx"

3. Update your personal "dates.xlsx" file to events that you would like to be notified about. The original template you downloaded comes with a sample event:

    * **Name** = Michael

    * **Event** = Work Anniversary

    * **Date** = 8/26/2019

    * **Years** = 1

    * **Is Today?** = FALSE

    * Note that the automation relies on the original column names and logic from the template you downloaded. You can delete the sample events and add your own events, in which the logic has been pre-filled for 100 rows. You can expand or condense to as many or little rows as you would like to.

    * Note that Excel inherently does not work well with dates prior to the year 1900, but workarounds exist online if you would like to do some research and make changes to the logic.

4. If the automation runs on a day where the “Is Today?” value is “FALSE” for all rows, the pop-up message box will state the following:

    * "There are no events today."

5. If the automation runs on a day where the “Is Today?” value is “TRUE” for at least one row, the pop-up message box will state the following, this example being the sample event getting ran on 8/26/2020:

    * "Michael is celebrating their Work Anniversary of 1 year(s)."

    * Note that if there are multiple “TRUE” events, each sentence will follow the same format and be appended to the text displayed in the pop-up message box to form multiple sentences.

6. Run the automation!

    * It is best ran attended from the UiPath Assistant while using the Reminders feature to be notified about running it so you can’t forget.
  
    * Note that if you run the automation unattended, the job does not complete until the pop-up message box is acknowledged and closed.
  
    * This is a very simple automation, as its actually the first one I built after joining UiPath! Use it to be reminded about personal events you may forget about on that day. It is also useful as a simple demo to get somebody new to automation excited about its potential.

    * Notice that the majority of the logic is taken care of by Excel, because why automate what can be done more simply by other software? There is ton of room for improvements, like sending a text message or email rather than a pop-up message box so that this can truly be an unattended automation seven days a week. Feel free to play around with it and make it your own!

## Owner

[Michael A.](https://linkedin.com/in/magarenzo)
