🚀 JLinux-Helpdesk
A Custom Debian-Based Live ISO for IT Support Engineers, Sysadmins, and Linux Learners

JLinux-Helpdesk is a fully customized Debian 12 (Bookworm) live ISO built with live-build, designed specifically for IT professionals who want a fast, preconfigured environment packed with troubleshooting tools, dev utilities, and system administration enhancements.

This project demonstrates real-world Linux engineering skills including image building, package customization, filesystem tailoring, branding, automation, and ISO packaging.

🌟 Features
🔧 Technical Foundation

Built on Debian 12 (Bookworm)

Generated with live-build (enterprise-grade image-building framework)

Produces a bootable ISO-Hybrid image (USB or VM)

🖥️ Desktop Environment

XFCE: Lightweight, fast, and ideal for IT tools

Custom hostname & MOTD branding

Optional custom wallpaper under:
config/includes.chroot/usr/share/jlinux/wallpaper.png

🧰 Included Tools
System & Network Utilities

htop — system monitoring

tmux — terminal multiplexing

curl, wget — transfer tools

net-tools, dnsutils, traceroute

nmap — scanning

tcpdump — packet capture

iperf3 — network throughput testing

openssh-client

Dev & Scripting Tools

git

vim / neovim

build-essential

python3, pip

GUI Utilities

Firefox ESR

Filezilla

Wireshark (graphical packet analyzer)

🧩 Custom Enhancements

Default aliases (in /etc/skel/.bash_aliases):

ll='ls -lah'
update='sudo apt update && sudo apt upgrade -y'
gs='git status'
v='vim'


Custom MOTD at login

Custom hostname: jlinux

📁 Project Structure
jlinux-helpdesk/
│
├── config/
│   ├── package-lists/
│   │   └── jlinux.list.chroot     # Installed software
│   ├── includes.chroot/           # Files injected into the live system
│   │   ├── etc/                   # Hostname, MOTD, aliases, configs
│   │   └── usr/share/jlinux/      # Wallpaper, branding assets
│   └── ...                        # live-build configuration layers
│
├── .gitignore                     # Ensures chroot/cache not committed
└── README.md                      # Project documentation

🛠️ How to Build the ISO
1️⃣ Install Dependencies
sudo apt update
sudo apt install -y live-build git

2️⃣ Clone the Repo
git clone https://github.com/<yourusername>/jlinux-helpdesk.git
cd jlinux-helpdesk

3️⃣ Build the ISO
sudo lb clean
sudo lb build


When complete, you’ll see an output file similar to:

live-image-amd64.hybrid.iso


Rename if desired:

mv live-image-amd64.hybrid.iso jlinux-helpdesk.iso

▶️ How to Run the ISO (VirtualBox)

Create a new VM

OS Type: Linux → Debian (64-bit)

RAM: 2–4 GB

Go to Settings → Storage → Add Optical Drive

Select jlinux-helpdesk.iso

Boot & explore.

🧪 What This Project Demonstrates

This project is ideal for showcasing:

Linux OS customization

Live image building (Debian live-build)

Package/environment automation

System configuration & branding

Filesystem injection

Git versioning of operating system artifacts

Virtualization testing (VirtualBox)

Perfect for roles like:

Linux Administrator

DevOps Engineer

IT Systems Engineer

Help Desk Automation Specialist

Cybersecurity Analyst Boot Environments

🔮 Future Enhancements (Roadmap)

Automated installer (Preseed/Kickstart)

Cloud-init support

Persistent USB overlay mode

Custom systemd services

“Cybersecurity edition” ISO

“Developer edition” ISO

Networking toolkit edition

🤝 Contributing

Pull requests and issues are welcome — suggestions from other Linux engineers appreciated.
