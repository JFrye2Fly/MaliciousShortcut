# MALICIOUS ATTACHMENT VIA EMAIL LEADS TO DEVICE COMPROMISE


## Introduction
### In this letsDefend Scenario an alert was triggered after a user downloaded a malicious email attachment named 2025AnnualReport.7z
<br>


<h4> On March 20th at 3:22am an email with a malicious attachment was successfully delivered to Cooper's inbox </h4>

  <img width="1715" height="858" alt="Email to cooper was allowed" src="https://github.com/user-attachments/assets/46f2aecb-32a9-44fa-88cf-518155fa3ee5" />
<br> <br>

<h4>Cooper downloaded the file at 1:47pm on March 20th</h4>
  <img width="1736" height="611" alt="Cooper downloaded this file" src="https://github.com/user-attachments/assets/62ff191c-6826-4e0e-9183-da573515837a" />
<br> <br>


<h4>I checked the hash of this attachment in Virus Total... It is malicious!! It is malware dressed up as something different. AKA a TROJAN</h4>
<img width="1766" height="978" alt="WE-2 Hash is malicious" src="https://github.com/user-attachments/assets/11ba8ca3-fafd-4efa-a074-bd06343eb669" />
<br> <br>


<h4> When the email attachment was downloaded and executed, it created a shortcut</h4>
<img width="1136" height="495" alt="Malicious shortcut made after Zip file was downloaded" src="https://github.com/user-attachments/assets/11d5b3bc-8645-42b5-9fd8-a343c4161b29" />
<br> <br>

<br>
<h4>When that shortcut was run Powershell reached out to an external IP *18.223.186.229*</h4>
<br>

<text>
 - According to Virus Total, the 18.223.186.229 IP is malicious and used for phishing <br>
 - The PowerShell command line Uses Execution Policy Bypass which bypasses Powershell's execution-policy restrictions <br>
 - The -W flag runs the Powershell in a hidden Window
 - It runs a remotely hosted Script called MBS.PS1, but it never saves it to the disk
</text>


<h4>After that MBS.PS1 script is ran we see a new local user is created on this computer</h4>
<img width="1012" height="465" alt="image" src="https://github.com/user-attachments/assets/95fd883c-0600-4f6d-b1dd-e249c5594e9b" />
<br> <br>


<h4>The new user "Helpdesk" is then added to the Administrators groups</h4>
<img width="1136" height="768" alt="New Local User added to Administrators group" src="https://github.com/user-attachments/assets/cdc1a5c4-6d37-4b90-8b16-87e9643c3405" />
<br> <br>

<h4>This "Helpdesk" user is also added to the Remote Desktop Users Group</h4>
<img width="1490" height="932" alt="New Local User added to Remote Desktop Users group" src="https://github.com/user-attachments/assets/7c283a09-961b-4fc2-9c4b-9af3c51a6cc8" />
<br> <br>


# Conclusion
## The malicious email attachment was opened by Cooper and then caused his device to communicate with the C2 server at 18.223.186.229. Upon communicating with that C2 server it ran the remotely hosted MBS.PS1 script which likely opened a reverse shell from the attacker computer to Cooper's device. We see later that a new user is created named "Helpdesk" and is added to the Administrators and Remote Desktop Users groups. 

<br> <br>

## Classic Persistence
<br>
<img width="270" height="276" alt="3ltv" src="https://github.com/user-attachments/assets/37bb9a7b-93e9-4cce-9129-94264f49d00b" />
</br>


### Final Clean up
<p>
  Aside from isolating this device from the network I also removed the **2025AnnualReport.7z** and **2025AnnualReport.lnk** files as well as the newly created "Helpdesk" local user from this computer.
</p> <br>

<p>I would also run a malware scan, check for any suspicious files in the Temp folder and check registry keys for other methods of persistence that have been added. </p>

<img width="906" height="733" alt="Deleted Zip and Shortcut of Annual Report" src="https://github.com/user-attachments/assets/290ed95c-3689-4f45-84c9-44d59d413809" /> <br>

<img width="893" height="717" alt="Deleted Help Desk user" src="https://github.com/user-attachments/assets/76cd38fd-dac1-4ce5-ae22-1d8b555a7918" />



<br><br>




