# Experiment No. 4: Analyze Email Headers and Detect Email Spoofing Using MHA

## Aim

To analyze an email header using Mail Header Analyzer (MHA) and detect possible email spoofing by examining email routing information and authentication results.

## Requirements

* Gmail / Outlook / Yahoo Mail
* Mail Header Analyzer (MHA)
* Web browser
* WHOIS / IP lookup tool
* Internet connection

## Procedure

### Step 1: Access the Email Header

**Gmail:**

1. Open the email.
2. Click the three-dot menu in the upper-right corner.
3. Select **Show original**.

**Outlook:**

1. Open the email.
2. Click **File**.
3. Select **Properties**.
4. Locate the **Internet headers** section.

**Yahoo:**

1. Open the email.
2. Click the three-dot menu.
3. Select **View raw message**.

### Step 2: Copy the Email Header

Copy the complete email header displayed by the email service.

### Step 3: Analyze the Header Using MHA

1. Open Mail Header Analyzer.
2. Paste the copied email header into the analyzer.
3. Submit the header for analysis.
4. Examine the parsed header information.
5. Identify the `From`, `To`, `Return-Path`, `Received`, and `Message-ID` fields.
6. Check the SPF, DKIM, and DMARC authentication results.

### Step 4: Analyze the Received Fields

Examine the `Received` fields to determine:

* Sending server hostname
* Sending server IP address
* Receiving server
* Date and time of transmission
* Sequence of mail servers

The `Received` headers should be analyzed from the **bottom upward** to trace the email's path.

### Step 5: Check IP Addresses and Hostnames

Use an IP lookup or WHOIS tool to check the IP addresses found in the `Received` headers.

Verify whether:

* The IP belongs to the expected mail server.
* The hostname matches the IP address.
* The sending server appears legitimate.
* Any unexpected server or IP address is present.

### Step 6: Check SPF, DKIM, and DMARC

Record the authentication results.

| Check | Result    | Observation                                |
| ----- | --------- | ------------------------------------------ |
| SPF   | PASS/FAIL | Check whether the sending IP is authorized |
| DKIM  | PASS/FAIL | Check whether the DKIM signature is valid  |
| DMARC | PASS/FAIL | Check domain authentication and alignment  |

### Step 7: Analyze Message-ID

Check the domain used in the `Message-ID` and compare it with the sender's domain.

### Step 8: Identify Possible Spoofing Indicators

Check for:

* `From` and `Return-Path` domain mismatch
* Suspicious IP addresses
* Unexpected hostnames
* SPF failure
* DKIM failure
* DMARC failure
* Unusual timestamps
* Inconsistent mail-server routing
* Suspicious Message-ID domain

## Sample Header

```text
Received: from mail.example.com (mail.example.com [192.0.2.1])
  by mail.receiver.com with ESMTP id u29si8604336pjs.40.2023.08.10.07.00.16;
  Thu, 10 Aug 2023 07:00:16 -0700 (PDT)

Received: by mail.example.com with SMTP id a1mr1243772ywh.51;
  Thu, 10 Aug 2023 07:00:15 -0700 (PDT)

Message-ID: <CA+7eu=4pSeXgQ@mail.example.com>
```

## Analysis

* The email passed through `mail.example.com` before reaching `mail.receiver.com`.
* The sending IP address shown is `192.0.2.1`.
* The timestamps in the `Received` fields are in logical chronological order.
* The `Message-ID` contains the `mail.example.com` domain.
* SPF, DKIM, and DMARC results should be checked in the actual email header.
* Any authentication failure combined with domain or IP inconsistencies should be investigated as a possible spoofing attempt.

## Observation

The email header was successfully parsed using MHA. The sender information, mail-server path, IP address, Message-ID, and email authentication results were examined for inconsistencies.

## Result

The email header was successfully analyzed using Mail Header Analyzer, and possible email spoofing indicators were identified by examining the **Received, Return-Path, Message-ID, SPF, DKIM, and DMARC** fields.

## Conclusion

Email header analysis using MHA can be used to trace the email's delivery path and identify inconsistencies that may indicate email spoofing or phishing.

## Output Screenshots

<img width="1920" height="1080" alt="Screenshot 2026-08-23 221453" src="https://github.com/user-attachments/assets/83de6892-41db-49d4-8294-011a69f430bb" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 221628" src="https://github.com/user-attachments/assets/13cdbc25-0836-4d2f-ad8c-57e465d54c0d" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 221707" src="https://github.com/user-attachments/assets/b45e44d3-10cc-4c18-aabd-b526132935ad" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 221747" src="https://github.com/user-attachments/assets/881aa9d0-d5a1-41a1-8b92-e377544e006a" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 221843" src="https://github.com/user-attachments/assets/10af02f6-4108-4dbc-b082-963424611d8b" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 221913" src="https://github.com/user-attachments/assets/23be57e4-9e71-4392-a262-8aa0e267df56" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 221928" src="https://github.com/user-attachments/assets/de908080-afe9-4c6d-b95f-16d9696fea62" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 221958" src="https://github.com/user-attachments/assets/74ae8a0f-0871-4260-8a0b-a0753d62e3c2" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 222015" src="https://github.com/user-attachments/assets/897ebc16-dd42-4c15-85ec-b215337b555c" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 222056" src="https://github.com/user-attachments/assets/10377709-f0c2-47ed-bf19-a016295bce7e" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 222124" src="https://github.com/user-attachments/assets/ec78d40b-9d26-4dda-a3a3-0bad8759257f" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 222154" src="https://github.com/user-attachments/assets/93a2e3a5-e4a5-44d6-8685-34d5258c0465" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 222452" src="https://github.com/user-attachments/assets/cdb00629-1f9d-4e8b-bfaa-6c0bab75d81c" />
<img width="1894" height="632" alt="Screenshot 2026-08-23 222615" src="https://github.com/user-attachments/assets/4e8cff8f-ebe3-4a95-9ae2-b4255701a973" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 222645" src="https://github.com/user-attachments/assets/67b294a9-2de2-4400-9267-a627493f7958" />
<img width="1920" height="1080" alt="Screenshot 2026-08-23 222721" src="https://github.com/user-attachments/assets/78724a7c-cefb-424e-ab32-c72498454aa0" />
<img width="1889" height="189" alt="Screenshot 2026-08-23 222831" src="https://github.com/user-attachments/assets/b20dd892-e39f-49b3-98f4-7a5082812ac2" />
