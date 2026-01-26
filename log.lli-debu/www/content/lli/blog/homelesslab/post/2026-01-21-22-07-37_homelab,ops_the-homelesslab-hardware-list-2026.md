<!--t The Home(less)lab Hardware List - 2026 t-->
<!--d My homelab stuff. d-->
<!--tag Homelab,Ops tag-->

<!--toc-->

Starting a new personal site (again) because my infrastructure management and self-hosting skills have finally reached a point where I’m comfortable managing my own stack 24/7. I’ve created at least five sites for myself in the past and abandoned them all, so I’m hoping this one can last.

This first post is just a list of the hardware in my homelab. I named it Home(less)lab simply because my gear (and my life) doesn't have a permanent home yet.

##The Core Nodes (The Vegetables)
I’ve gone with a vegetable-themed naming convention for the servers that keep everything running. It’s inspired by a friend of mine who uses the name "Zucchini" for a chip he designed for his dissertation.

### Garlic (ZimaBoard 832)
![enter image description here](https://log.lli-debu.top/content/images/20260125125504-Garlic.jpeg)
```
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀   debu@Garlic
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠛⠉⣁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀   --------
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣿⣿⣿⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀   OS: Debian GNU/Linux 12 (bookworm) x86_64
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣸⣿⣿⣿⣿⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀   Kernel: 6.1.0-42-amd64
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣴⣿⣿⣿⣿⣿⣧⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀   Uptime: 1 day, 7 hours, 22 mins
⠀⠀⠀⠀⠀⠀⠀⠀⣀⣴⣿⣿⣿⣿⣿⣿⣿⣿⣧⡹⣦⣄⡀⠀⠀⠀⠀⠀⠀⠀   Packages: 1946 (dpkg)
⠀⠀⠀⠀⠀⢀⣴⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣦⣄⠀⠀⠀⠀⠀   Shell: bash 5.2.15
⠀⠀⠀⢠⣾⣿⣿⣿⣿⡿⢫⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣝⠿⣿⣷⡄⠀⠀⠀   Terminal: /dev/pts/0
⠀⠀⢰⣿⣿⣿⣿⣿⠟⣱⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⣌⠻⣿⡄⠀⠀   CPU: Intel Celeron J3455 (4) @ 2.300GHz
⠀⠀⠸⣿⣿⣿⡿⠃⣼⣿⣿⣿⡿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣦⠈⠁⠀⠀   GPU: Intel HD Graphics 500
⠀⠀⠀⠹⣿⣿⠃⣸⣿⣿⣿⣿⠁⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣇⠀⠀⠀   Memory: 2551MiB / 7785MiB
⠀⠀⠀⠀⠈⠙⠀⢿⣿⣿⣿⣿⡄⠹⣿⣿⣿⣿⡟⢻⣿⣿⣿⣿⣿⣿⡏⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠘⢿⣿⣿⣿⣿⠄⠙⠿⣿⣿⣿⣦⠙⠛⠿⠿⠿⠋⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣤⢠⣶⢀⣶⠀⡈⢉⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠁⠈⠋⠀⠛⠀⠋⠈⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
```
This is a ZimaBoard 832 I bought back in 2023. I had to exchange the first unit because it was unstable and freezes randomly, but the replacement has been great. I keep it running 24/7 and has never had any issue.

It is a solid x86 micro-server with extremely low power consumption (under 5W at idle and roughly 15W under load). Most importantly, it uses passive cooling and is **fanless**. This is quite important because I sleep in the same room as my hardware, so fan noise is a big deal.

While the CPU isn't the most powerful, it easily handles several lightweight services. I use it as as my primary web host, IoT hub, micro-NAS, network gateway, DNS server, and jump host.


### Onion (Naked 12700k)
![enter image description here](https://log.lli-debu.top/content/images/20260123230055-Onion.jpeg)
```
              ▓▓██             debu@Onion
              ▓▓██             ---------------
            ▓▓██               OS: Debian GNU/Linux 12 (bookworm) x86_64
      ▓▓▓▓  ▓▓██▓▓▓▓           Host: MS-7D30 2.0
    ▓▓████▓▓▓▓▓▓████▓▓         Kernel: 6.1.0-42-amd64
    ██    ██▓▓██    ██         Uptime: 1 day, 6 hours, 50 mins
          ██▓▓██               Packages: 2038 (dpkg)
          ██░░▓▓██             Shell: bash 5.2.15
        ██▓▓░░░░▓▓██           Resolution: 1920x1080
      ██░░░░░░░░░░░░██         Terminal: /dev/pts/0
    ██▒▒░░░░░░░░░░░░▒▒██       CPU: 12th Gen Intel i7-12700K (20) @ 3.600GHz
  ██░░░░░░░░░░░░░░░░░░░░██     GPU: Intel AlderLake-S GT1
██▒▒░░░░░░░░░░░░░░░░░░░░▒▒██   Memory: 11184MiB / 31886MiB
██░░░░░░████░░░░████░░░░░░██
██░░░░░░████░░░░████░░░░░░██
██░░░░░░░░░░░░░░░░░░░░░░░░██
██▒▒░░░░░░░░░░░░░░░░░░░░▒▒██
  ██▒▒░░░░░░░░░░░░░░░░▒▒██
    ████████████████████
```
This one is basically a naked desktop—mostly just parts salvaged from my retired main rig. I had to retire it because its unreliable. It’s fine for gaming on Windows, but the second I put it under load in Linux, it just freezes.

My guess is that it's either a problem with the Intel Gen 12 processors or the early DDR5 RAM. Our lab has another Alienware PC that runs on a 12900KF, and it suffers from the exact same issue. My solution is to disable Turbo Boost on the Intel CPUs and XMP for the RAM—basically just running them on their base frequency.

I only use this machine for non-essential stuff. Some things I'm running on it are my personal RAG site for research papers, a Minecraft server, and some debugging and latex compilation jobs.

### Potato (My workstation)
![enter image description here](https://log.lli-debu.top/content/images/20260123230103-Potato.jpeg)
```
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣠⠤⠴⠒⠋⠉⠉⠉⠉⠙⠒⠲⠤⢴⣤⣄⠀⠀⠀   debu@Potato
⠀⠀⠀⠀⠀⠀⢀⣀⡴⠋⠁⠀⠀⠳⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠉⠳⡄⠀   ----------------
⠀⠀⠀⢀⠴⠊⠁⢸⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠘⠆⠘⡄   OS: Debian GNU/Linux 12 (bookworm) x86_64
⠀⢀⠜⠁⠀⠀⠀⠀⠑⠀⠀⠀⠀⠀⢸⠓⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡤⠀⢱   Kernel: 6.1.0-21-amd64
⢀⠎⠀⠀⠀⠀⠀⡤⣤⡀⠀⠀⠀⠀⠀⠉⠀⠀⠀⠀⠀⢀⠀⠀⠀⠀⠀⠀⠀⢸   Uptime: 5 days, 4 hours, 42 mins
⡎⠀⠀⠀⠀⠀⠀⠈⠒⠣⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠄⢀⣀⣠⠏   Packages: 2827 (dpkg)
⣧⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⠀⠀⠀⠀⠀⠀⣨⠁⠀   Shell: bash 5.2.15
⡟⠄⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠀⠀⠀⠀⠀⠀⠀⠈⠛⠃⠀⠀⠀⣠⡾⠃⠀⠀   Terminal: /dev/pts/29
⢱⡈⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠑⠠⡄⠀⠀⠀⠀⠀⢀⣠⠀⣀⡴⠋⠀⠀⠀⠀   CPU: AMD Ryzen Threadripper 7970X s (64) @ 4.000GHz
⠀⠑⢤⣀⠀⠀⣖⡆⠀⠀⠀⢄⡀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣠⠏⠀⠀⠀⠀⠀⠀   GPU: NVIDIA GeForce RTX 4090
⠀⠀⠀⠈⠙⠒⠢⠤⠤⣄⣀⣠⣤⣬⠶⠶⠦⠤⠶⠖⠚⠋⠀⠀⠀⠀⠀⠀⠀⠀   Memory: 5.91GiB / 125.29GiB (4%)
```
I eventually spent my stipend and upgraded to this workstation setup. It was a significant investment, but it’s worth it since it allows me to run experiments locally without having to deal with the awful university VPN. This setup also lets me mess around with the latest AI stuff like LLMs and diffusion models. It runs headlessly most of the time, but occasionally I connect a monitor for things like video editing or gaming. The ECC memory is a massive upgrade in terms of system stability.

I actually managed to get this setup at a great value. I bought the CPU, motherboard, and RAM as a bundle from Micro Center right before RAM prices skyrocketed. The RTX 4090 was snagged from Best Buy at MSRP, the PSU was an Amazon Black Friday deal, and everything else is from my old setup.

AMD YES!