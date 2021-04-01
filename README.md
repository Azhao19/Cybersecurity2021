# Honeypot Assignment

**Time spent:** **10** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?

Deployed using GCP virtual machines.

<img src="mhn-admin.gif">

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?

Dionaea attracts hackers on the Internet to itself and collects their IP and target port. If hackers deposit malware onto Dionaea, they are captured for me to  analyze.

<img src="dionaea-honeypot.gif">

### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

MHN-Admin uses mnemosyne. The file session.json records, for each attack, origin IP and port, destination port network protocol used, time of attack, the honeypot, and two identifiers.

### Deploying Additional Honeypot(s) (Optional)

#### Snort Honeypot

**Summary:** What does this honeypot simulate and do for a security researcher?

Snort allows a security researcher to detect intrusions on various resources. This could be placed at various points in software infrastructure to see what hackers tend to target.

<img src="snort-honeypot.gif">

### Malware Capture and Identification (Optional)

#### Windows Malware

**Summary:** 
I found the following Windows malware: https://malshare.com/sample.php?action=detail&hash=685bc2af410d86a742b59b96d116a7d9. It was listed on the Payloads tab on MHN-admin in my browswer. It was captured by Dionaea.

MD5 Hash: *685bc2af410d86a742b59b96d116a7d9*

SHA1 Hash: *17c237b3bd6b63effa1c309c91f7203300eb07e2*

<img src="windows-malware.gif">

## Notes

Describe any challenges encountered while doing the assignment.
