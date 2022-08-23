<details>
<summary><b>1: A Template on How to Write a Mail to Delete An Online Account</b></summary>
<pre>
<b>SUBJECT: Request To Delete My Account From Your Database</b>

Dear (Company Name) Team,

I have an account in your database with the name …………… and the email address that is linked to the account is ……………….
Meanwhile, for some reason, I have decided not to use the account again, therefore I request that you kindly delete my account from your database and also wipe all notifications if any.

From:
<b>Your Name.</b>
<b>Email Account.</b>
<b>Phone Number.</b>

NOTE: The name, email address and phone number that will be contained in the mail must be linked to the account you want to delete. This will be proof that you are the real owner of the account.
</pre>
</details>





<details>
<summary><b>2: Another Template on How to Write a Mail to Delete An Online Account</b></summary><br>
<pre>
<b>SUBJECT: Request To Delete My Account From Your Database</b>

To Whom It May Concern: I would like to hereby formally request the removal of all my personal and private details from your company database as soon as possible. I have recently noticed an increased amount of junk mail as well as telephone calls from companies that I have never been in touch with in the past which are very disruptive and intrusive.

However, in order to avoid this from continuing, I prefer have my details removed completely from your database as perhaps (name of company) has passed my details to a third party marketing company recently. Please confirm to me in writing that this has been done. I thank you in advance, Kind regards (Your name)

Meanwhile, if your mobile number is not linked to the account, there will be no need for you to add any phone number.

<b>Account deletion procedure</b>

The following described below are schematic approach for any account deletion.

-<b>Request</b>: A user who wishes to delete their account/data may have to submit an account deletion request.</b>
-<b>Validation</b>: Their support team member may have to cross-check your information with their internal database. If data matches, they will initiate the deletion process and notify you that the deletion has started.</b>
-<b>Deletion</b>: At this level, all the records of your account will be deleted.</b>
-<b>Final Notification</b>: Now, once the deletion process has been deleted, they will notify you that your account has been successfully deleted.</b>
</pre>
</details>





<details>
<summary><b>3: Disable Firefox Updates and Update Notifications</b></summary><br>
<b>Disable Updates using Enterprise Policy JSON (Windows/Linux/macOS)</b>

<hr><b>1. Open a plain text editor like notepad or notepad++ and paste the following code in it:</b><br>
<pre>
{
 "policies": {
    "DisableAppUpdate": true
  }
}
</pre>
<b>2. Save the file as a json file named: policies.json</b>

<hr><pre>
The following policy JSON file has to be saved in the installation directory of Firefox in a folder called <b>Distribution</b>. This folder is by default not included, and so you’ll have to create it manually. The default installation directories on the three platforms are as follows:

<b>Windows:</b>
    C:\Program Files\Mozilla Firefox\distribution or;
    C:\Program Files\Mozilla Firefox (x86)\distribution [if you’re running a 32-bit Firefox installation on a 64-bit Windows.]
    
<b>Linux:</b>
    firefox/distribution [where firefox is the installation directory for Firefox in the distribution you’re using,] or ;
    [you can specify a system-wide policy by saving the file inside] /etc/firefox/policies

<b>macOS:</b>
    Before you can install the file on your Mac, you need to remove the quarantine set by macOS which breaks an app should its installation be modified.
    To do that, open the terminal and navigate to the applications’ directory by running cd /Applications. Next, run the command: xattr -r -d com.apple.quarantine Firefox.app
    After doing that, save the policies.json file inside: /Applications/Firefox.app/Contents/Resources/distribution. You’ll have to make the directories if they’re not present.
    If you run Firefox after this and get an error message that ‘Firefox is damaged and can’t be opened. You should move it to the Trash‘, that means the quarantine wasn’t removed correctly.

</pre>
</details>



<details>
<summary><b>4: Disable Windows Defender</b></summary><br>

<b>Open notepad and make a rename file name as</b> disable.win.def.reg
<b>Copy and paste the below code into the reg file</b>
<hr> 

<pre>
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender]
"DisableAntiSpyware"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection]
"DisableBehaviorMonitoring"=dword:00000001
"DisableOnAccessProtection"=dword:00000001
"DisableScanOnRealtimeEnable"=dword:00000001
</pre>
<hr>
<b>Save the File and double click on it.</b><br>
<b>It'll give a warning, just ignore and click yes.</b><br>
<b>You're done.</b>
</details>
