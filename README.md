# Defensive Security Monitoring for VSI

## Overview

This project presents a comprehensive defensive security monitoring solution developed to protect the **Virtual Systems Infrastructure (VSI)** from cyberattacks. Our analysis was driven by a potential threat from JobeCorp, suspected of launching cyberattacks aimed at disrupting VSI operations.

**Contributors:**  
- Hassan Evans  
- Drew Dickenson  
- Camron Neal  
- Harshini Lanka  

---

## Objective

To monitor and analyze system logs from Unix/Linux, Windows, and Apache servers to identify suspicious activities, detect anomalies, and propose effective mitigation strategies to enhance VSI's cyber defense posture.

---

## Monitoring Tools & Technologies

- **Splunk App Add-On for Unix and Linux**  
  Enables collection, parsing, and normalization of logs from Unix/Linux systems for analysis in Splunk.

- **Windows Logs**  
  Included system log reports, alert thresholds, and user behavior monitoring dashboards.

- **Apache Server Logs**  
  Analyzed HTTP request patterns, status codes, and geographic origin of traffic.

---

## Key Findings

### 🔍 Windows Attack Log Summary

- **Spike in Logs** on **March 25, 2020, at 8 AM** (35 logs).
- Suspicious activity at **11 AM (196 logs)** and **12 PM (77 logs)**.
- **User Account Lockouts** peaked at **896 occurrences** around **1–2 AM**.
- **Password Reset Attempts** spiked at **1,258 occurrences** between **8–11 AM**.
- **Users A and K** showed suspicious login behavior, with **User K** having more events.

### 🌐 Apache Log Analysis

- URI `/VSI_Account_logon.php` was targeted **1,323 times**, mainly from **Kiev** and **Kharkiv, Ukraine**.
- HTTP **POST requests increased by 29%**, suggesting brute-force login attempts.
- HTTP **404 status codes rose from 2% to 15%**, indicating probing or broken endpoint targeting.

---

## Mitigation Strategies

- **Enable Two-Factor Authentication (2FA)** – Critical to prevent brute-force password attacks.
- **Implement Account Lockouts** – After a set number of failed login attempts.
- **Lower Thresholds for Account Lockouts and Password Resets** – To catch attacks earlier.
- **Geo-IP Filtering** – Block traffic from high-risk regions outside the U.S.

---

## Dashboards & Reports

The project includes Splunk dashboards and visual reports covering:
- User and Signature-based attack analysis.
- Windows log event trends and alerts.
- Apache traffic behavior and top domain analysis before and after attacks.

---

## Conclusion

This monitoring solution provides actionable insights into potential threats against VSI. By proactively tracking log anomalies, enforcing stricter access control measures, and deploying Splunk-powered alerts and dashboards, VSI can better defend against future cyber threats.
