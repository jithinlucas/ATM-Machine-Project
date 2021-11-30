# ATM-Machine-Project

Operating System:
- Windows

Language:
- Python

Frameworks and Libraries
- Tkinter (The overall library for the GUI)
- JSON (Used to read the text file as a database)
- Pillow (Inserting images into the GUI) 

IDE
- Pycharm

RUNNING THE EXECTUABLE:

Resource: https://softwarekeep.com/help-center/operation-did-not-complete-successfully-because-the-file-contains-a-virus

1) Download the zip from github (https://github.com/jithinlucas/ATM-Machine-Project)
2) Extract the files somewhere to your computer from the zip
3) Navigate to that folder and locate the "dist" folder and double click it
4) Run the UI.exe file
	4.1) If there is a message about windows defender, we will need to disable the firewall temporarily.
		NOTE: IF THE UI.EXE FILE DISAPPEARED COPY PASTE THE UI.EXE FROM THE ZIP FILE BACK INTO THE DIST FOLDER OR REXTRACT ALL FILES AGAIN
	4.2) To disable windows defender, first navigate to the "Settings" menu in windows (bottom left click windows button, type settings or click settings)
	4.3) Click "Update and Security"
	4.3) On the lefthand size, navigate to "Windows Security"
	4.4) Click "Open Windows Security"
	4.5) Click "Virus & Threat Protection"
	4.6) Click "Manage Settings" under "Virus and Threat protection settings"
	4.7) Under "Real-time protection" turn it to off
5) Run the UI.exe file again

VALID TEST CASES

Receipt:
1) Login to a user
2) Logout
3) Output - Thank you screen should show

Deposit:
1) Login to a user
2) Click deposit button
3) Output - Deposit screen is shown

Depsoit Set Amount:
1) Login to a user
2) Click deposit button
3) Click either 5,10,25,50 or 100
4) Output - Balance amount should be changed to corresponding value

Deposit Custom Amount:
1) Login to a user
2) Click withdraw button
3) Enter a custom amount to withdraw
4) Output - Balance amount should be changed to corresponding value

Withdraw:
1) Login to a user
2) Click withdraw button
3) Output - Withdraw screen is shown

Withdraw Set Amount:
1) Login to a user
2) Click withdraw button
3) Click either 5,10,25,50 or 100
4) Output - Balance amount should be changed to corresponding value

Withdraw Custom Amount:
1) Login to a user
2) Click withdraw button
3) Enter a custom amount to withdraw
4) Output - Balance amount should be changed to corresponding value

Create Account:
1) Click Create Account
2) Enter user information to create an account
3) Click Create Account
4) User should be appended to the database (uses a dictionary)
5) Output - User can now login to the ATM

Help Menu:
1) Click Help
2) Help information should be shown
3) Help screen is also available in the welcome screen
4) Output - If clicked through any of these screens the help screen should appear

Back Button:
1) Click back (should be available on most screens)
2) Output - Should return to previous screen

Thank You Screen:
1) Once logging out from the users welcome screen
2) Thank you screen should be shown
3) Output - Return button should return the application to the login screen

Login:
1) Click Login
2) Input - Username: JSmith, Password: banana123
3) Output - User should be directed to the welcome screen where there account balance is shown etc.

INVALID TEST CASES

Username Taken:
1) Click Create Account
2) Input - Username: JSmith, Password: basketball123, Email: joesmith@gmail.com, Balance: 0
3) Output - Error messagebox stating 'Username taken.'

Invalid Email (No '@' in email):
1) Click Create Account
2) Input - Username: JeremySmith, Password: basketball123, Email: joesmithgmail.com, Balance: 0
3) Output - Error messagebox stating 'Invalid email.'

Invalid Email (No '.' in email):
1) Click Create Account
2) Input - Username: JeremySmith, Password: basketball123, Email: joesmith@gmailcom, Balance: 0
3) Output - Error messagebox stating 'Invalid email.'

Invalid Balance Value (Contains alphabet values):
1) Click Create Account
2) Input - Username: JeremySmith, Password: basketball123, Email: joesmith@gmail.com, Balance: abcd
3) Output - Error messagebox stating 'Invalid Deposit Value.'

Invalid Login:
1) Click Login
2) Input - Username: JSmith, Password: super123
3) Output - Error messagebox stating 'Login Invalid.'

Invalid Deposit Custom Value (Contains alphabet values):
1) Click Login
2) Input - Username: JSmith, Password: banana123
3) Click Deposit Button
4) Input - Custom Amount: abcd
5) Output - Error messagebox stating 'Invalid Deposit Value.'

Invalid Withdraw Custom Value (Contains alphabet values):
1) Click Login
2) Input - Username: JSmith, Password: banana123
3) Click Withdraw Button
4) Input - Custom Amount: abcd
5) Output - Error messagebox stating 'Invalid Withdraw Value.'

Invalid Withdraw Custom Value (Value would make account balance negative):
1) Click Login
2) Input - Username: JSmith, Password: banana123
3) Click Withdraw Button
4) Input - Custom Amount: 1000000
5) Output - Error messagebox stating 'Balance will go negative!'
