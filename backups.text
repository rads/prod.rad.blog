---
title: Backups
---

*plural noun*

> things that can be called on if necessary; reserves.

## My Home Backup System

When I put effort into something [I want to keep it around](bliki). That's why I'm paranoid about my backups.

### Structure

- Offsite
    - **Dropbox**
        - Schedule
            - Continuous
    - **CrashPlan**
        - Schedule
            - Continuous
- Onsite
    - **Time Machine**
        - Schedule
            - Continuous
        - Hardware
            - QNAP TS-251 NAS
            - APC Back-UPS 550
    - **Carbon Copy Cloner**
        - Schedule
            - Daily at 3:30am
        - Hardware
            - 1TB Western Digital SSD over USB

### Notes

I do all of my work in the Dropbox folder. This means the files are backed up as soon as I save them. It also gives me a limited form of version control (though if I need more I'll use a local Git repository).

Time Machine is enabled on each Mac. Since this part of the backup has a higher delay than Dropbox, I don't rely it on for files I'm actively working on.

CrashPlan runs on each machine (including the NAS). Since the local disks contain Time Machine archives, all the machines *and* their history are replicated to CrashPlan. The full Time Machine archive is safe as long as at least one copy, local or remote, is preserved. The NAS is setup in a RAID-1 array with large disks to tolerate individual hardware failures and perserve as much history as possible.

The only realistic scenario where I can lose data is if my local backups and CrashPlan fail at the same time. That said, I'm lacking a routine for testing the backups. For example, if something goes wrong with Time Machine, the bad version will still get backed up to CrashPlan.
