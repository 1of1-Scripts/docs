---
icon: circle-info
---

# Disable UDP for RDP

* **Prevent UDP-based RDP Exploits**: UDP is more susceptible to spoofing and reflection attacks. Disabling UDP can mitigate risks related to **man-in-the-middle (MITM)** and **replay attacks**.
* **Protection Against DDoS Attacks**: Some RDP-based attacks leverage UDP for amplification. Disabling it reduces attack vectors.
* **Better Encryption Control**: TCP-based RDP traffic is typically encrypted via TLS, while UDP-based traffic might have different security mechanisms.

## Disable UDP for RDP using a single PowerShell command.

### Run the following **elevated PowerShell command** (as Administrator):

```powershell
Set-ItemProperty -Path "HKLM:\SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services\Client" -Name "fClientDisableUDP" -Value 1 -Type DWORD -Force
```

### **Verification:**

To check if the setting was applied correctly, run:

```powershell
Get-ItemProperty -Path "HKLM:\SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services\Client" -Name "fClientDisableUDP"
```

If it returns:

```
fClientDisableUDP : 1
```

Then UDP is disabled for RDP.

### **Apply Changes:**

For the change to take effect, restart your dedicated server or VPS.

Now, RDP will only use **TCP** and not UDP.
