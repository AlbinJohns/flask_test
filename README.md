## Commands to Update
Kill the existing deployment server process(daemon): <br>
``` pkill -f gunicorn ```<br>
Go to the directory :<br>
``` cd flask_test/ ```<br>
Pull the changes from the repo: <br>
``` git pull origin ```<br>
Go back to home directory: <br>
``` cd .. ```<br>
Copy files from local repo to home page for hosting :<br>
``` cp -r flask_test/* . ```<br>
Activate the Environment: <br>
``` source venv/bin/activate```<br>
Run the database updation Script: <br>
``` python update_db.py ```<br>
Restart the deployment server <br>
```nohup gunicorn -w 5 -b 0.0.0.0:8000 app:app &```<br>
