## 1 instuction1. Prepare Their Device

A. For Windows Users:  
 • Download the ZeroTier client installer from:  
  https://www.zerotier.com/download.shtml  
 • Run the installer and follow the instructions to install the ZeroTier One client.  

B. For macOS Users:  
 • Download the ZeroTier One package for macOS from:  
  https://www.zerotier.com/download.shtml  
 • Open the downloaded DMG file and drag the ZeroTier One app to your Applications folder.  
 • You might need to grant additional security permissions via System Preferences → Security & Privacy if macOS blocks the app.  

──────────────────────────────
## 2. Join the ZeroTier Virtual Network  

A. Once installed, the ZeroTier client will run in the background. To join the network, users need your ZeroTier Network ID.  
 • On Windows:  
  – Right-click the ZeroTier icon in the system tray.  
  – Select “Join Network…”  
  – Enter the provided network ID and press “Join.”  
 • On macOS:  
  – Click the ZeroTier icon in the menu bar.  
  – Choose “Join Network…” and enter the network ID.  
Alternatively, via the command line (if familiar):  
 – Open Command Prompt (Windows) or Terminal (macOS) and run:  
  zerotier-cli join <NETWORK_ID>  

──────────────────────────────
## 3. Admin Authorization via ZeroTier Central  

A. Log in to ZeroTier Central (https://my.zerotier.com) with your administrative account.  
B. Navigate to your network’s “Members” list.  
C. You will see new devices appearing once users join the network. Each device will be listed with a unique Node ID.  
D. For security, make sure to check (authorize) the checkbox next to each new device. This “Auth” step allows them to communicate on the network.  
E. Optionally, assign meaningful names or tags so you can easily identify users later.  

──────────────────────────────
## 4. Logging in via SSH to the Bunker  

A. For Windows Users:  
 Option 1: Using PuTTY  
  • Download PuTTY (https://www.putty.org).  
  • Open PuTTY.  
  • In the “Host Name” field, enter the bunker’s ZeroTier IP.  
  • Ensure the port is set to 22.  
  • Click “Open.”  
  • When prompted, log in using your SSH username and password (or key-based authentication details).  
  Option 2: Using Windows Terminal or PowerShell (if using OpenSSH client)  
  • Open Command Prompt, Windows Terminal, or PowerShell.  
  • Type:  
   ssh username@<bunker_ZeroTier_IP>  
  • Press Enter and complete authentication.  

B. For macOS Users:  
 • Open Terminal.  
 • Type:  
  ssh username@<bunker_ZeroTier_IP>  
 • Press Enter and follow the prompts (possibly accepting the host fingerprint and then entering your password or using your SSH key).  
