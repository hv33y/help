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

<a href="./windefender_disable.reg">windefender_disable.reg</a>

<pre>OR</pre>
Open notepad and make a rename file name as <code>disable.win.def.reg</code><br>
Copy and paste the below code into the reg file
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

Save the File and double click on it.<br>
It'll give a warning, just ignore and click yes.<br>
You're done.
</details>


<details>
<summary><b>5: Unsubscribe from All YouTube Channels</b></summary><br>
<b>STEPS</b>

- Go to [YouTube Subscribed Channel List](https://www.youtube.com/feed/channels)
- Right Click and select Inspect Element.
- Go to Console and Paste the contents of <code>youtube-unsubscriber.js</code> listed below in the console and press Enter.
- The script will execute and it will sequentially unsubscribe you from all the channels you have subscribed to.
<hr>

<x> beginning of <code>youtube-unsubscriber.js</code> </x>

<pre>
var i = 0;
var c = document.querySelectorAll("ytd-channel-renderer:not(.ytd-item-section-renderer)").length;

L1N3();

function uzmanimNet () {    
    if (c == 0) return;

    el = document.querySelector('.ytd-subscribe-button-renderer');
    el.click();

    setTimeout(function () {
        var unSubBtn = document.getElementById("confirm-button").click();
        i++;
        c--;

        console.log(i + " Unsubscribed.(L1N3)");
        console.log(c + " left.");

        setTimeout(function () {
            el = document.querySelector("ytd-channel-renderer");
            el.parentNode.removeChild(el);

            L1N3();
        }, 250);
    }, 250);
}
</pre>
</details>

 
 <details>
<summary><b>6: Delete All YouTube Liked Videos</b></summary><br>
<b>STEPS</b>
 
- [Go Here](https://www.youtube.com/playlist?list=LL) to view list of all the videos you've liked to.
- Right Click and select Inspect Element.
- Go to Console and Paste the contents of <code>youtube-like-deleter.js</code> listed below in the console and press Enter.
- The script will execute and it will sequentially delete likes you from all the videos you have liked to.
<hr>

<x> beginning of <code>youtube-like-deleter.js</code> </x>

<pre>
function sleep(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}

async function deleteLikedVideos() {
    'use strict';
    var items = document.querySelectorAll('#primary ytd-playlist-video-renderer yt-icon-button.dropdown-trigger > button[aria-label]');
    var out;

    for (var i = 0; i < items.length; i++) {
        items[i].click();
        out = setTimeout(function () {
            if (document.querySelector('tp-yt-paper-listbox.style-scope.ytd-menu-popup-renderer').lastElementChild) {
                document.querySelector('tp-yt-paper-listbox.style-scope.ytd-menu-popup-renderer').lastElementChild.click();
            }
        }, 100);
        await sleep(500); // sleep cause browser can not handle the process
        clearTimeout(out);
    }
}

deleteLikedVideos();
</pre>
</details>
 
 
 <details>
<summary><b>7: Get Back old windows photos viewer in Windows 10</b></summary><br>
<b>How to get Windows Photo Viewer back in Windows 10 (Home / Pro / Education)</b><br>
<code>Windows 10 has a bunch of new apps, including a new Photos app. I HATE the Photos app, it sucks. Slow & sluggish as hell. Here is the solution to bring back old Windows Photo Viewer.</code>
<hr>

<x> beginning of <code>enable_photo_viewer.reg</code> </x>

<pre>
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll]

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll\shell]

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll\shell\open]
"MuiVerb"="@photoviewer.dll,-3043"

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll\shell\open\command]
@=hex(2):25,00,53,00,79,00,73,00,74,00,65,00,6d,00,52,00,6f,00,6f,00,74,00,25,\
00,5c,00,53,00,79,00,73,00,74,00,65,00,6d,00,33,00,32,00,5c,00,72,00,75,00,\
6e,00,64,00,6c,00,6c,00,33,00,32,00,2e,00,65,00,78,00,65,00,20,00,22,00,25,\
00,50,00,72,00,6f,00,67,00,72,00,61,00,6d,00,46,00,69,00,6c,00,65,00,73,00,\
25,00,5c,00,57,00,69,00,6e,00,64,00,6f,00,77,00,73,00,20,00,50,00,68,00,6f,\
00,74,00,6f,00,20,00,56,00,69,00,65,00,77,00,65,00,72,00,5c,00,50,00,68,00,\
6f,00,74,00,6f,00,56,00,69,00,65,00,77,00,65,00,72,00,2e,00,64,00,6c,00,6c,\
00,22,00,2c,00,20,00,49,00,6d,00,61,00,67,00,65,00,56,00,69,00,65,00,77,00,\
5f,00,46,00,75,00,6c,00,6c,00,73,00,63,00,72,00,65,00,65,00,6e,00,20,00,25,\
00,31,00,00,00

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll\shell\open\DropTarget]
"Clsid"="{FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}"

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll\shell\print]

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll\shell\print\command]
@=hex(2):25,00,53,00,79,00,73,00,74,00,65,00,6d,00,52,00,6f,00,6f,00,74,00,25,\
00,5c,00,53,00,79,00,73,00,74,00,65,00,6d,00,33,00,32,00,5c,00,72,00,75,00,\
6e,00,64,00,6c,00,6c,00,33,00,32,00,2e,00,65,00,78,00,65,00,20,00,22,00,25,\
00,50,00,72,00,6f,00,67,00,72,00,61,00,6d,00,46,00,69,00,6c,00,65,00,73,00,\
25,00,5c,00,57,00,69,00,6e,00,64,00,6f,00,77,00,73,00,20,00,50,00,68,00,6f,\
00,74,00,6f,00,20,00,56,00,69,00,65,00,77,00,65,00,72,00,5c,00,50,00,68,00,\
6f,00,74,00,6f,00,56,00,69,00,65,00,77,00,65,00,72,00,2e,00,64,00,6c,00,6c,\
00,22,00,2c,00,20,00,49,00,6d,00,61,00,67,00,65,00,56,00,69,00,65,00,77,00,\
5f,00,46,00,75,00,6c,00,6c,00,73,00,63,00,72,00,65,00,65,00,6e,00,20,00,25,\
00,31,00,00,00

[HKEY_CLASSES_ROOT\Applications\photoviewer.dll\shell\print\DropTarget]
"Clsid"="{60fd46de-f830-4894-a628-6fa81bc0190d}"
</pre>

<b>Confirmed Working Windows 10 Versions</b><br>
<pre>
Version 1803 (OS build 17134)
Version 1709 (OS build 16299)
Version 1703 (OS build 15063)
Version 1607 (OS build 14393)
Version 1511 (OS build 10586)
Version 1507 (RTM) (OS build 10240)
Version 20H2
Version 21H2
</pre><br>
<b>Confirmed Working Windows 11 Versions</b><br>
<code>Version 21H2</code>
</details>


<details>
<summary><b>8. Rclone Config</b></summary>
<pre>
rclone mount (Config Name):/ (Drive Letter Name): --allow-other --cache-db-purge --allow-non-empty --buffer-size 256M --cache-chunk-path C:\Users\(USER)\.config\rcloneCache --cache-dir C:\Users\(USER)\.config\rclone --dir-cache-time 24h --drive-chunk-size 32M  --timeout 1h  --vfs-cache-mode minimal --vfs-read-chunk-size 128M --vfs-read-chunk-size-limit 1G --network-mode --daemon
<br>
<b>Use --daemon if vps is linux</b>
</pre>
<i>Personal Config</i>
<pre>
rclone mount Kekk:/ A: --allow-other --cache-db-purge --allow-non-empty --buffer-size 256M --cache-chunk-path C:\rclone\cache --cache-dir C:\rclone\rclone --dir-cache-time 1h --drive-chunk-size 32M  --timeout 1h --vfs-cache-mode full --vfs-read-chunk-size 128M --vfs-read-chunk-size-limit 10G --network-mode 
</pre>
</details>

