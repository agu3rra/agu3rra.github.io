# SAP BTP Playground

!!! abstract "First published: 2026-08-16"

This post covers a brief introduction to what SAP is and how to begin getting hands-on practice with its technology free of charge.

## What is SAP?

SAP SE is a German multinational software corporation that develops enterprise software to manage business operations and customer relations. Founded in 1972 by five former IBM engineers in Weinheim, Germany. Since that's perhaps too much of a mouthful to remember, here's a more memorable version of it:

!!! quote "The coolest software company you have never heard of."
    <iframe width="560" height="315" src="https://www.youtube.com/embed/YyDM3LajCog?si=JKE-5G4_gXRsxn-c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## In the before times
Back when I first started working with SAP ERP systems ([back in 2009](https://www.linkedin.com/in/agu3rra/)), there were one of 2 ways you'd be able to learn anyting related to SAP: either you'd get lucky (like I did) and get hired by a company that had it and would teach you what it was and how it worked OR you'd self-sponsor some set of expensive certifications that would do the same.

Fortunately, a lot has changed since then and today, anyone with a regular computer and a cell phone is able to provision not only SAP's famous ERP system based on ABAP, but also its many different cloud offerings via SAP BTP.

The first step on this journey is getting yourself an SAP Account, and that's what we'll cover next.

## SAP Universal ID

!!! quote "SAP Universal ID is your personal, permanent digital identity for the entire SAP ecosystem."

Think of it as a single account that stays with you throughout your career, regardless of which company you work for or which SAP products you use.

It acts as a central wallet that ties together all your SAP user identities (such as S-users or P-users), preserves your learning certificates, community badges, and professional achievements, and gives you one place to manage them all in the SAP Universal ID account manager.

**Unlike a company account that you might lose when you change jobs, your SAP Universal ID is personal and belongs to you alone.**

> source: https://www.sap.com/account/universal-id.html

??? question "How does one link SAP accounts?"
    Your email address is the primary association key: Instead of manually linking accounts.
    All SAP user accounts that use the same email address will automatically be associated

#### Creating an SAP ID

Access [SAP Learning Login](https://learning.sap.com/?userlogin=true) and register for a new account.

??? question "What is SAP Learning?"
    SAP Learning is SAP’s learning ecosystem for building SAP skills through self-paced content, premium learning, live sessions, hands-on practice, and certification preparation. It includes resources for individuals and organizations, with options aimed at both free learning and subscription-based upskilling. More at https://learning.sap.com.

=== "Registration" 
    ![registration](./img/sap-id-registration.png)

=== "Confirmation message"
    ![cm](./img/sap-id-registration-email.png)

=== "Confirmed"
    ![confirmed](./img/sap-id-registration-confirmation.png)

Accessing SAP BTP does not require an SAP Universal ID (sorry), but you can **optionally** upgrade the account you have just created to one at https://account.sap.com/sam/my-account once you complete this step.

## SAP Business Technology Platform
SAP BTP is SAP’s cloud platform for building, extending, integrating, automating, and analyzing business applications and processes.

## Creating a BTP Trial environment
Access [SAP BTP Trial](https://account.hanatrial.ondemand.com/trial/#/home/trial).
Complete an account upgrade process by informing your phone and confirming the SMS code you'll receive.
Then, on the next page, select one of the available options for region and wait for provision to finish.

Once that happens, you should be able to see the main global account menu, then access the corresponding `trial` subaccount you've just provisioned.

??? info "Global vs. Subaccounts"
    - a **global account** is the top-level container that represents your contract with SAP and holds the entitlements, quotas, members, and subaccounts for your organization.
    - a **subaccount** is a child environment inside that global account where you actually deploy apps, use services, and manage subscriptions.

=== "Region selection"
    ![create-menu](./img/sapbtp-create-account.png)
    
=== "Provisioning"
    ![create-menu](./img/sapbtp-create-account-creating.png)

=== "Trial account"
    ![landing-page](./img/trial-account-landing.png)

=== "Subaccount"
    ![subaccount](./img/trial-subaccount.png)

!!! warning "How long do I have it for?"
    A trial account is valid for up to 90 days before your playground is destroyed.
    During that time, you can select a variety of SAP products and services to provision and learn through hand-on practice.
    After that period you can create a brand new environment from scratch if you want to keep exploring SAP softwares.

## Provisioning an SAP service
Talk about trial duration and possible services to provision. Then continue with a sample service and access it.

??? question "What is Cloud Foundry?"
    Explain without too much fuss.



![service-marketplace](./img/trial-service-marketplace.png)
