# Module 2 Notes: Create a Cisco Packet Tracer Network

*Getting Started with Cisco Packet Tracer, Cisco Networking Academy*

Okay, Module 2. In Module 1 I learned my way around the interface. Now it's about the stuff you actually run into when you use Packet Tracer in a course: the file types, the assessments, and finally building a network. Let's go.

---

## 2.0 Packet Tracer File Types

### 2.0.1 The four file types

At first I thought a file is just a file, but Packet Tracer has **four different types**, and each one has its own job:

`.pka`, `.pkt`, `.pksz`, and `.pkz`

Here they are side by side:

| File type | What it is | Instructions window? | Scored? |
|---|---|---|---|
| **.pka** | Packet Tracer **A**ctivity | Yes | Usually yes |
| **.pkt** | A simulated network you built and saved | No | No |
| **.pksz** | Packet Tracer **Tutored** Activity (PTTA) | Yes (it bundles a .pka) | Yes, plus hints |
| **.pkz** | Old file type, now deprecated | No | No |

Now a bit more on each one.

#### .pka: the activity file

This is the one I'll see **most often**. An easy way to remember it is that the **"a" means "activity."**

What makes it special:

- It has an **instructions window** with the steps to complete the activity, assignment, or assessment
- It's usually **scored**
- The instructions window can show a **completion percentage**
- The **Check Results** feature can be turned on to give feedback

The part I found interesting is that a .pka file contains **two networks**:

1. **Initial network**: this is the one that opens when you launch the activity. It's what you work on.
2. **Answer network**: this runs **in the background** and is used for scoring and feedback. As a learner, you **can't access it**.

> So the way it grades you is by comparing what you built to a hidden "right answer" network. That's how the completion percentage knows how far along you are.

#### .pkt: the saved network

This is what you get when you **build a network in Packet Tracer and save it**. It can also have **background images** embedded in it. But there's **no instructions window and no scoring**.

> Simple way to think about it: .pka is a worksheet with an answer key. .pkt is a blank sheet of paper you drew on.

#### .pksz: the tutored activity

This one is specific to **PTTAs** (Packet Tracer Tutored Activities). Remember those from Module 1, the ones with the hint levels? Those use this file type.

A .pksz bundles together:

- A **.pka file**
- **Media assets**
- A **scripting file for the hinting system**

That bundle is what gives students **contextualized hints** while they work.

#### .pkz: the old one

You'll still see **Save As PKZ...** in the File menu. It used to be for embedding images and other files into a Packet Tracer file. But now images are **embedded directly in a regular .pkt or .pka by default**, so .pkz isn't needed anymore. It's considered **deprecated**.

---

### 2.0.2 Packet Tracer assessments

Packet Tracer isn't just for practice. It's also used in **two types of assessments**:

| | **PTMO** | **PTSA** |
|---|---|---|
| **Stands for** | Packet Tracer Media Object | Packet Tracer Skills Assessment |
| **File type** | .pkt or .pka | Its own standalone assessment |
| **Where it shows up** | Inline with a question in a quiz, module exam, or other graded assessment | Mid-point or end of a course |
| **What you do** | Configure or investigate the network, then answer a multiple choice question | Implement the technologies you learned |
| **Grading** | Through the quiz question you answer | Its own grading engine, with results recorded in the course gradebook (if there is one) |

#### How a PTMO works (from the video)

1. In a module exam, you'll see questions (multiple choice, single answer or multiple answer)
2. At the PTMO question, there's a **link to download a PT Activity**
3. Open it, **read the instructions**, and do the tasks
4. Close Packet Tracer and **go back to the question**
5. **Select your answer**

#### How a PTSA works (from the video)

1. At the end of the course, click **Take Assessment**
2. In the next window, click **Start Assessment**
3. Packet Tracer **loads**
4. Go through the instructions and complete the assessment items
5. **Don't close Packet Tracer itself.** Go back to the **browser window** and click **Submit Assessment**

> That step 5 is easy to mess up. Submitting happens in the browser, not in Packet Tracer.

#### Feedback after a PTSA

The amount of feedback depends on the exam. You might get:

- **Personalized feedback**: you can look at it, print it, or email it
- **Detailed item feedback**: shows your proficiency in each performance component and detailed info about each component in the exam

You also get **item level feedback for each graded component** after finishing a PTSA.

---

## 2.1 Build a Home Network

### 2.1.1 Using .pka activities: finding an end device's IP address

*(The course labels this 2.2.1, but it's in the 2.1 section.)*

This video is a prep for the activity. It shows **two ways to find the IP address info** on a device. This stuff connects directly to networking basics: IP address, subnet mask, and default gateway.

#### Way 1: the Config tab

On the **PC**:

1. Click the PC, then go to the **Config** tab
2. Click the **FastEthernet0** interface
3. Look at the IP settings

What the PC shows:

| Setting | Value | What it means |
|---|---|---|
| **Addressing** | Static | I set it myself, it's not automatic |
| **IP address** | 192.168.1.3 | The device's unique address on the network |
| **Subnet mask** | (shown on the same screen) | Tells me which part of the address is the **network** and which is the **host** |
| **Default gateway** | 192.168.1.1 | The way out of my local network (found under **Settings**) |

The subnet mask part clicked for me like this: the address has four parts, and in this example the **first three parts are the network portion** and the **rest is the host portion**. (That works out to a mask of 255.255.255.0.)

#### Way 2: the command prompt

1. Click the device and go to the **Desktop** tab
2. Open the **Command Prompt**
3. Run `ipconfig`

You'll see the **IPv4 address, subnet mask, and default gateway**. They're the same values as in the Config tab. It basically acts like a **Windows machine emulated inside Packet Tracer**.

#### The laptop is different: DHCP

Now look at the **laptop**. In the Config tab under FastEthernet0, the address is **grayed out**.

Why? Because of **DHCP** (Dynamic Host Configuration Protocol):

- The laptop **asked a DHCP server** for an address
- The server **assigned** it automatically
- So I can see the IP address and subnet mask, but I **can't edit them**
- The **default gateway under Settings is grayed out too**, because that came from the DHCP server as well
- Running `ipconfig` from the Desktop tab still shows the IP address, subnet mask, and default gateway

| | **PC** | **Laptop** |
|---|---|---|
| Address type | Static (typed in by hand) | DHCP (assigned automatically) |
| In the Config tab | Editable | **Grayed out** |
| Default gateway | Set manually | Received from DHCP |
| `ipconfig` | Shows all the values | Shows all the values |

> Trick to remember: **grayed out = it came from DHCP.** If I can type in the box, it's static.

---

### 2.1.2 Packet Tracer activity: Create a Simple Network

This is the hands-on part. It's a **.pka** file, so it has the instructions window and scoring I learned about in 2.0.1.

**Objectives:**

- **Part 1:** Build a simple network
- **Part 2:** Configure the end devices and verify connectivity

You don't need any networking experience. The **instruction file gives step-by-step directions**. Use the **left button** to open the instructions and the **right button** to download the `.pka` file.

---

### 2.1.3 Advanced features: customizing backgrounds

You can put **background images** on the workspace. Here's how:

1. Click the **Background Image** icon in the upper right
2. Click **Browse**
3. Pick an image
4. Click **Apply**, close the window, and zoom out to see the full image

You've got two options:

- **Built-in images**: for example, the *building* image shows a schematic of a building or floor
- **Custom images**: in the video they used a **campus map** and a **city map**

Once the city map is applied, you can **move the routers to where they'd be in each of the buildings** in the city. So your topology can actually match a real place.

> This connects back to the file types: .pkt and .pka files can have these background images **embedded** in them, which is why .pkz isn't needed anymore.

---

## Key terms

| Term | What it means (my words) |
|---|---|
| **.pka** | Packet Tracer Activity file, with an instructions window and scoring |
| **.pkt** | A saved network you built, with no instructions or scoring |
| **.pksz** | Tutored activity file that bundles a .pka, media, and the hint script |
| **.pkz** | Old, deprecated file type for embedding images and files |
| **Initial network** | The network you work on when a .pka opens |
| **Answer network** | The hidden network in a .pka that's used for scoring and feedback |
| **Instructions window** | The panel in a .pka with the steps and completion percentage |
| **Check Results** | A feature that can be turned on to give feedback in an activity |
| **PTTA** | Packet Tracer Tutored Activity, with hints |
| **PTMO** | Packet Tracer Media Object, a .pkt or .pka file launched from inside a quiz question |
| **PTSA** | Packet Tracer Skills Assessment, a standalone test at the mid-point or end of a course |
| **Gradebook** | Where PTSA results are recorded (if the course has one) |
| **IP address** | A device's unique address on the network |
| **Subnet mask** | Shows which part of the IP address is the network and which is the host |
| **Default gateway** | The device's way out of the local network |
| **Static addressing** | An address you set manually |
| **DHCP** | Dynamic Host Configuration Protocol, which hands out addresses automatically |
| **`ipconfig`** | Command that shows IP address, subnet mask, and default gateway |
| **Background image** | An image behind the workspace (like a city map) |

---

## Quick summary

- Packet Tracer makes **four file types**: .pka, .pkt, .pksz, and .pkz (deprecated).
- **.pka** = activity with instructions and scoring. It contains an **initial network** and a hidden **answer network**.
- **.pkt** = a network you built and saved, with no instructions or scoring.
- **.pksz** = tutored activity (PTTA) that bundles a .pka, media, and the hinting script.
- Packet Tracer is used in two assessments: **PTMO** (inline in a quiz question, .pkt or .pka) and **PTSA** (standalone skills test with its own grading engine).
- When you finish a PTSA, **submit from the browser**, not from inside Packet Tracer.
- You can check a device's IP info through the **Config tab** or **`ipconfig`** in the Desktop tab's command prompt.
- **Static** = typed in by hand. **DHCP** = automatic, and the fields are grayed out.
- You can add **built-in or custom background images** to line up your topology with a real map.

That's the end of the course. Packet Tracer shows up in lots of other Cisco Networking Academy courses, so I'll be using all of this again.
