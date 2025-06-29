
# VPN Setup Report

## Objective  
The main goal of this task is to gain practical knowledge about how Virtual Private Networks (VPNs) function, specifically their role in enhancing privacy and securing communications on the internet.

## VPN Client Selected  
**ProtonVPN (Free Tier)** – chosen for its strong privacy policies, transparency, no-logs commitment, and secure encryption protocols.

---

## Detailed Setup Steps  

### 1. Research and Selection of VPN Service  
Compared ProtonVPN, Windscribe, TunnelBear, and Hotspot Shield. ProtonVPN stood out for its transparency and open-source nature.

### 2. Creating a ProtonVPN Account  
1. Go to [ProtonVPN](https://protonvpn.com).
2. Click **Sign Up**.
3. Choose the **Free Plan**, enter your **email** and create a **strong password**.
4. Verify your email.



### 3. Downloading and Installing the VPN Client  
1. Download client from ProtonVPN’s [official site](https://protonvpn.com/download).
2. Run the installer and follow instructions.



### 4. Launching the VPN Client and Logging In  
Launch the installed app, enter your credentials.


### 5. Choosing and Connecting to a VPN Server  
Select a nearby country (e.g., Netherlands), then click **Connect**.



### 6. Verifying VPN Connection  

**Before VPN:**  
```bash
curl ifconfig.me
# Output: <Your actual IP>
```

**After VPN:**  
```bash
curl ifconfig.me
# Output: <VPN IP from selected country>
```

Also used [https://whatismyipaddress.com](https://whatismyipaddress.com) to confirm.

### 7. DNS Leak Test  
Visit [https://dnsleaktest.com](https://dnsleaktest.com). Ensure DNS servers match your VPN’s location.



### 8. Disconnecting VPN and Comparing Speed  
Tested speeds using [Speedtest.net](https://www.speedtest.net). Observed ~30% reduction in speed when VPN was active.


## VPN setup and results:
1. Choose a Reputable VPN Service
VPN Selected: ProtonVPN 
Reason: Strong privacy policy, free tier with no ads, open-source client.  
Signup Output: Account created using email, verified successfully.
 
3. Download and Install the VPN Client
Action: Downloaded ProtonVPN for Windows from official website.  
Result: Installation successful without any issues.

3. Connect to a VPN Server
Server Chosen: Netherlands (closest available on free plan)    
Status: Connection successful. VPN tunnel established in ~3 seconds.  
Dashboard Output: Green status indicator, IP address listed as Dutch server.

5. Verify IP Address Change
Before VPN: IP – 103.xxx.xxx.xxx, Location – India  
After VPN: IP – 185.xxx.xxx.xxx, Location – Netherlands  
Confirmation:  IP successfully masked and changed.

5. Browse Website to Confirm Encryption
Websites Tested: Gmail, ProtonMail, Bank Login Page  
Result: Pages loaded securely using HTTPS. 
DNS Leak Test:  No DNS leaks detected.  
Conclusion: All traffic is encrypted and rerouted.

6. Disconnect and Compare Performance
Browsing Speed (before VPN): 47 Mbps  
Browsing Speed (with VPN): 21 Mbps  
Browsing Speed (after disconnect): 46 Mbps   
IP reverted: Yes  
Conclusion: Minor speed drop with VPN due to encryption overhead.

7. Research: VPN Encryption and Privacy
Encryption Used: AES-256 (military-grade)   
Protocols Supported: OpenVPN, IKEv2/IPSec, WireGuard (ProtonVPN)  
Privacy Features:
- No-logs policy
- Kill switch
- DNS leak protection
- Secure Core routing (paid)

## Summary of VPN Benefits  
- Privacy and anonymity online
- Secure encrypted traffic over public Wi-Fi
- Bypass geo-blocking and censorship
- Prevent ISP throttling

## Summary of VPN Limitations  
- Reduced connection speeds
- Free plans have limitations (fewer servers, lower priority)
- Some websites block VPN traffic
- Trust in provider is crucial

---

## Additional Notes  

### Common Commands Used (Linux/macOS):
```bash
curl ifconfig.me         # Check current IP
nmcli connection show    # Show all active connections
sudo killall openvpn     # Kill all VPN processes (if CLI used)
```


## Conclusion  
ProtonVPN provided a safe and efficient method to explore the functionality and practical benefits of VPNs. Hands-on experimentation helped illustrate both the advantages (privacy, encryption) and limitations (speed, blocked content) of using VPN services.
