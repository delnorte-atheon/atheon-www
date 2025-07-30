---
layout: single
title:  "Why Email Encryption Doesn't Really Matter"
author: Vulpecula
author_profile: true
categories: email
---

In the world of digital security, few myths are as stubbornly persistent as the notion that simply encrypting your email makes it "secure." It's a comfortable illusion, I'll give it that. But for anyone serious about privacy and OPSEC, it's integral to understand that email, *by its design*, is fundamentally, irrevocably insecure for private communication, regardless where you layer PGP, S/MIME, or any other content encryption on top.


## Metadata

Let's assume you are able to encrypt the contents of your email securely, and only your recipient can decrypt this (even if intercepted, let's assume the attackers cannot access the plaintext contents of the email). The metadata of your email which remains unencrypted by design, reveals a lot about who, what, and where the communications are occurring.

Consider the standard email header, an unencrypted, plaintext dossier attached to every single message. You have the sender, recipient(s), subject line, timestamps, IPs, email client/software info, message ID, etc.

Metadata is everything. State actors like the NSA don't necessarily need to decrypt your conversations if they can track *who* you're talking to, when, and where. That is the very essence of **traffic analysis**. Knowing that an activist if frequently communicating with a journalist, researcher with a foreign national, or an employee with a competitor, even without knowing exact words, provides an incredibly rich intelligence picture. Corporations use similar patterns to build psychological profiles for targeted advertising, insurance risk assessment, and other predictive analytics.


## Email Architecture

Email's default plaintext nature is its fatal flaw. Even when a message is encrypted, a totally reasonable person might reply, quote the unencrypted original, or forward it to an insecure recipient. Human error, exacerbated by poor user experience in most PGP clients, is a constant attack vector for information leak.

Traditional PGP also doesn't inherently offer perfect forward secrecy. This means if your long term private key is ever compromised (e.g., your computer is seized years later), every single message you've ever encrypted with that key can be decrypted. And while modern OpenPGP and `age` use ephemeral keys or ECC to improve PFS, the *email transport* itself doesn't enforce it across the chain of communication, nor do most users consistently configure it. Even attachment, if encrypted, still leave a trail. Their filenames, sizes, and even types can be exposed as metadata as well.

Did I mention email is notoriously prone to spoofing? While you can digitally sign a message to prove its authenticity, the "From" address can easily be faked. Mechanisms like SPF, DKIM, and DMARC exist to combat this, but their implementation is inconsistent and often overlooked.

There is no guarantee of delivery or recipient. Email is a "store-and-forward" system. There's no inherent realtime handshaking. You send it, and you hope it gets there. There's not inherent mechanism to confirm the email was delivered, much less read (in a secure way).  

And naturally, the final nail in the coffin: server side storage and trust. Unless you are self hosting your own mail server (and have impeccably good security practices), your emails, encrypted or not, will be sitting on third party servers (Gmail, Outlook, etc.). You are trusting these providers with your data. They have legal access to metadata, and potentially to unencrypted content if you or your recipient ever made a mistake.

So why did we have you send us an email using PGP then? Oh, that's so we can track you!! 

It's really just intended to be a first hands-on encounter with practical cryptography. We want you to feel the direct, tangible sensation of taking a little more control over your communication. We believe this instills a crucial understanding: that true privacy often requires a bit of effort, when it really shouldn't. But a majority of the world can't be bothered, which is what we're trying to change (including you)!


## So, is Matrix "Safe Enough"?

Matrix is a good step in the right direction. Most modern Matrix clients (like the one we use, Element) have E2EE on by default with an open standard. 

You might still be asking... well, what about the metadata? And you'd be right. Matrix, being a decentralized protocol, requires you to either self host a server or rely on a federated, public homeserver (like `matrix.org`), which you have to trust. These servers will see your metadata just like email providers do.

Naturally, the next question that follows is, "So why do we even use the Matrix protocol?" Matrix is still a good choice for primary communication. It's miles ahead of email out of the box and even more so if done correctly. We are currently working on a homeserver implementation of the protocol, and we hope that this will suffice for a school club. Even then, we're more so focused on the privacy side of things (public Matrix homeservers don't tend to broker your data) than security *as of now*.


## Now What

We recommend using Signal as your primary messenger. Signal uses the Signal Protocol, providing pretty good forward secrecy in addition to minimzing metadata (only phone number used to register, the date of registration, and the date of last use). Now, the reason we don't use this is because we require communications between relatively large groups of people, but I digress. 

There are also options like Session and Briar, if you do so desire.


## Ok And?

Ok, your emails aren't secure, and the chat we use isn't secure. What are you trying to tell me?!

Our mission here is to provide people with the knowledge, tools, and critical thinking needed to navigate the current digital world. We aim to help people understand the sheer complexity of privacy, and to move beyond the simple binary "encrypted/unencrypted" talk.

*Understanding* is the most elaborate form of defiance. While you can't really have perfect privacy, you can have *pretty good privacy* (hehe, get it? PGP?), and it's in that fact that we hope modern society will come to realization of the fundamental right to human privacy.