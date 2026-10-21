# Getting Started with Cisco Packet Tracer: Course Summary

*Cisco Networking Academy*

Okay, that's the whole course. Two modules, and now I can explain what Packet Tracer is, how to move around in it, and what all the different files and activities are. This is my wrap-up so everything sits in one place.


---

## The big picture

**Cisco Packet Tracer (PT)** is a simulator. It lets you explore networking **without buying equipment** and **without risking an existing network**.

It can simulate:

- Simple home networks
- Office networks
- IoT networks
- Even complex enterprise networks

And you can look at a network in two ways: as a **logical topology** (what's connected to what) or as a **representation of the physical network** (racks, cables, ports).

---

## Module 1: Download and Use Cisco Packet Tracer

### What I learned

Module 1 was about getting PT and getting comfortable with it. The main takeaways:

- PT is built for practicing without real hardware, and it's great for visualizing how a network is put together.
- The **Config tab** is specific to PT. It's a GUI that shows the **equivalent CLI commands** as you click, so it's a way to pick up the commands while you work.
- The **Desktop tab** (for some end devices) gives you IP configuration, wireless configuration, a command prompt, a web browser, and other apps.
- Servers have a **Services tab** for setting up common server processes like HTTP, DHCP, and DNS.
- I installed PT so I could do the **PTTA: Logical and Physical Mode Exploration**. It has a **hinting system and a built-in tutorial**. Other PTTAs have hints too, but not the tutorial.

### Device tabs cheat sheet

| Tab | What it's for |
|---|---|
| **Physical** | Power on/off, install modules |
| **Config** | PT-only GUI for basic settings (shows the equivalent IOS commands) |
| **CLI** | The real command line, using Cisco IOS |
| **Desktop** | IP config, wireless config, command prompt, web browser (end devices) |
| **Services** | HTTP, DHCP, DNS and other server processes (servers) |

---

## Module 2: Create a Cisco Packet Tracer Network

### What I learned

Module 2 showed me that PT has **more than one type of file**, and each one has its own purpose.

| File type | What it is |
|---|---|
| **.pka** | Packet Tracer **Activity**. The one I'll see the most. It has an instructions window, is usually scored, and contains two networks: an **initial network** and an **answer network** |
| **.pkt** | A simulated network that I built and saved. No instructions window, no scoring |
| **.pksz** | A **tutored activity** (PTTA). It bundles a .pka file, media assets, and a scripting file for the hinting system |
| **.pkz** | No longer used |

I also learned about the two ways PT is used for assessments:

- **PTMO** (Packet Tracer Media Object): a PT file used as part of an assessment question
- **PTSA** (Packet Tracer Skills Assessment): a standalone skills assessment

Then I used what I learned in the **Create a Simple Network** activity (a .pka file). In logical mode I **built a network, configured the end devices, and verified connectivity**. A video also showed some **advanced features** of PT, like putting background images on the workspace.

---

## Connecting the dots

Now that I've seen both modules, a few things link up:

- The **PTTA from Module 1** is a **.pksz** file. So the hints I used in that activity came from the scripting file bundled inside it.
- The **Create a Simple Network** activity is a **.pka** file. That's why it has an instructions window and scoring.
- A **.pkt** is what I get if I build my own network from scratch and save it.
- The **Config tab** and the **CLI tab** are basically two views of the same thing. Whatever I click in Config shows up as IOS commands.
- The **Desktop tab** and the **command prompt** are how I verify things, like checking that end devices are configured and connected.

---

## Key terms

| Term | What it means (my words) |
|---|---|
| **Packet Tracer (PT)** | A network simulator for practice without real equipment |
| **Logical topology** | The view of how devices connect and how data flows |
| **Physical representation** | The view of the physical layout |
| **Config tab** | PT-only GUI that also shows equivalent CLI commands |
| **Desktop tab** | End device tools like IP config and the command prompt |
| **Services tab** | Server settings for HTTP, DHCP, DNS, etc. |
| **PTTA** | Packet Tracer Tutored Activity, an activity with hints |
| **.pka / .pkt / .pksz / .pkz** | The four PT file types |
| **Initial network / answer network** | The two networks inside a .pka |
| **PTMO** | Packet Tracer Media Object, used in assessments |
| **PTSA** | Packet Tracer Skills Assessment, a standalone assessment |

---

## Can I explain these?

- [ ] What Packet Tracer is and why it's useful
- [ ] The difference between the logical and physical views
- [ ] What each device tab does
- [ ] How the four file types are different
- [ ] What PTMO and PTSA are
- [ ] How I'd build a simple network and check that it works

---

## What's next

The course says it best: **open Cisco Packet Tracer and keep exploring!** The more I build, the more all of this sticks.
