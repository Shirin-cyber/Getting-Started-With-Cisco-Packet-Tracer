# Module 1 Notes: Download and Use Cisco Packet Tracer

*Getting Started with Cisco Packet Tracer, Cisco Networking Academy*

Okay, so this module is all about meeting Packet Tracer. Before it, networking for me was kind of abstract: routers, switches, cables, all in theory. Packet Tracer is the thing that lets you actually *see* it and try it. Let's go through it.

---

## 1.0 Install Cisco Packet Tracer

### 1.0.1 What is Packet Tracer?

Short version: it's a **virtual lab on your computer**. You don't need any real hardware to practice networking, Internet of Things (IoT), or cybersecurity. And the best part is it's **free**.

It has a few different ways to look at things:

- **Simulation mode**: this is where you see how a network actually works. You build a logical view, set up your devices, and then follow the data packets as they travel. You can even open a packet and look inside it.
- **Physical mode**: this shows how the logical drawing turns into real-looking stuff. You get a device rack, you pick the right cables, you pick the right ports.
- **Built-in tutor**: gives you hints while you work, but only if you want them.

And once you're comfortable, you can go further with IoT devices, Python code, and network automation.

> So it's not just "draw boxes and lines." It goes from the big picture all the way down to the cable in the port.

### 1.0.2 First time in the course

The course is for new Packet Tracer users. That includes people with zero networking background, people with some, and people whose other course needs Packet Tracer.

What you can do with it:

- Build a network from scratch
- Use a pre-built sample network
- Complete lab assignments

One thing to keep in mind: Packet Tracer is **not a replacement** for practicing on real routers, switches, firewalls, and servers. But it's still really useful because you can practice config and troubleshooting without owning any of that.

**Where to get help:**

- FAQs: <https://www.netacad.com/help> (or click Help in the top bar)
- Download help: <https://www.netacad.com/resources/lab-downloads> (scroll to Learning Resources)
- **Morgan**, the virtual assistant, via the chat icon in the top right. It can help with Packet Tracer, certificates, and badging.

### 1.0.3 Downloading it

Everything starts at: <https://www.netacad.com/resources/lab-downloads>

### 1.0.4 Why take this course?

The pitch is basically: what if you could see inside a small business network, or even the internet? Or set up an IoT system that alerts your phone when something's wrong at home?

The course has **two modules**:

| Module | What happens | Content |
|---|---|---|
| 1. Download and Use Cisco Packet Tracer | Install the software, explore the interface | Text, 7 videos, 1 hands-on exploration activity |
| 2. Create a Cisco Packet Tracer Network | Build your own network, learn the PT file types | 5 videos, 1 Packet Tracer activity |

### 1.0.5 Overview video: what can you actually do with it?

This video is kind of a highlight reel. With Packet Tracer you can:

- Open an existing topology or file
- Rack mount and cable equipment like you're in a real network facility
- Design, plan, and test **IP addressing schemes**
- Configure wireless devices and wireless security
- Configure and program IoT devices like **sensors and actuators**
- Build and test smart home stuff (the example was a smart thermostat and a lawn sprinkler)
- Open a pre-built network, watch data flow, and look at detailed packet info
- Start with a blank screen and build a simple or complex topology

It's also an **assessment tool**. Classes that use it will have activities and skills assessments inside Packet Tracer.

And it runs on **Windows, Mac, and Linux**.

---

## 1.1 The Cisco Packet Tracer Interface

### 1.1.1 The user interface

Packet Tracer has three main menus. The way I understand them:

1. **Add devices** and connect them with cables or wireless
2. **Work with components**: select, delete, inspect, label, group
3. **Manage the network**: open a sample, save, change your profile or preferences

Now let's walk through the screen from top to bottom.

#### Top menu bar

- **File menu**: the usual New, Open, Save, Save As, plus **Open Samples**. Every new version of Packet Tracer comes with example devices and protocols, so Open Samples is a good place to poke around.
- **Options > Preferences**:
  - *Interface tab*: show device model labels and device name labels
  - *Font tab*: change app size, font, font size, and font color
  - *Miscellaneous*: the **auto file backup interval** (it's **off by default**, so turn it on if you don't want to lose work)

#### Toolbars

- **Main toolbar** (under the menu): the most-used stuff like Undo, Zoom In, Zoom Out
- **Secondary toolbar** (under that): select objects, delete objects, add drawing objects

#### Workspace toolbar (the blue bar at the top)

- Left side has two buttons: **Logical** and **Physical**
- The menu on the right side **changes depending on which mode you're in**

| View | What it shows |
|---|---|
| **Logical** | How devices connect and how data flows through the network |
| **Physical** | How the devices are laid out and cabled. Example: an equipment rack holding a router and a switch, plus a table with two PCs |

#### Bottom blue bar

- **Power cycle devices**: turns everything off and on
- **Fast forward**: speeds up network convergence so you don't have to wait for all the protocols to finish
- **Real-time vs. Simulation** (bottom right):
  - *Real-time* = the network runs normally as things happen
  - *Simulation* = **you control time**, add packets, and watch them move across the network

#### Bottom left and bottom right panels

- **Network components** (bottom left): where you pick routers, switches, PCs, other devices, and the cables to connect them
- **Scenario box** (bottom right): where you create packets that travel across devices so you can watch them

---

### 1.1.2 Deploying devices

Okay, this is where it gets fun. The video builds a small home network. Here's how the device area works:

- **Top row** = categories
- **Bottom row** = subcategories

#### Building the home network

| Device | Where I found it |
|---|---|
| Home router | **Wireless Devices** (not the "Routers" category, since those are more like corporate routers) |
| Gaming PC and laptop | **End Devices** |
| Webcam (front door camera) | The **Home** subcategory (it also has temperature sensors, garage doors, sprinklers, etc.) |

The point I want to remember: a home router has a **wireless part**, so it lives under Wireless Devices, not under regular routers.

#### Handy tricks

- **Zoom in/out** to see the topology better
- Press **R** to reset the zoom if things drift off screen
- **Delete tool**: click it, click a device, then confirm. If you change your mind, hit **Undo**.

#### Connecting devices

Down in the **Connections** category there's a **lightning bolt**. That's the **automatic connection** tool.

- It picks the **first available port** and the cable type it thinks is best
- If you know the cable type you need, you can choose it manually
- In the video: router to PC, and router to webcam

#### Making the laptop wireless (this part is cool)

The default laptop comes with a **wired card**, so you have to swap it:

1. Click the laptop to open its properties
2. Go to the **Physical** tab
3. **Turn the power off** (you have to do this before changing the module)
4. Drag the **wired card** out
5. Drag the **wireless interface** into that slot
6. **Turn the power back on**

Then the laptop **connects to the wireless router automatically**. That's the whole small home network done.

> This also made it click for me that Packet Tracer treats devices like real hardware. You can't swap a card while the thing is powered on, just like in real life.

---

### 1.1.3 GUI and CLI configuration

Each device has tabs for configuring it. **Which tabs you see depends on the device.**

| Tab | What it's for | Which devices |
|---|---|---|
| **Physical** | Power the device on/off, install modules (like a wireless NIC) | Most devices |
| **Config** | Basic setup using a GUI | Routers, switches |
| **CLI** | Command line access to the device (Cisco IOS) | Routers, switches |
| **Desktop** | IP config, wireless config, command prompt, web browser, other apps | End devices like PCs and laptops |
| **Services** | Server processes like HTTP, DHCP, DNS | Servers |

A bit more about each one:

#### Physical tab
Think of it like the back of the device where you can plug stuff in. Power on/off, install modules.

#### Config tab (the GUI)
- This is a **Packet Tracer-only** thing. It doesn't simulate how a real device works.
- It's great if you don't know the command line yet.
- As you change settings, the **Equivalent IOS Commands** window shows the CLI commands that do the same thing. For example, if you set the device name to `MyRouter` in the GUI, you'll see the matching IOS command pop up.
- You can also **save, load, erase, and export** device config files here.

> So the Config tab is like training wheels. You click, and it shows you what you'd have typed. That's a pretty good way to learn IOS commands.

#### CLI tab
- This is the real **command line** for a Cisco device. You need to know IOS to use it.
- It's where you practice real configuration, and it's a **necessary skill** for more advanced networking.
- Any commands you ran from the Config tab **also show up here**.

#### Desktop tab
For end devices (PCs, laptops). It gives you a desktop-style interface with IP config, wireless config, a command prompt, a web browser, and other apps.

#### Services tab
A **server** can do everything a normal host does, *plus* it gets this extra tab. This is where you turn on common server processes like **HTTP, DHCP, and DNS**.

*(There are other tabs on some devices, but they're beyond this course.)*

---

### 1.1.4 The Packet Tracer Tutored Activity (PTTA)

A **PTTA** is a guided activity, like having a teacher looking over your shoulder. Every PTTA has hints, and **you choose how many you get**.

#### Hint levels

| Level | What you get |
|---|---|
| **No hints** | You're on your own (the challenge mode) |
| **Critical hints** | Only the most essential hints |
| **More hints** | A level between critical and all |
| **All hints** | Every hint the activity has |

Some details I noticed:

- Hints **don't show up right away**. You get a moment to think first.
- You can **change the hint level anytime** during the activity.
- **Not all Packet Tracer activities** have this hint system. Some other courses have PTTAs, but not every activity is one.

#### How the activity works

- Read the **background and scenario** first. They give you important details about the task.
- Tasks have **green check marks** when you finish them.
- The **completion percentage** goes up as you work.
- The **Next button** only shows up after you finish all the tasks in that part. You can go **Back** anytime though.
- **FRQs (free response questions)** can show up at the beginning (like predicting what will happen) or at the end (reflecting on what you learned). Don't forget to **submit** them.
- At the end there's a **summary screen** that recaps the tasks you did and your FRQ answers.
- You can **dock and undock** the panels and move them around.
- You can **right-click to zoom in** on text.
- There's a **reset button** if you want to start over.
- You can hover over **cables** to see what type they are.

#### This PTTA specifically

It goes beyond just exploring. You'll:

- Connect devices to networking devices
- **Install a backup router**
- **Configure a host name**

---

### 1.1.5 Inspecting devices in physical mode

This was a mini tutorial for the PTTA, and it's actually really practical.

In **Physical mode**, you can **right-click a device** and pick **Inspect Front**. That gives you a bigger view where you can read the **port numbers and labels**. Some devices let you look at the **back** too.

- On the switch, the back is where you'd find the **console port**.
- You can use Inspect **while you're cabling**: pick a cable, right-click the device, inspect it, then find the port you need.

Example from the video:

1. Pick the **straight-through cable**
2. Right-click the router, **Inspect Front**, zoom in
3. Hover over the port to see its name (here it was **FastEthernet 0/0**)
4. Connect that end, then do the same on the switch and choose port **0/24**

> Why this matters: when you're cabling for real, you can't just guess which port. Inspect lets you check before you plug in.

---

### 1.1.6 Activity: Logical and Physical Mode Exploration

This is the hands-on part of the module. It's a **PTTA** with the hint system and a built-in tutorial.

- It's recommended to **watch the PTTA video first** (1.1.4)
- The tutorial videos from 1.1.5 are there if you need them
- The file can take a while to load after you open it, so be patient

---

## Key terms

| Term | What it means (my words) |
|---|---|
| **Cisco Packet Tracer** | A free network simulator for practicing networking, IoT, and cybersecurity |
| **Logical view** | The diagram view: what's connected to what and how data flows |
| **Physical view** | The "real world" view: racks, cables, ports |
| **Real-time mode** | The network runs normally |
| **Simulation mode** | You control time and watch packets move |
| **Topology** | The layout of the network |
| **Power cycle** | Turn all devices off and back on |
| **Fast forward** | Skip ahead so the network converges quickly |
| **Convergence** | When network protocols finish their processes and the network settles |
| **Scenario box** | Where you create packets to send across the network |
| **Automatic connection** | The lightning bolt tool that picks a cable and port for you |
| **NIC** | Network interface card (the part that connects a device to the network) |
| **GUI** | Graphical user interface (the Config tab is one) |
| **CLI** | Command line interface (where you type commands) |
| **IOS** | Cisco Internetwork Operating System, the software on Cisco devices |
| **Equivalent IOS Commands** | The window in the Config tab that shows the CLI version of what you clicked |
| **IoT** | Internet of Things (smart devices like sensors, cameras, thermostats) |
| **PTTA** | Packet Tracer Tutored Activity, a guided activity with hints |
| **FRQ** | Free response question |
| **HTTP / DHCP / DNS** | Common server services you can set up in the Services tab |

---

## Quick summary

- Packet Tracer is a **free simulator** that runs on Windows, Mac, and Linux. You get hands-on practice with no hardware.
- It's a great learning tool, but it **doesn't replace** real equipment.
- The screen has **menus, toolbars, a workspace, a device area at the bottom left, and a scenario box at the bottom right**.
- You can switch between **logical and physical** views, and between **real-time and simulation** modes.
- To build a network: **pick a device category and subcategory, drag the device in, then connect with cables** (the lightning bolt is the easy option).
- You can swap modules on a device (like wired to wireless), but you have to **power it off first**.
- Device tabs: **Physical, Config, CLI, Desktop, Services**. What you see depends on the device.
- The **Config tab** shows you the CLI commands as you click, which is a nice way to learn IOS.
- **PTTAs** are guided activities where you pick how many hints you get.
- In physical mode, **Inspect Front** helps you find the right ports while cabling.

Next up is Module 2, where I build my own network and learn about the file types.
