# MALICIOUS SHORTCUT


## Introduction
### In this letsDefend Scenario an alert was triggered after a user downloaded a malicious email attachment named 2025AnnualReport.7z
<br>


<h4> On March 20th at 3:22am an email with a malicious attachment was successfully delivered to Cooper's inbox </h4>

  <img width="1715" height="858" alt="Email to cooper was allowed" src="https://github.com/user-attachments/assets/46f2aecb-32a9-44fa-88cf-518155fa3ee5" />
<br> <br>

<h4>Cooper downloaded the file at 1:47pm on March 20th</h4>
  <img width="1736" height="611" alt="Cooper downloaded this file" src="https://github.com/user-attachments/assets/62ff191c-6826-4e0e-9183-da573515837a" />
<br> <br>


<h4>I checked the hash of this attachment in Virus Total... It is malicious!!</h4>
<img width="1766" height="978" alt="WE-2 Hash is malicious" src="https://github.com/user-attachments/assets/11ba8ca3-fafd-4efa-a074-bd06343eb669" />
<br> <br>


<h4> When the email attachment was downloaded and executed, it created a shortcut</h4>
<img width="1136" height="495" alt="Malicious shortcut made after Zip file was downloaded" src="https://github.com/user-attachments/assets/11d5b3bc-8645-42b5-9fd8-a343c4161b29" />
<br> <br>

<h4>When that shortcut was run Powershell reached out to an external IP</h4>
<img width="1406" height="812" alt="image" src="https://github.com/user-attachments/assets/8bcf6385-887f-4021-a64f-2de6ae60483c" />
<br> <br>

<text>
 - According to Virus Total, the 18.223.186.229 IP is malicious and used for phishing <br>
 - The PowerShell command line Uses Execution Policy Bypass which bypasses Powershell's execution-policy restrictions <br>
 - The -W flag runs the Powershell in a hidden Window
</text>


<img width="1898" height="926" alt="Suspicious Source IP" src="https://github.com/user-attachments/assets/fd00e7b9-e22f-4fa5-8dd3-2be8d13e920e" />
<br>

## Test

<br>
  <img width="904" height="495" alt="Username=adm Password=Iloveyou" src="https://github.com/user-attachments/assets/ea0f5aa0-5b30-4a19-b7d9-a12d46cdadf0" />
<br>

<br>
  <img width="1093" height="564" alt="Username=Admin Password=12345" src="https://github.com/user-attachments/assets/f66c0502-5d10-4088-a466-666ac2d56e43" />
<br>

<br>
  <img width="1242" height="548" alt="Username=Test Password=12345" src="https://github.com/user-attachments/assets/0279b7c5-50b9-4a51-b721-7f0cb47ba10d" />
<br>

<br>
<img width="1021" height="577" alt="Username=guest Password=12345" src="https://github.com/user-attachments/assets/f5af77bf-6691-4396-8dd7-0d50b927fbfb" />
<br>

<br>
<img width="1029" height="536" alt="Username=info Password=12345" src="https://github.com/user-attachments/assets/3ff21ce1-a809-44a1-a250-9439fafffe24" />
<br>

<br><hr><br>

## Text

<h3>This logon happened at 2:15pm. </h3>
<br>
<img width="1072" height="548" alt="Username=admin Password=password" src="https://github.com/user-attachments/assets/007bda10-84ef-4a43-871b-5fde4672b9ef" />
<br>

<h3>The Proxy Log shows that a successful logon occured at 2:15pm</h3>
<br>
<img width="1236" height="491" alt="User Login Successful" src="https://github.com/user-attachments/assets/29d139e3-b00d-46aa-a29b-b7935c7d3817" />
<br>


# Conclusion
## This was a successful Brute Force attempt. The extent of damage done after the bad actor gained access is hard to determine but it is clear that this Endpoint needed to be isolated from the network. 


