# How I Prepared for and Passed the AWS Certified Cloud Practitioner Exam

> A practical look at CLF-C02 preparation, online-proctored exam day, what surprised me, and the small things I would tell another candidate to get right.

<!-- Suggested Hashnode tags: AWS, Cloud Computing, Certification, DevOps, Career -->

I recently sat for the **AWS Certified Cloud Practitioner (CLF-C02)** exam and passed.

The technical preparation mattered, but so did something I had initially underestimated: **the exam-day setup itself**.

An online-proctored certification exam is not just about knowing EC2, S3, IAM, VPCs, pricing models, and the shared responsibility model. You also need a compliant room, a working camera, stable internet, valid identification, and enough discipline to stay calm when the proctoring system interrupts you.

This article shares the practical lessons I would give another candidate. I am deliberately not sharing live exam questions or reconstructed exam content.

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
- **Global Accelerator**: improved global network routing and endpoint failover, not content caching.
- **EFS**: shared Linux file system.
- **FSx for Windows File Server**: Windows, SMB, Active Directory.
- **Site-to-Site VPN**: on-premises network to AWS over the internet.
- **Direct Connect**: dedicated private network connection.

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

That turned out to be useful because the verification process involved several steps before I could start the actual exam.

My advice is to be completely ready before the check-in window opens. Do not use the appointment time as the time you begin preparing your room or looking for your ID.

## Have a proper government ID ready

I prepared a **passport** for identification.

Whatever ID you use, make sure it meets the exact requirements in your current appointment instructions and that the name matches your booking.

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

- private room
- clear desk
- no books or notes nearby
- no watch or smartwatch
- no unnecessary electronics
- no second person in the room
- good lighting
- laptop connected to power
- strong, stable internet

Always check the current official rules because online-proctoring requirements can change.

## The proctor asked me to show the room

At the beginning, the proctor contacted me by video and asked me to walk them around the room using my **laptop camera**.

That is a good reason to prepare the entire room, not only the small area visible behind your laptop.

If your laptop is plugged in, arrange the cable so you can move the computer briefly without disconnecting anything.

## Put the phone away after verification

A phone may be used during the permitted verification process depending on the current check-in flow.

Once that stage is complete, put it away as instructed.

Do not leave it sitting beside the keyboard where reaching for it could look suspicious or violate the exam rules.

## My exam was paused because the proctor lost my camera feed

This was the most unexpected part of my session.

Partway through the exam, the proctor sent me a message saying they could no longer see my webcam feed.

From my side, it was not immediately obvious that anything had failed.

The exam was paused while the issue was checked. After roughly **three to four minutes**, I was able to resume.

That experience reinforced two things for me:

### 1. Stable internet matters

The proctor needs continuous video and audio, not just enough bandwidth to load exam questions.

Use the strongest and most stable connection available to you and test the exact setup before exam time.

### 2. Do not panic during a technical interruption

If the proctor pauses the exam, follow the instructions they give you.

Do not start randomly opening applications, changing network settings, or leaving the workstation unless instructed to do so.

The pause in my case was temporary and I resumed after the check.

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
2. Restart the laptop before check-in.
3. Close VPNs, messaging apps, screen recorders, and unnecessary background programs.
4. Plug the laptop into power.
5. Test the webcam, microphone, and speakers.
6. Prepare the entire room, not just the desk.
7. Keep valid ID ready before the check-in window opens.
8. Remove watches and unnecessary electronics.
9. Make sure nobody can enter the room.
10. Use good lighting and the most stable internet connection available.
11. Put the phone away after the permitted verification stage.
12. Stay calm if the proctor needs to pause or re-check something.
13. Flag uncertain exam questions and return to them.
14. Use extra time for a deliberate review before submitting.

## What I would not do

I would not rely on memorized question dumps or reconstructed live exam questions.

Apart from the exam-integrity issue, dumps are a bad way to learn AWS because product terminology and services change. Understanding why one service is better than another in a scenario is far more reusable.

I would also not spend the final hours learning deep implementation topics that the foundational exam does not require. At that stage, service recognition, security responsibilities, pricing distinctions, networking basics, and scenario reading are much higher value.

## A final word to anyone preparing

There will probably be a few questions where you pause and think, “Both of these look right.”

That is normal.

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
