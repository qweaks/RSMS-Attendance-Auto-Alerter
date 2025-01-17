# RSMS-Attendance-Auto-Alerter

![main workflow](https://img.shields.io/github/actions/workflow/status/notalanjoseph/RSMS-Attendance-Auto-Alerter/actions.yml?logo=github)
![documentation](https://img.shields.io/readthedocs/gspread?logo=readthedocs)
![python version](https://img.shields.io/pypi/pyversions/gspread?style=pypi)
 
RSET students are asked to regularly check if they are wrongly marked absent in RSMS website.  
RSMS attendance gets locked 3 days after each class, so if students fail to realise and report any discrepancies, they lose their attendance.  
This project alerts you if you have been marked absent, hence saves your precious attendance!

## How it works 🧠

The python script uses selenium to automate RSMS student's login using credentials provided.  
If an absent has been marked in the attendance table for the specified dates, an email will be sent automatically to the student's uid email to notify them of this.  
Since monday's attendance will only be locked on wednesday, the script will have to run only on every wed, thu & fri.  
Github actions has been utilised to schedule the script to run every wed, thu and fri at 6:30pm.

## How to use this 💻

- Fork this repository.  
- Edit the `chromium.py` to enter your credentials OR save your credentials as github secrets named `YOUR_UID` and `RSMS_PASSWORD`.
- Enable the workflow `Schedule Python script` from the repository's action tab. You can manually run the workflow by clicking `Run workflow` button to test if it's working.
- Thats it! The service will run automatically according to schedule as explained.