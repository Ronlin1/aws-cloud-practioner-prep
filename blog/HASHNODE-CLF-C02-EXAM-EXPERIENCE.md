# How I Prepared for and Passed the AWS Certified Cloud Practitioner Exam

> A practical look at CLF-C02 preparation, online-proctored exam day, what surprised me, and the small things I would tell another candidate to get right.

<!-- Suggested Hashnode tags: AWS, Cloud Computing, Certification, DevOps, Career -->

I recently sat for the **AWS Certified Cloud Practitioner (CLF-C02)** exam and passed.

The technical preparation mattered, but so did something I had initially underestimated: **the exam-day setup itself**.

An online-proctored certification exam is not just about knowing EC2, S3, IAM, VPCs, pricing models, and the shared responsibility model. You also need a compliant room, a working camera, stable internet, valid identification, and enough discipline to stay calm when something technical goes wrong.

This article shares the practical lessons I would give another candidate. I am deliberately not sharing live exam questions or reconstructed exam content.

> **Policy note:** Online-proctoring rules can change. The details below were rechecked against Pearson VUE's AWS OnVUE requirements on **September 26, 2026**. Always verify your own current appointment instructions.

## What I focused on before the exam

I treated CLF-C02 as a **service-recognition and cloud-concepts exam**, not as an architecture or implementation exam.

For each important AWS service, I tried to know four things:

1. What problem does it solve?
2. What wording in a scenario should make me think of it?
3. Which AWS service is it commonly confused with?
4. What does it *not* primarily do?

That approach was more useful than memorizing long definitions.

For example:

- **CloudTrail**: API/account activity. Think, “Who changed or deleted this resource?”
- **CloudWatch**: metrics, logs, alarms, observability.
- **AWS Config**: resource configuration history and compliance.
- **CloudFront**: CDN and content caching at the edge.
- **Global Accelerator**: improved global network routing and endpoint availability, not content caching.
- **EFS**: shared Linux file system.
- **FSx for Windows File Server**: Windows, SMB, Active Directory.
- **Site-to-Site VPN**: on-premises network to AWS over an encrypted internet connection.
- **Direct Connect**: dedicated network connection.

Those distinctions mattered because many questions present several answers that are technically related, but only one satisfies the complete requirement.

## I built my preparation around the actual exam blueprint

The Cloud Practitioner exam is broad, so I avoided trying to learn every AWS product equally.

I prioritized:

- Cloud concepts and AWS global infrastructure
- Shared responsibility
- IAM and security basics
- Compute, storage, databases, and networking
- Monitoring and governance
- Pricing models and cost-management tools
- AWS Support and partner resources
- Common service comparison traps

I also used a public study repository that I had been refining while preparing:

[**AWS Certified Cloud Practitioner CLF-C02 Prep Repository**](https://github.com/Ronlin1/aws-cloud-practioner-prep)

It contains concise domain notes, service comparisons, practice questions, targeted gap drills, and official AWS resources.

## Exam day: start check-in early

I began the check-in process about **25 minutes before my scheduled exam time**.

Pearson's current AWS OnVUE guidance says candidates should **begin check-in 30 minutes before the appointment**, so I would now recommend being completely ready before that window opens.

Do not use the appointment time as the time you begin preparing your room or looking for your ID.

## Have a proper government ID ready

I prepared a **passport** for identification.

Pearson currently accepts an international passport among its approved government-issued IDs. Whatever ID you use, make sure the name exactly matches the exam booking.

Do not wait until the check-in screen to discover a mismatch.

Also, if you are writing publicly about your experience later, never publish:

- passport or national ID numbers
- candidate IDs
- registration numbers
- appointment tokens
- QR codes or barcodes
- screenshots containing personal details

## No watch, no notes, and nobody else in the room

I prepared a private room and cleared the workspace.

I removed my watch, kept study materials away, and made sure **no one else was in the room**.

Good lighting is also worth thinking about. The proctor needs to see you clearly, and a dim or backlit room can create unnecessary friction.

A practical room checklist is:

- private, quiet room
- clear desk
- no books, notes, paper, or pens nearby
- no watch or smartwatch
- no headphones or earbuds
- no unnecessary electronics
- no second person in the room
- **one display only**
- good lighting
- laptop connected to power
- strong, stable internet

Pearson currently prohibits public spaces such as libraries and coffee shops for OnVUE testing.

## The proctor asked me to show the room

At the beginning, the proctor contacted me by video and asked me to walk them around the room using my **laptop camera**.

Pearson's current check-in process includes a **360-degree room scan**, so prepare the entire room, not only the small area directly behind your laptop.

If your laptop is plugged in, arrange the cable so you can move the computer briefly without disconnecting anything.

## Run the system test on the exact setup you will use

Pearson currently says to run and pass the OnVUE system test on the **same device and network** you plan to use for the real exam.

I would test:

- computer
- webcam
- microphone
- speakers
- internet connection
- intended room/location

Then, before check-in:

- restart the laptop
- close unnecessary background apps
- disable VPN software
- disconnect additional displays
- plug the laptop into power

## Your internet connection needs to be more than “working”

The proctor needs continuous video and audio, not just enough bandwidth to load exam questions.

Pearson currently states minimum connectivity of:

- **6 Mbps download**
- **2 Mbps upload**

It also currently prohibits:

- VPNs
- corporate networks
- public/shared networks

and recommends ensuring nobody else is consuming the connection with large downloads or streaming during the exam.

Use the strongest, most stable **compliant** connection available to you and test it in advance.

## My webcam feed disappeared for the proctor

This was the most unexpected part of my session.

Partway through the exam, the proctor sent me a message saying they could no longer see my webcam feed.

From my side, it was not immediately obvious that anything had failed.

My **testing session was temporarily interrupted while the issue was checked**. After roughly **three to four minutes**, I was able to resume.

One important nuance: Pearson's current public guidance says an in-exam proctor **cannot formally pause or extend the exam timer**. So I describe what happened as a temporary session interruption rather than assuming the timer itself was officially paused.

That experience reinforced two things for me.

### 1. Stable internet matters

Use the strongest and most stable compliant connection available to you and test the exact setup before exam time.

### 2. Do not panic during a technical interruption

If something goes wrong, follow the proctor and on-screen instructions.

Do not start randomly opening applications, changing network settings, or leaving the workstation unless instructed to do so.

Pearson says to use the in-exam chat to reach a proctor. If the computer freezes or disconnects, follow the current relaunch instructions for OnVUE.

## Put the phone away after verification

A phone may be used during the permitted verification process depending on the current check-in flow.

Once that stage is complete, put it away as instructed.

Pearson's current rule is that you should **not access your phone during the exam unless explicitly permitted by a proctor**.

Do not leave it beside the keyboard where reaching for it could look suspicious or violate the rules.

## Some questions are trickier than they first appear

Cloud Practitioner is a foundational certification, but “foundational” does not mean every question is obvious.

A recurring challenge is that multiple answers can look correct until you notice one word in the scenario.

Watch for qualifiers such as:

- **BEST**
- **MOST cost-effective**
- **fully managed**
- **without interruption**
- **least operational overhead**
- **dedicated connection**
- **over the internet**
- **private**
- **highly available**

For example, “lowest cost” and “lowest cost without interruption” can lead to very different EC2 purchasing choices.

Similarly, “global low-latency content delivery” and “global traffic routing to healthy endpoints” sound close, but they point toward different networking services.

My approach was to ask:

> Which option satisfies every requirement in the scenario, not just one keyword?

## I finished early, then reviewed twice

I completed the first pass with time left.

Rather than submit immediately, I went through my answers **two more times**.

That was valuable because some mistakes come from reading too quickly rather than not knowing the technology.

If you have time remaining:

- revisit flagged questions
- re-read multiple-response questions carefully
- check qualifiers such as BEST and MOST
- verify that the answer fits every requirement
- avoid changing an answer unless you can clearly explain why your new choice is better

Finishing early is useful only if you use the remaining time well.

## The small things I would do again

If I were sitting another online-proctored AWS exam tomorrow, I would repeat these habits:

1. Run the official system test on the exact computer and network I will use.
2. Confirm at least 6 Mbps download and 2 Mbps upload on a stable connection.
3. Avoid VPNs, corporate networks, and public/shared networks.
4. Restart the laptop before check-in.
5. Close messaging apps, screen recorders, VPNs, and unnecessary background programs.
6. Plug the laptop into power.
7. Test the webcam, microphone, and speakers.
8. Use one display only.
9. Prepare the entire room, not just the desk.
10. Keep valid ID ready before the check-in window opens.
11. Remove watches and unnecessary electronics.
12. Make sure nobody can enter the room.
13. Use good lighting.
14. Put the phone away after the permitted verification stage.
15. Stay calm if the proctor needs to re-check something.
16. Flag uncertain exam questions and return to them.
17. Use extra time for a deliberate review before submitting.

## What I would not do

I would not rely on memorized question dumps or reconstructed live exam questions.

Apart from the exam-integrity issue, dumps are a bad way to learn AWS because product terminology and services change. Understanding why one service is better than another in a scenario is far more reusable.

I would also not spend the final hours learning deep implementation topics that the foundational exam does not require. At that stage, service recognition, security responsibilities, pricing distinctions, networking basics, and scenario reading are much higher value.

## A final word to anyone preparing

There will probably be a few questions where you pause and think, “Both of these look right.”

Read the requirement again. Look for the word that changes the scenario. Eliminate anything that fails even one condition.

And if you finish with time left, review your work.

The combination that helped me most was:

> **Understand the cloud concepts. Learn the service distinctions. Practice scenarios. Prepare the exam environment early. Stay calm.**

You do not need to know everything in AWS to pass a foundational AWS certification.

You need to understand the map well enough to recognize the right path.

You've got this.

---

### Useful links

- [AWS Certified Cloud Practitioner](https://aws.amazon.com/certification/certified-cloud-practitioner/)
- [AWS Certification Exam Prep](https://aws.amazon.com/certification/certification-prep/)
- [Pearson VUE AWS online testing](https://www.pearsonvue.com/us/en/aws/onvue.html)
- [My public CLF-C02 prep repository](https://github.com/Ronlin1/aws-cloud-practioner-prep)

> **Disclosure:** This is an independent personal experience. It is not affiliated with or endorsed by AWS or Pearson VUE. Exam procedures and policies can change, so always verify the latest official instructions before your appointment.
