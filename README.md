## Commands to Update
Kill the existing deployment server process(daemon): <br><br>
``` pkill -f gunicorn ```<br><br>
Go to the directory :<br><br>
``` cd flask_test/ ```<br><br>
Pull the changes from the repo: <br><br>
``` git pull origin ```<br><br>
Go back to home directory: <br><br>
``` cd .. ```<br><br>
Copy files from local repo to home page for hosting :<br><br>
``` cp -r flask_test/* . ```<br><br>
Activate the Environment: <br><br>
``` source venv/bin/activate```<br><br>
Run the database updation Script: <br><br>
``` python update_db.py ```<br><br>
Restart the deployment server <br><br>
```nohup gunicorn -w 5 -b 0.0.0.0:8000 app:app &```<br><br>
