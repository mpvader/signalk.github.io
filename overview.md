---
title: Overview
layout: rsidebar
overview: active
sidebar: overview-sb.html
description:
  "The Signal K data standard is the next generation solution for marine data exchange. It not only allows
  for communication between instruments and sensors on board a single vessel, but also to allow for sharing of data
  between multiple boats, aids to navigation, bridges, marinas and more."
---

## [Introduction](#) <a class="anchor" id="introduction"></a>
The Signal K data standard is an open marine data standard. It is a modern data format for marine use, suitable for WiFi,
cellphones, tablets and the internet. It is built on standard web technologies including JSON, WebSockets and HTTP.

It not only allows for communication between instruments and sensors on board a single vessel, but also allows sharing
of data between multiple boats, aids to navigation, bridges, marinas and other land-based resources. It is designed
to be easily used by Web and Mobile applications and to connect boats to the Internet of Things.

With all above, the Signal K data standard complements the other two popular marine data protocols, NMEA 0183 and NMEA 2000.

## [Background](#) <a class="anchor" id="background"></a>
To explain its place and need, lets first have look at the other marine data protocols. Some are proprietary such
as Raymarine's SeaTalk interface, but the two most popular were both developed by the
[National Marine Electronics Association](http://www.nmea.org/) (NMEA):

### NMEA 0183
Based on the RS422 serial interface, NMEA 0183 is now over 35 years old but has aged remarkably well and is still in use on many
leisure and commercial vessels. As you can see from the diagram, it works by having lots of pairs of wires going between
equipment, in fact two pairs of wires if you want bi-directional communication. It is primarily a one to one method of
communication although you can have 3 or 4 “listeners” connected to one “talker”.

<figure>
  <img src="/images/diagrams/Typical_NMEA0183_Diagram.png" width="400">
  <figcaption>Typical NMEA 0183 Implementation</figcaption>
</figure>

### NMEA 2000
Based on the same CAN Bus technology used in cars, NMEA 2000 is now over 15 years old and
most new boats have an NMEA 2000 network. It can handle a wide spread of information sources from engines to stereos.
It is faster than NMEA0183, but more difficult to interface to.

As you can see from the diagram, you have a network “back bone” with “spurs” or drop cables that take power and data to
the equipment. Every device on the network can talk or listen to any other device or broadcast to all devices.

<figure>
  <img src="/images/diagrams/Typical_NMEA2000_Diagram.png" width="400">
  <figcaption>Typical NMEA 2000 Implementation</figcaption>
</figure>

These existing standards serve their purpose to connect marine sensors and display units. But when it comes to development
of modern mobile and web apps, as well as cloud services, they are not suitable.

Here are their two main limitations:

### Technical limitations
Both standards are fundamentally local area networks designed for limited deployments.
NMEA 0183 is normally limited to 4800 baud (or 34,800bps in high speed mode) and one transmitting device. NMEA 2000
works at a significantly higher bit-rate (250kbps) and allows multiple devices to transmit on one shared bus, but it is
limited to 50 devices on a bus.

By their nature, both protocols are difficult to connect to WiFi, phones, tablets and internet.

### Legal limitations
Although all NMEA standards are published and available for use by any developer and therefore are technically “open
standards”, anyone wishing to use them must not only pay for the standards but also sign a license agreement which
restricts how they can be used and in the case of NMEA 2000, a non-disclosure agreement. Hardware manufacturers are
also obliged to have their equipment ‘certified’ before they can sell it, an expensive process for small companies. In
essence, this prevents the release of an open source application developed using these standards and presents a high
cost of entry for smaller developers.

<figure>
  <img src="/images/diagrams/Technical+Legal_Barriers.png" width="400">
  <figcaption>Technical and Legal Barriers</figcaption>
</figure>

## [The Internet of Things](#) <a class="anchor" id="IoT"></a>
In a world where even your home thermostat can be connected to the Internet, and the number of worldwide
internet connected devices is projected to exceed 70 billion by 2025, there is no more need for your boat
to be an island to itself.

After all, there are lots of other boats out there, and lots of other sources of information, all of which could be of
interest and benefit to you. In the modern connected world, shouldn’t you be able to access that information from your
boat where ever you are and on whatever device you want?

To move forward we need to think in a connected way, a way fundamentally different from NMEA protocols. Sun
Microsystems famously coined the phrase _The network is the computer_, and Signal K reflects that global peer-to-peer
concept.

The ability to share information with other boats, and via the Internet, has the potential to revolutionise the way
nautical data is treated both afloat and ashore. Applications will be limited only by developers' imagination, but
could include:

* Innovative Apps: If a standard is free to use, cost of entry is lower. This is encouraging new software and hardware
  developers to compete on providing new solutions.
* Crowd-Sourced data: Aircraft already share information on clear-air turbulence, similarly, boats could share
  real-time information on weather with each other.
* Boat Monitoring: It becomes simple to monitor the health of your boat, onboard or afloat, wherever you are in the
  world.
* Fleet Management: Flotilla companies could monitor their fleet to get advance notice of problems occurring.
* Marinas: It should be possible to book marina berths direct from your Chartplotter. By sharing your information with
  the Marina, they get real-time information on your arrival.
* Race Management: The monitoring and management of Race Fleets, currently the province of major round-the-world
  events, can be brought to club level.
* Pilotage & Cruising Information: Real time information from established organisations can be beamed directly to your
  boat to enhance your onboard tools.

## [Security](#) <a class="anchor" id="security"></a>
We are constantly hearing horror stories of the latest security flaw being exploited by hackers and it is extremely
important that any modern data standard, that allows your information to be transferred across the Internet, has
security designed in to its heart.

The Internet has widely adopted and proven security standards, so there was no need to reinvent the wheel. Signal K
supports secure, encrypted HTTPS and WSS connections, with the same authorisation and authentication techniques that
you are using everyday on Facebook, Paypal, Googlemail, online banking, etc.

As a user, having fun sailing miles out at sea, it is easy to forget about security, but the in-built security of
Signal K coupled with your own good security practices like strong passwords and WPA2 encryption on your wireless
router, will keep your data safe.

## [Signal K](#) <a class="anchor" id="signalk"></a>
The Signal K data standard is based on  modern techniques, creating a marine data standard for the 21st Century. It is:

* Open. Signal K is managed by a community of boaters, and developers are able to propose
  improvements to the standard.
* Free. All of the code is published under Open Source licenses for anyone to use free of charge.
* Modern. It uses widely available, Open Source technologies.
* Extensible. It can mature with new requirements as they emerge.
* Flexible. Signal K is not tied to specific hardware
* Respectful. It is designed to interface to existing equipment and protocols.
* Proven. Several commercial vendors have adopted the Signal K data standard; and thousands of boaters are using it daily.

It is easy to get started with Signal K. With a Google Group for users, Slack Channels for developers, lots of online
information, low cost hardware and many free or low costs apps and solutions, you can quickly build a system and start
benefiting from the tens of thousands of man-hours of community development that has gone in to Signal K.

Signal K works by having a small black box — a Signal K Server — on board your boat. This can interface to existing
NMEA networks onboard as well as databases, other Signal K data streams, and potentially land-based and cloud-based
resources. The server can also hold static items like charts, routes and notes. It can also hold and act as a
web-server for browser-based Apps.

The Signal K server is available as a ready-to-fit commercial product (such as the
[Digital Yacht iKommunicate](http://ikommunicate.com)), or you can download the software for free and run it yourself.
The software runs on a range of single board computers; Raspberry Pi, Beagle Board, etc. as well as any normal PC running Linux, Windows and MacOS, see the
[Install page]({{site.path}}/installation.html) for details.

One of the latest developments on the Signal K Node server, is the support for
[Plugins](https://en.wikipedia.org/wiki/Plug-in_(computing)). A plugin is an extra software component (program)
that adds a specific feature to an existing computer program, in this case the Node Server. There are an increasing
number of plugins being released and they are easily selected and installed on the “Signal K Plugin Store”.

<figure>
  <img src="/images/diagrams/pluginstore.png" width="400">
  <figcaption>List of Available “Plugins”</figcaption>
</figure>

Please [click here](https://www.npmjs.com/search?q=signalk-node-server-plugin) for a list of all the latest Signal K plugins or [click here](https://www.npmjs.com/search?q=signalk-webapp) for a list of the latest Signal K Web Apps that can be installed via NPM. Additional Signal K Apps and Solutions can be found on the [Applications and Solutions
page]({{site.path}}/solutions.html).

Signal K is an on-going, collaborative effort between a global network of volunteers and interested hardware
manufacturers and software vendors in the marine industry. We encourage you to get in touch via the [mailing
list](https://groups.google.com/forum/#!forum/SignalK) or group chat in our [Slack
channel](http://slack-invite.SignalK.org/). Suggestions and requests via [Github](http://github.com/SignalK) are also
welcome.
