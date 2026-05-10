
#### Step 1: Install XAMMP
- Download from: https://www.apachefriends.com
- Install to the default location: `C:\xampp` 

	![[step1.gif|493]]
#### Step 2: Copy Project Files
- Now you need to put the project file in the right folder, the file: `school_job_portal`
- place into this folder: `C:\xampp\htdocs\school_job_portal`
- After that, confirm these files exist in the `school_job_portal` folder:
	- index.php
	- config.php
	- sql (folder)
		- jobsportal.sql (file in the sql folder)
		
		 ![[step2 1.gif|515]]

#### Step 3: Start the XAMPP Server
- Open the XAMPP control panel (the app you downloaded earlier)
- Click start next to **Apache**
- Click start next to **MySQL**.

	![[step3 1.gif|549]]

#### Step 4: Set up the Database
- Open your browser and go to: `http://127.0.0.1/phpmyadmin`
- Click **Import** in the top menu
- Click **Choose file** and select: `C:\xampp\htdocs\school_job_portal\sql\jobportal.sql`
- Scroll down and click **Go**
	![[step4.gif|546]]

#### Step 5: Check Config File
- Open the file **config.php** in the project folder with notepad and confirm it looks like this:
	 ![[Pasted image 20260507174557.png]]
	![[step5.gif|544]]

*==Note: if you set a password while setting up MySQL during the XAMPP setup, enter it in the DB_PASS field, if not leave it blank==*

/

#### Step 6: Create Uploads Folder
- Make sure this folder exists: `C:\xampp\htdocs\school_job_portal\uploads\resumes\`
- if not, create it, in the `school_job_portal` create a new folder called `uploads` and then in the newly created uploads folder, create a new folder called `resumes`
	![[step6.gif|530]]

#### Step 7: Open the Portal
- Everything is set up, now open the portal:
	- http://127.0.0.1/school_job_portal/
	- http://127.0.0.1/school_job_portal/auth/login.php (Login link)
	- http://127.0.0.1/school_job_portal/auth/register.php (Register link)
- Default Admin Login details:
	- Email: admin@school.edu
	- Password: password
	![[step7.gif|561]]

#### Step 8: Test that Everything works!
- Register a student account and log in.
- Register an employer account (it'll show as pending).
- Log in as admin and approve the employer account.
- Log in as employer and post a job.
- Log in as admin again and approve the job.
- Log in as student, search for the job, and apply

After this initial setup, you won't need to repeat all these steps. To open the portal in future, simply start Apache and MySQL from the XAMPP Control Panel, then visit [http://127.0.0.1/school_job_portal/](http://127.0.0.1/school_job_portal/) in your browser

