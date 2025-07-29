---
layout: splash
title: Join
permalink: /join/
---

# First Contact

## Objective

As part of the club's privacy conscious and security focused induction process, you are required to establish a secure, authenticated channel of communication using Pretty Good Privacy (PGP). This is your first contact task and serves as both an introduction to applied cryptography and a demonstration of digital security.


## Scope of the Challenge

You will initiate contact with the club by sending a **PGP encrypted email** to a designated club email address. This message must contain specific components outlined below and must be encrypted using the club's private key. This exercise is designed to simulate a basic operational security protocol.


## Deliverables

You must compose and send an email to the club's designated address `delnorte.atheon@protonmail.com`, containing the following elements:

1. **Your Public PGP Key**

    This can be provided as a file attachment (`.asc`) or pasted inline.

    Include the associated fingerprint so we can verify authenticity.

2. **A Chosen Pseudonym**

    This alias will be used for the next step of communications (your official pseudonym may be chosen after completing this First Contact task).

    Ensure that it does not reveal your real world identity.

3. **Statement of Intent**

    A brief, personal message explaining your interest in the club and its mission.

    This will help us understand your motivations and alignment with our values.

It is recommended to create a new email address that does not reveal *as much* personal information as a simple full name, but both options work for our purposes.


## Technical Requirements

You are expected to use a modern, standards-compliant PGP implementation (e.g., GnuPG). We recommend against using RSA in favor of ECC. This organization's public key will be available below.

Ensure that your message is encrypted with the provided key and NOT sent in plaintext.


## Security Notes

- Do NOT send sensitive personal information at this stage.

- This First Contact will be facilitated via a third-party service (i.e., ProtonMail and the client's email provider), so understand the implications regarding metadata exposure.


## Information

Email: `delnorte.atheon@protonmail.com`

Pubkey: [keys.openpgp.org](https://keys.openpgp.org/vks/v1/by-fingerprint/D7D883B68465FF38A58A58CCEA2F1D0CD82B6184)

Fingerprint: `D7D8 83B6 8465 FF38 A58A 58CC EA2F 1D0C D82B 6184`


## Disclaimer

Welcome to Del Norte Atheon Group.

While this PGP exercise is intended to act as an introduction to security concepts, it is critical to understand its limitations for ongoing, truly private communication.

Email, by design, suffers from inherent weaknesses (such as metadata leakage, exposed subject lines, and the lack of perfect forward secrecy) that makes it unsuitable for sensitive discussions. In fact, encrypted email offers very little security given a malicious actor can very much obtain information as critical as metadata (most mass surveillance is more so focused on metadata than actual contents usually, anyway). This exercise is intended to facilitate your understanding of public key infrastructure and to establish an encrypted channel for your First Contact task. if you're still curious, here's a [good read](https://soatok.blog/2024/11/15/what-to-use-instead-of-pgp/).

Upon successful completion of this task, all sensitive club communications will transition to more robust, privacy-preserving platforms that better mitigate these concerns. 