---
icon: circle-info
---

# 'wmic' Command

> Failed to get processes tree usage data.
>
> This is probably because the 'wmic' command is not available in your system.
>
> If you are on Windows 11 or Windows Server 2025, you can enable it in the Wndows Features settings.

That error is happening because the **`wmic`** (Windows Management Instrumentation Command-line) tool is missing or disabled on your system.

\
Newer versions of Windows (like Windows 11 and Server 2025) have **deprecated WMIC** by default, but you can re-enable it or use a modern alternative.

Here’s how to fix it depending on your setup:

***

#### **Option 1: Re-enable WMIC on Windows 11 / Server 2025**

1.  Press **Windows + R**, type:

    ```
    optionalfeatures
    ```

    and press **Enter**.
2. In the **Windows Features** window:
   * Scroll down to **Legacy Components** or **WMIC** (if shown).
   * Check the box next to it and click **OK**.
3. Reboot your system.
4.  Test in Command Prompt:

    ```
    wmic
    ```

    If it opens the WMIC prompt, it’s restored.

***

#### **Option 2: Use PowerShell Equivalent**

If WMIC isn’t available or can’t be re-enabled, you can replace its functionality with PowerShell.

For example, if your application/script is trying to get CPU or process info via WMIC, you can use:

```powershell
Get-Process
Get-WmiObject Win32_Process
```

If it’s your own code, replace WMIC calls with PowerShell equivalents.

***

#### **Option 3: Manually Reinstall WMIC**

If “Windows Features” doesn’t list WMIC:

1. Open **PowerShell (Admin)**.
2.  Run:

    ```powershell
    dism /online /add-capability /capabilityname:WMIC~~~~
    ```
3. Restart your machine.
