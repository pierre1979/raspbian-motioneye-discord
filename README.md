# raspbian-motioneye-discord
For RASPBIAN and MOTIONEYE, command to use for sending notification and picture to DISCORD with a WEBHOOK

---------------------

# I.INSTALLATION
  * install discord_webhook to format discord messages
    * https://pypi.org/project/discord-webhook/
    * sudo pip install discord-webhook
    
  * copy raspbian-motioneye-discord.py to motioneye folder (should be /home/pi/motioneye/)
  * edit raspbian-motioneye-discord.py
      - paste your DISCORD webhook URL
      - edit Camera lib folder if different (folder = '/home/pi/motioneye/lib/Camera1/')
      - customize 'title' and 'description' on line "embed =..."
      
# II.USE IN MOTIONEYE
  * in command field, type :
      - python /home/pi/motioneye/raspbian-motioneye-discord.py &

# HOW IT WORKS
 As you can see the code is simple, it will send a webhook containing the last .jpg file create in the folder of the day used by Motioneye (should be /home/pi/motioneye/lib/).

# NOTES
 I only found .py for MotioneyeOS, that don't work on my Raspbian with Motioneye, that's why i made this one from scratch.

# FUTURE
* NRE (if no .jpg in folder, even if no folder)
