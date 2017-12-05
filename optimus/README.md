## How I finally got this working
1. Added virtual screens to i915 xorg.conf.d
2. Changed bumblebee xorg.conf.nvidia to use EDID and outputs
3. Added `acpi_osi=! acpi_osi="!Windows 2009" pcie_port_pm=off` to kernel command line
   - Note that one of these might not be needed
   - Since adding this, there has been some odd backlight flickering when adjusting
4. Fire up `intel-virtual-output` whenever I wanted to use an external display
   - *after* plugging it in, or it won't be picked up.
5. Profit!!!
