Threat model
Assets 
1. Special personal information: clinical and diagnostic referral  notes, medical history/wound and radiology images and patient urgency levels.
2. Personal identifiable information: Patient and staff full names and South African national Identity document numbers, phone numbers and home addresses.  
3. Provider Identity and credential data: Health worker login credentials, session tokens, HBCSA registration numbers and system API keys.
4. Infostructure and operational stores: Core relational databases, cloud object storage and immutable audit logs.
Actors
1. Regular users:  Clinic nurses, general practitioners and community health workers Initiating referrals
2. Specialist users: Hospital-specialists receiving, triaging and advising on cases.
3. System administrators: Internal Devops/it personnel with elevated database and infrastructure permissions
4. External malicious hackers: Cyber criminals seeking to steel identity record, deploy Ransomware or exfiltrate sensitive medical records.
5. Negligent insiders: Authorized staff who inadvertently expose credentials, misplace devices or access files outside their duty of care.
Entry points
1. User authentication portals:  
Brute force or credential stuffing to crack passwords.
Exploiting week forgot password or otp flows to hijack medical staff accounts.
Tampering with sign-up fields to elevate permissions to admin.
2. API keys:
Changing record IDs in requests (BOLA/IDOR to pull other patient’s files.     
Steeling and replaying API session tokens
Sniffing raw JSON responses that leak hidden patient data.
3. Diagnostic upload handlers:
Uploading malware or web shells disguised as images/PDFs to execute malicious code.
Exploiting file parsers to trigger remote code execution.
Flooding endpoints with huge files to crash system storage.
4. Cloud and network endpoints:
Scanning for exposed, unauthenticated database and SSH ports.
Scraping misconfigured, publicly accessible cloud storage buckets containing photos and PDFs.
Compromising third-party webhooks and service integrations to pivot inside.

5. End user devices and networks:
Intercepting network traffic over fake or unencrypted clinic Wi-Fi.
Stealing unencrypted physical phones/tablets to dump locally cached patient files.
Installing spyware or mobile malware to log clinician passwords.

 Top risks

1. Unauthorized data exfiltration and breech:
Attackers exploit broken access controls downloading bulk patient records, causing legal liability and financial   penalties.
2. Account takeover and session hijacking:
Threat actors use credential phishing or stolen session tokens to impersonate on call specialists leading to unauthorized access and tampering.
3. Ransomware and critical service disruption:
Attackers use unpatched software to gain access to back-end servers or storage repositories, they encrypt clinical databases , disrupting service and demand payment to in exchange   for returned access.
