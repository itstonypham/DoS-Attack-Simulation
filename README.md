# DoS Attack Simulation Runbook

  <img src="https://github.com/itstonypham/DoS-Attack-Simulation/blob/images/dos.png?raw=true" alt="Description" width="35%">
<small>Image source:  
<a href="https://www.upguard.com/blog/what-is-a-ddos-attack">https://www.upguard.com/blog/what-is-a-ddos-attack</a></small>


## 📌 Overview
The purpose of this runbook is to simulate a DoS attack to assess system resilience and response capabilities under stress, identifying vulnerabilities and improving security measures. 

## 📖 What is a Runbook?
The runbook is a document used to create a simulated situation so that blue teams (Defence) can practice the response plan.  

## 🛠️ Setup
### Step 1: Initial Setup for Simulating a DoS attack
- Set up VMs in the same network, use ping to verify connectivity, and ensure firewall settings allow traffic.

  ![Description](https://github.com/itstonypham/DoS-Attack-Simulation/blob/images/image4.png?raw=true)

### Step 2: Start the DoS
- Use a tool such as hping3 to send a flood of requests to the target server targeting port 80.
   ```bash
   sudo hping3 -S -p 80 --flood 192.168.0.1
   ```

  ![Description](https://github.com/itstonypham/DoS-Attack-Simulation/blob/images/image4.png?raw=true)

  
### Step 3: Monitor Server Performance
- Check for slow response or service disruption using network monitoring tools (e.g., Wireshark or Netstat).

  ![Description](https://github.com/itstonypham/DoS-Attack-Simulation/blob/images/image2.png?raw=true)

### Step 4: Confirm Downtime and Stop the Attack
- Use the ping command to check if the server is unresponsive. Record the time it takes for the server to stop responding. Run CTRL+C to stop the attack in the terminal. Document the attack.

  ![Description](https://github.com/itstonypham/DoS-Attack-Simulation/blob/images/image3.png?raw=true)

## 🔚 DoS Attack Response Procedure
This document outlines procedures for responding to a DoS attack, ensuring service restoration and system protection. It follows the NIST Incident Response Framework to guide effective mitigation and defense during incidents.

### Step 1: Preparation
Ensure network defenses like firewalls and load balancers are active to protect against threats. 
### Step 2: Detection & Analysis
Use network monitoring tools to identify unusual traffic patterns, such as spikes or irregular requests. Check logs to trace the source of the attack, confirming it as a DoS incident for effective response and mitigation.
### Step 3: Containment, Eradication & Recovery
Block malicious IP addresses using the firewall to prevent further attacks. Implement traffic filtering or rate limiting to manage incoming requests, reducing the impact on your server. Once traffic levels normalise, restore service to ensure availability for legitimate users.
### Step 4: Post Incident Activity
Check logs and performance data to find weaknesses. Strengthen defenses, like DoS protection and update security policies. Share what you learned with the team to improve future responses.


## 🔚 Conclusion
This runbook provides a structured approach to simulating and mitigating DoS attacks, improving response readiness. Regular testing and analysis help strengthen defenses, minimise downtime and ensure a resilient, secure network against future threats.

## 👤 Author
**Tony Pham** – [GitHub](https://github.com/itstonypham) | [LinkedIn](https://www.linkedin.com/in/itstonypham/)

## 🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss.  


## ⭐ Acknowledgments
Thanks to contributors and resources that helped with the project.

---
