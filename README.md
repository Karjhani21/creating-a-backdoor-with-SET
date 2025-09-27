# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit

```
<img width="798" height="641" alt="image" src="https://github.com/user-attachments/assets/3dc3da27-4e96-43eb-bb8f-2837698fe660" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method
```
<img width="1688" height="723" alt="image" src="https://github.com/user-attachments/assets/2a69507d-0079-4dd9-9de3-989df23eefaf" />
  
**3. Enter your IP address as the attacker server.**
<img width="853" height="197" alt="image" src="https://github.com/user-attachments/assets/3658d5b9-078b-4bd6-862f-22fc3e403cc7" />

**4. Choose:**
```bash
2) Site Cloner
```
<img width="788" height="432" alt="image" src="https://github.com/user-attachments/assets/133b738b-9796-4e10-8c5a-1f5cd6573462" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
```
htttp://www.instagram.com
```

**6. Send the generated link to the victim.**

**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="771" height="193" alt="image" src="https://github.com/user-attachments/assets/478e5b51-34a7-490b-81cc-7fe090c19c5a" />



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
