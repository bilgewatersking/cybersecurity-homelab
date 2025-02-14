# **A full stack Cybersecurity Homelab**
Hi everyone! This lab is designed with a multitude of domain focused projects based on my professional experiences and knowledge working as a Cybersecurity Engineer. You are free to use this repo as you please as long as you learn something from it. This project is an homage to the younger me who, through struggle, determination and hard work helped shape me into who I am today. 
To the future me, when you look back at all that you've learnt and accomplished, all the eager, cybersecurity enthusiasts you've helped, I want you to feel proud and grateful for everything you've achieved. None of this would be possible without God's help and living vicariously through the mantra, "Trust in Allah, do your best, leave the rest to Him". Alhamdulillah.

## Little bit About me
My name is Waseem. I am a 29 year old Sri Lankan, and some of my hobbies are reading, writing poems, photography, making vlogs, gaming, tinkering with cybersecurity tools trying to find my own template of approaching this fast evolving field and doing some physical activities like football, cricket, padel tennis, swimming and gymming. 
My cybersecurity journey started 3 years ago when I decided Mechanical Engineering wasn't for me. During this midlife crisis I analyzed my strengths and personality traits to figure out a career path - a field I could look forward to waking up everyday for. That turned out to be cybersecurity. I find my personality aligns more with Red Teaming, but to be a good hacker you need to know how systems work at the fundamental level before you exploit them. If you'd like to get in touch with me, you can find me on LinkedIn *https://www.linkedin.com/in/waseem-rahman/*

So without further ado, let's get started!

## List of Components used in this Lab
| Tool | Objective     | Domain  |
|-----|---------------|---|
|Spare Laptop/Server |To host our virtual environment (VE). Will serve as a bare metal hypervisor (VE running directly on hardware)|Security Architecture   |
|Proxmox| Virtual Environment that will host all servers and VMs. Will also be used to create our networking interfaces|Security Architecture   |
|Kali Linux|Our primary Red teaming tool|Penetration Testing   |
|Ubuntu Server|Lightweight OS perfect for our use case|Security Architecture   |
|Atomic RedTeam|Library of attacks based on MITRE ATT&CK framework|Penetration Testing   |
|Wazuh|SIEM which will be the base of our SOC|SOC   |
|TheHive|For Incident Response (IR)|SOC   |
|Cortex|For threat/alert analysis and Active response|SOC   |
|Shuffle|SOAR platform. Syncs well with Hive, Cortex and Wazuh for automated response to threats|SOC   |
|Ansible|Our primary automation tool that will use custom playbooks built based on SIEM use cases for IR|DevSecOps   |
|Kubernetes|Will use K3s and Kubernetes GOAT later on. Will be used alongside Ansible and AWS later on in depth|DevSecOps   |
|DVWA, OWASP Juice Shop| Main victim machines. Intentionally vulnerable web apps we will hack into |Application Security   |
|Docker, Portainer|Docker to pull images and portainer to manage all our images|DevSecOps   |
|Jenkins|Our CI/CD server|Application Security   |
|DefectDojo|Centralized Application Security Vulnerability Management platform. All CI/CD security scans will send reports here|Application Security   |
|Snyk and Sonarqube|SAST scanning|Application Security   |
|OWASP ZAP|DAST Scanning|Application Security|
|NGINX|Web server. Will use nginx ingress as load balancer once we deploy Kubernetes clusters.|Security Architecture   |
|Excel, Word|Reporting and documentation|Governance, Risk and Compliance   |
|More to be added as we go deeper| - | - |

## Action Plan for this Lab. Detailed write ups for each domain will be in their respective folders.
- [x] Have your pfsense, kali linux, and ubuntu server iso's downloaded beforehand.
- [x] After downloading proxmox and rufus, flash proxmox onto a USB using rufus. Ensure you have an ethernet cable connected to your router on your spare laptop. Trust me this will save you hours of troubleshooting internet connectivity issues after installing proxmox.
- [x] In BIOS settings, change to secure boot and change SATA operation from RAID to AHCI (you'll encouter an issue with raid when installing proxmox). Then set boot priority to proxmox usb
- [x] Once Proxmox is installed, configure virtual networks and upload the ISO images to the VE.
- [ ] Create PFsense vm.
- [ ] Create Kali Linux vm.
- [ ] Create Ubuntu vm to deploy Docker, Portainer, Jenkins, DVWA and OWASP Juice shop.
- [ ] Create Ubuntu vm for SOC.
### In the future, after Phase 1 is completed, we will enhance our PenTesting skills by adding Kubernetes, AWS and Mobile App hacking to our skill set. 
- [ ] Create a kubernetes cluster and deploy 'kubernetes-goat'.
- [ ] Deploy 'AWSGoat'. This will also teach us about IAC, specifically terraform.
- [ ] Deploy Goatlin and use MobSF tool for android mobile app pentesting.
