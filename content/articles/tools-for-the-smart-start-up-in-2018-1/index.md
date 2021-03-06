---
title: Tools for the Smart Start-up in 2018 (I)
publishdate: 2018-08-02
lastmod: 2019-06-28
tags:
- Likes
- Technology
summary: If you start a project on a small budget today in 2018, there is no need to do without state-of-the-art IT infrastructure for your team. Let me give you some ideas.
images:
- https://res.cloudinary.com/ypertex/image/upload/c_fill,dpr_auto,f_auto,g_auto,h_630,q_auto,w_1200/7b95a9b0-0f54-44f9-8af3-dd6820d3051d
aliases:
- /articles/tools-for-the-smart-start-up-1/
---

> We are not a start-up, so we don’t have the luxury of experimenting endlessly. How do you work within the constraints of our limited budget?
>
> {{<attribution>}}Question from an interview at the [Swiss Financial Market Supervisory Authority FINMA](https://www.finma.ch/en/){{</attribution>}}

This was a question I was asked in an interview when I applied for a new job after [my start-up experience](https://blog.ypertex.com/articles/start-up-success-factors-trust-and-loyalty/).

Of course, we all read and hear about the astronomical valuations of the start-ups i.e. in Silicon Valley and the amounts of money they can pour into their <abbr title="Research & Development">R&D</abbr> and innovation labs. This, however, distorts our perception of reality: The fact is that the vast majority of business ventures start with very few resources at their disposal.

{{<figure src="7b95a9b0-0f54-44f9-8af3-dd6820d3051d" cite="[Evan Kirby](https://unsplash.com/photos/jl8x6XpE8Y4)">}}As a small start-up you can still cast a long shadow{{</figure>}}

So my response was: “Sure, we had a lot of freedom to experiment. But like for most start-ups in their initial phase, our budget was extremely tight, too, and we had to be *extra* smart about how we spent every single Swiss franc. I will employ the same approach in this role as well!”

Now, four years later, I observe that being smart in the above sense has become *so* much easier with the range of high quality, low-cost software available today. It now is possible with little to no extra money to do things that previously were achievable only in a very complex and very cost-intensive manner.

So how do you get the most bang for the buck? Let me highlight a few services and applications (and how to combine them) that are **less known** but deliver **outstanding value**—especially for start-ups on a small budget. This article is the first in a series of two and is written from an IT infrastructure perspective. The second article focuses on the application level.

For this series of articles, let’s assume a start-up with a team of eight people.

---

{{<note>}}
##### <i class="las la-balance-scale-left"></i> Disclaimer

I am in no way affiliated with any of the vendors and providers mentioned below. My recommendations stem from personal and professional experience with these tools.
{{</note>}}

---

## Hardware

To start, your team probably needs some hardware to communicate and collaborate. Outfitting everybody with devices can quickly exceed your budget, though. Imagine paying upfront a total of $4,000 for eight mid-range laptops, before your team even worked a single minute on the project…

{{<figure src="c978c945-4baf-480d-8e91-c07731f2e1e9" cite="[PCWorld](https://www.pcworld.com/article/3017182/hardware/usb-c-charging-universal-or-bust-we-plug-in-every-device-we-have-to-chase-the-dream.html)">}}A stack of laptops{{</figure>}}

So, here are a few ideas on how to address this challenge:

### BYOD: Bring Your Own Device

This is probably a no-brainer, but still: Just have your team use their privately owned devices to work on your project. These are already set up and operational, so you and your teammates can hit the ground running. This concept of <abbr="Bring Your Own Device">BYOD</abbr> will carry you a long way.

At some point though, your team probably will run into more and more issues due to the different setups of their hardware and operating systems: Apple users might have problems to work on files that are used by users with Microsoft devices–while the Windows people might not be able to execute applications that run just fine on macOS systems. The friction caused by BYOD starts to show.

One way to deal with this is to install a hypervisor on each device and run a virtual machine on top of it. This gives you the ability to align the virtual working environment of all team members and eliminate interoperability issues. For example: With [VirtualBox](https://www.virtualbox.org/) as hypervisor and a Linux distribution like [Ubuntu](https://www.ubuntu.com/) as the desktop operating system for the virtual machines, you can set up a cost-free and homogeneous virtual workplace for your entire team. (In cases where Linux is no option and you need a Microsoft operating system: There are ways to buy genuine but cheap software [as described below](#microsoft-software-licensing). Virtualizing Apple operating systems, unfortunately, is no practical option due to legal and technical impediments.)

Then there are cases where installing a hypervisor like VirtualBox on your team’s hardware is impossible or impractical. However, there exist solutions for such a scenario, they are categorized as <abbr title="Virtual Desktop Infrastructure">VDI</abbr>: virtual desktops in the cloud.

## Hardware as a Service

There are only a few cloud providers of virtual desktops (compared to the number of cloud providers who offer virtual servers), and most of them target rather large enterprises than start-ups.

{{<figure src="2441553b-3402-4e29-a505-1b043aa53241" cite="[Patrick Fore](https://unsplash.com/photos/0gkw_9fy0eQ)">}}The contrary of a virtual desktop: a mechanical typewriter{{</figure>}}

However, there is one provider that I can recommend:

### VDI Provider [Paperspace](https://www.paperspace.com/)

If paid by the hour, the pricing of a reasonably sized Paperspace virtual desktop today is roughly somewhere between $16 and $22 per month based on a 40-hours-week. Given the Windows 10 license already included, this appears to be a fair offer in my opinion.

The fact that Paperspace desktops can simply be used *via browser* without any additional software to install, makes this option especially valuable if you don’t want to or can’t touch your team members’ devices.

{{<figure src="b5ae993f-c2d4-46f2-9dc7-9043e3f72fa0" transformation="full">}} Screenshot of the Paperspace VDI website, August 2018{{</figure>}}

I have used Paperspace productively myself a few months ago and generally can recommend their service. The only issue I encountered was a weird keyboard mapping concerning the German Umlauts (äöü).

But what if $16 per month per team member is already too high of a price? Imagine a team of 8 people; they would have to pay roughly $128/month to use Paperspace—or more if they burn the midnight oil and exceed the 40 hours per week in that calculation. What if team members forget to turn off their virtual desktops after work? We certainly can be even smarter and bring this cost down further. What about instead running our own VDI on a server that we rent?

### Dedicated Server Providers [Online.net](https://www.online.net/en/), [Hetzner](https://www.hetzner.com/), and [Servdiscount](https://servdiscount.com/)

Several providers in Europe offer server hardware as a service at very low prices: the French provider Online.net (with data centers in France and the Netherlands) as well as the German providers Hetzner (with data centers in Germany and Finland) and Servdiscount (with a data center in Germany). The low-end divisions [Kimsufi](https://www.kimsufi.com/us/en/) and [So you Start](https://www.soyoustart.com/us/) of [OVH](https://www.ovh.com/world/) are hands down no match for Online.net, Hetzner, and Servdiscount.

{{<figure src="af86d5f7-0a25-4e58-aab9-e3496ef78000" transformation="full">}}Screenshot of the Hetzner Dedicated Server website, August 2018{{</figure>}}

Overall, Hetzner currently has better deals in my opinion. The new *vSwitch* feature, available for all their servers with no additional cost, allows to securely interconnect servers within Hetzner’s data centers. This adds a lot of value if you need more than one server (for clustering for example).

{{<figure src="aba0d8c0-c11a-4982-8d58-649e6dca239f" transformation="full">}}Screenshot of the Online.net Dedicated Server website, August 2018{{</figure>}}

One feature that I especially like at Online.net is the availability of a <abbr title="Keyboard Video Mouse">KVM</abbr> console *within seconds*. Such a console allows accessing the server’s screen even during boot time or after accidentally having locked out oneself (by i.e. messing with the servers connectivity settings). In the case of Hetzner, users first have to raise a support ticket, never knowing upfront how long it might take to get the requested KVM console. (The Hetzner support usually acts fast, but gets squarely beaten by the automated process at Online.net.)

On the other hand, Hetzner rarely seems to run out of stock while Online.net appears to constantly being sold out. It might take months for Online.net to restock their portfolio.

I have intensively used Online.net and Hetzner services in professional projects and for my private lab and can recommend them both. On the rare occasions that I had issues, both support teams act fast and in a very friendly manner.

---

{{<note class="alert-secondary">}}
##### <i class="las la-sync"></i> Edited {{<date>}}2019-06-28{{</date>}}

Let me add [Servdiscount](https://servdiscount.com/) to this list of providers. I've only used their services for a few weeks and already can tell that they deliver great value for competitive prices.

As an example: For roughly $26, they provided me an 8-core processor, 24GB RAM (instead of the promoted 16), 265GB SSD (instead of the promoted 128), 1TB HDD, unmetered 1Gbps connectivity, *and a dedicated KVM*. Customer support is competent, prompt and friendly.

If you can live with the missing disk redundancy options in most of their low-cost offers, it's worth a look!
{{</note>}}

---

Back to the example of our team of eight persons: A reasonably sized mid-range server from Hetzner costs around $60 per month. It comes with hardware resources that would *easily* accommodate virtual desktops for eight people—or more!

Compared to the $128 per month for eight Paperspace virtual desktops that run only about 8 hours per day (compared to the 24 hours that the Hetzner server is available), this looks like a steal.

## Software

Hang on! A server from Hetzner does not include any licenses for virtual desktops like Windows 10. How is this supposed to help?

Great question, but there is a smart solution for that.

### Microsoft Software Licensing

On a Subreddit called [Microsoft Softwareswap](https://www.reddit.com/r/microsoftsoftwareswap/), people sell Microsoft software licenses that they own for low prices. At first glance, this marketplace seems a bit phony—but from what I can tell and have researched, these are legitimate, genuine Microsoft software licenses. The handful that I bought there in the past all activated the software perfectly fine without any problem whatsoever.

{{<figure src="2ccb3d88-a2e7-42cc-b405-9f9ceaf101df" transformation="full" />}}

One license is particularly interesting: the **Windows Server Datacenter edition**. The current version 2016, for example, sells as low as $40 on Reddit. Compared to the price that Microsoft asks, it’s unbelievably cheap: Microsoft sells the Datacenter 2016 license for currently *$6,155*. Read that again. Yes, you pay only *0.65%* of the list price if you buy such a license via the Subreddit mentioned above instead of buying it directly from Microsoft.

> Ever wanted to **save 99.35%** on something? Here you go: A genuine Windows Server Datacenter edition license for $40 instead of $6,155.

This Datacenter edition is so interesting due to one feature: Any Windows server that runs as a Hyper-V virtual machine inside of such a Windows Server Datacenter can be activated *at no additional cost*. Read that again, too. You only pay a one-time investment as low as $40 to obtain a single Windows Server license which then enables you to run *as many Windows Server instances* on top of it as you possibly can.

---

{{<note>}}
##### <i class="las la-lightbulb"></i> Tip

If you want to install your $40 license on a Hetzner server, you will have to ask for the above-mentioned KVM. This allows you to mount your <abbr title="ISO 9660 file system disk image">ISO</abbr> and install Windows Server from there. I recommend putting the several GB large ISO on a Hetzner Storagebox beforehand to keep your source ISO as close as possible to the server. Otherwise, the installation might take many hours.
{{</note>}}

---

To come back to our hypothetical team of eight people: Rent a hardware server from Hetzner for $60 per month; then install Windows Server Datacenter on that hardware server and activate it with the $40 license from Reddit. Then create as many Windows Servers as virtual Hyper-V machines on your hardware server and activate them with the [official <abbr title="Automatic Virtual Machine Activation">AVMA</abbr> keys](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn303421(v=ws.11)) from Microsoft.

With this setup, you can offer every team member a dedicated virtual client in a homogeneous environment. The financial impact of your team growing from eight to i.e. ten is zero: Just create new virtual machines. Your hardware can handle it and you already have the software licenses built-in. Your team connects via <abbr title="Remote Desktop Protocol">RDP</abbr> and can work on their virtual Windows desktops in the cloud. All of this for the fraction of the price that VDI providers like Paperspace ask. And of course, if your start-up implodes already after two months, you have only invested like $250 (considering the one-off fee to provision the server) instead of $4000 that you would have spent to buy every team member a mid-sized Windows laptop right from the start. That’s smart.

One feature, however, is still missing: the ability to connect to the virtual desktops *via browser*. Maybe not all devices in your team of eight people have an RDP client installed—but certainly, all already have a browser ready to be used. This kind of “zero-touch BYOD” is preferable, especially in the beginnings of your start-up. (Because as soon as you “touch” and modify your teammates’ devices, you assume some sort of responsibility for them.)

Fortunately, there exists an excellent open-source software that enables this feature: Guacamole. And as an avid lover of Mexico and Mexican food, I love this software and its name even more!

### Web Gateway [Apache Guacamole](https://guacamole.apache.org/)

The developers call Guacamole a “clientless remote desktop gateway”. This means that you can access the gateway simply via a web browser, without any specific client. This gateway then connects to the desktops and lets users interact with them through their browsers.

{{<figure src="d8c0ae14-99c6-4a14-ad5b-1e62bcbf1759" cite="[Juan Manuel Giraldo Grisales](https://unsplash.com/photos/K7bd0WoYfoo)">}}Did I mention that I love Guacamole—both the food and the software?{{</figure>}}

The installation of Guacamole is a bit of a head-scratcher, though. Following the official installation guide involves many manual steps. Fortunately, some smart people found [ways to simplify the process](https://github.com/BrowncoatShadow/compose-guacamole) with the help of [Docker](https://www.docker.com/). So, all you need is a Linux virtual machine somewhere (i.e. on the server from Hetzner that runs all your virtual desktops), install Docker and [Docker Compose](https://docs.docker.com/compose/) and then run the following three commands:

{{<highlight shell>}}
git clone git@github.com:BrowncoatShadow/compose-guacamole.git
cd docker-compose-guacamole
sudo docker-compose up -d
{{</highlight>}}

Now point your browser to your Docker host that runs the Guacamole container, log in and add the users and virtual desktops. That’s it. You now have your browser-accessible virtual desktop infrastructure up and running at extremely low cost.

If you are interested in encrypting the traffic between your users and this gateway, however—and you should—, you might want to secure the gateway behind an SSL-capable proxy. Like I composed Guacamole with Træfik in my [Wapps repository](https://github.com/MichaelSchmidle/wapps).

Talking about security: We still need to address a few concerns. Read on!

### Firewall [OPNsense](https://opnsense.org/)

Having lots of (physical or virtual) Windows servers and desktops running somewhere in the cloud without any particular security measures in place is a very bad idea. Fortunately, there are a few excellent open source solutions available to implement a firewall and secure the small network of Windows desktops in the cloud. Simply create another virtual machine on your Windows Server Datacenter host and install the firewall on that virtual machine, then connect all other virtual machines to that firewall <abbr title="Virtual Machine">VM</abbr> instead of the open Internet. 

My favorite for quite some time was the Sophos XG <abbr title="Unified Threat Management">UTM</abbr> firewall that is available as [Free Home Use XG Firewall](https://www.sophos.com/en-us/products/free-tools/sophos-xg-firewall-home-edition.aspx) at zero cost.

However, I recently gave the open-source firewall OPNsense a try—and never looked back. It has the same feature set as the Sophos XG but with a much, much smaller footprint in terms of hardware resources (especially <abbr title="Random Access Memory">RAM</abbr>, hovering over *extremely economical* 160MB in my current cloud lab setup). It also installs much faster.

{{<figure src="1ad0fea9-b819-43fe-9f60-633fc6493bf6" transformation="full">}}Screenshot of the OPNsense dashboard, March 2016{{</figure>}}

Additionally, OPNsense even has one crucial feature that most other firewalls lack: support for ZeroTier. Which brings me to my next point.

## Software as a Service

I love <abbr title="Software as a Service">SaaS</abbr> providers who offer a free entry-level to their service, letting users come to appreciate the service so much that at some point they upgrade to a paid service level. Let me introduce two such services that can help a smart start-up better manage their IT devices.

### Virtual Private Network [ZeroTier](https://zerotier.com/)

The first service I’d like to mention is called ZeroTier. It works like a <abbr title="Virtual Private Network">VPN</abbr> in the sense that it allows to interconnect devices in a private network wherever they are: at home, in the data center, somewhere in the cloud or roaming abroad. All at once, all encrypted.

{{<figure src="72197694-a570-4781-9625-1639b4f03414" cite="[Ishan @seefromthesky](https://unsplash.com/photos/N2HtDFA-AgM)">}}Interconnecting things can be complex sometimes—like these roads in a Malaysian interchange{{</figure>}}

What separates ZeroTier from traditional VPN technology like [OpenVPN](https://openvpn.net/) is that it does not require any user intervention. Users don’t have to dial in—their devices simply interconnect as soon as they get Internet connectivity. It works a bit like [Microsoft DirectAccess](https://docs.microsoft.com/en-us/windows-server/remote/remote-access/directaccess/directaccess) with the difference that ZeroTier is also available for Apple (macOS and iOS), Linux, Android, Microsoft, and even some <abbr title="Network Attached Storage">NAS</abbr> devices. With ZeroTier you can offer your team to directly but securely connect to their virtual desktops via RDP.

Combined with the ZeroTier capable OPNsense firewall mentioned above, it is possible to significantly reduce the attack surface of your virtual desktops in the cloud while still conserving ease of access and keeping the complexity of the setup at a low level. I strongly recommend this service over other VPNs.

The free ZeroTier service is limited to 100 devices. For our team of eight persons, this should be more than sufficient. Speaking about persons: Let’s also manage your team’s user accounts.

### User Directory [JumpCloud](https://jumpcloud.com/)

We all know the pain of having to manage a myriad of our logins and user accounts. One way to deal with this problem is by relying on a password manager—as I also recommend doing in the second article of this series.

The second approach is called <abbr title="Single-Sign-On">SSO</abbr>. It involves a central store for your team’s credentials where each user is represented with a single account. Applications and services then connect to this central user directory to authenticate users whenever they try to log in. The advantage is that users only have to remember a single sign-on and that there is only one place that stores this sensitive information.

JumpCloud is such a service, offering a free entry-level plan for up to ten users. The neat thing about it is that you can use it to even manage the logins for large parts of the <abbr title="Do It Yourself">DIY</abbr> mentioned above: native Windows and Linux logins, Apache Guacamole, and OPNsense logins. Simply define which user is allowed to access which device, and with what kind of privileges (root/administrator or normal user). This also means that your IT administrator can revoke access to any or all devices by a single click if need be. I can recommend the service as it improves both overall security and user comfort.

{{<figure src="c6541768-4b41-4bae-967c-3f121b50a695">}}Last time [I wrote about JumpCloud](https://blog.ypertex.com/articles/jumpcloud-curl-error-22/), they sent me this shirt with a handwritten note. So you know they must be cool!{{</figure>}}

## Conclusion

I hope this overview gave you some insight into how to leverage services and software capabilities out there to set up a smart and powerful team infrastructure at a very low cost. If you have any further suggestions, please feel free to [reach out](https://twitter.com/MichaelSchmidle) and share your ideas.

The [second article in this series](/articles/tools-for-the-smart-start-up-in-2018-2/) focuses on the application level (compared to the emphasis on infrastructure in this blog post). It lists applications and services that deliver high quality at low prices in the area of design, web publishing, knowledge management, password management, and more. Stay tuned! 
