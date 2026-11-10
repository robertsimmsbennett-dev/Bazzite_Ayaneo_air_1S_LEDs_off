# Bazzite_Ayaneo_air_1S_LEDs_off

AYANEO Joystick LED Disable Script when suspended or charging - BAZZITE ONLY

This automated script package is designed to disable the glowing joystick ring LEDs on AYANEO handheld devices running the Bazzite Linux operating system when suspended, or charging.
What the Fix Does

    Immediate LED Disable: Forces the active hardware brightness attribute for the joystick rings to zero (0), shutting off the lights instantly.
    Persistent Power-State Hook: Configures a systemd core override (systemd-suspend.service.d/override.conf) that hooks directly into the kernel's power management. Whenever the device wakes up from sleep, hibernation, or restarts from a low-power charging state, the script automatically re-applies the shutdown command so the lights never flash or turn back on.

Who It Is Intended For

It is built specifically for AYANEO handheld owners (such as users with the AYANEO Air Plus or Air 1S) who use Bazzite as their operating system, prefer a dark profile without distracting peripheral lighting, and want a hands-off, permanent solution that survives system reboots, deep sleep, and charging cycles without requiring manual terminal commands.
Operating System

    Primary OS: Bazzite (an immutable, Fedora-based Linux distribution optimized for gaming handhelds and desktop PCs).
    Environment: Fully compatible across both Steam Game Mode and the KDE Plasma Desktop Mode.

How to Run This
Method 1: Using the Terminal (Fastest & Most Reliable)

od 1: Using the Terminal (Fastest & Most Reliable)

Switch to Desktop Mode and open the Konsole terminal.

Navigate to your Downloads folder where the script was saved:
Bash

cd ~/Downloads

Make the script executable:
Bash

chmod +x install-ayaneo-led-fix.sh

Run the installer using sudo (since it requires root permissions to configure systemd services):
Bash

sudo ./install-ayaneo-led-fix.sh

Enter your device password when prompted.
Verification: The script will output confirmation steps showing that the persistence service was created, reloaded, and enabled successfully.

Method 2: Using the Graphical File Manager (Desktop Mode)

If you prefer using the mouse and want to make the file launchable directly from the desktop or file manager:

Open the Dolphin file manager and go to your Downloads folder.

Locate install-ayaneo-led-fix.sh.

Right-click the file and select Properties.

Go to the Permissions tab, check the box that says Is executable, and click Apply / OK.

To run it: Right-click the file again and look for an option like Run in Konsole (or open your terminal in that folder and run sudo ./in
