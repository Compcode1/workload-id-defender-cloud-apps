
PROJECT PLAN: AUTOMATED NON-HUMAN IDENTITY HARDENING
================================================================================

1. PROJECT OVERVIEW:
   Human logins are protected by multi-factor authentication, but software 
   applications, automation scripts, and background services (known as service 
   principals) cannot pass an interactive security challenge. This project uses 
   Microsoft Entra Workload ID to assign strict security perimeters to these 
   non-human services, and integrates them directly into Microsoft Defender for 
   Cloud Apps. This allows the system to continuously monitor the behavior of 
   machine accounts, flag anomalous data downloads, and automatically block 
   compromised software connections in real time.

2. STEP-BY-STEP EXECUTION PLAYBOOK:

   * STEP 1: Inventory and Target Identification
     Open the Microsoft Entra ID portal, navigate to Application Registrations, 
     and select a dedicated non-human service principal or automated script 
     account to act as our primary deployment target.

   * STEP 2: Enable Workload Identity Premium Capabilities
     Verify that Microsoft Entra Workload ID licensing is active within your 
     tenant to unlock advanced conditional access security policies tailored 
     specifically for machine identities.

   * STEP 3: Configure Cloud App Discovery and Integration
     Open the Microsoft Defender for Cloud Apps management portal and ensure the 
     Microsoft Entra ID directory connector is fully linked. This establishes the 
     bidirectional data stream that feeds application events directly into the 
     cloud monitoring system.

   * STEP 4: Build a Conditional Access Policy for the Service Principal
     Create a new conditional access security policy targeted strictly at your 
     non-human asset. Configure a condition that evaluates the location or risk 
     state of the service principal, forcing an access block if a connection 
     originates from an unverified Internet Protocol address.

   * STEP 5: Deploy Anomaly Detection and Automated Governance Actions
     Inside Microsoft Defender for Cloud Apps, create an activity alert policy 
     that monitors the selected application for mass data extraction or unusual 
     privilege escalations. Set the automated governance remediation to instantly 
     disable the compromised Microsoft Entra ID service principal the moment an 
     alert triggers.

   * STEP 6: Execute Validation Testing
     Simulate a malicious credential leak by invoking an automated terminal call 
     from an unauthorized outside network. Verify that the system instantly detects 
     the variance, generates a high-severity alert, and successfully disables 
     the machine identity automatically.
================================================================================
