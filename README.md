<p><b>LeGo1 Fan Control</b> is a fork of <a href="https://github.com/Rodpad/LeGo2-Fan-Control-Decky">Rodpad/LeGo2-Fan-Control-Decky</a> by <b>Luke Cama</b> (GPL-3.0), maintained by <a href="https://github.com/everancii">everancii</a>, with Lenovo Legion Go 1 (83E1) support added: a Full Fan Speed toggle (the firmware's own override), live temp/RPM monitoring, and one-click installation of the acpi-call module on pacman-based distros such as CachyOS. All Legion Go 2 functionality is unchanged. Full credit for the original plugin goes to Luke Cama.</p>

<p>Tired of your Legion Go 2 fan revving up and down at high speeds regardless of light or heavy games? Existing fan control applications don't let you override the hardware's minimum fan speeds. Frustrated by this I built a tool that bypasses this limitation.</p>

<br>

<h3>LeGo2 Fan Control</h3>
LeGo2 Fan Control controls your fan directly at the hardware level. You can set any fan speed at any temperature, and it will actually take effect. You could even set the fan to 0 RPM at 100°C if you really wanted to (don't do this 🫠).

Some of the core features include:
<ul>
<li><b>Interactive Fan Curve Graph:</b> Create your own fan curve with a clean graphic interface.</li>
<li><b>Fan Smoothing Algorithm:</b> Designed to ignore micro-spikes in temperatures whilst ensuring gradual temperature changes are responded to, keeping the fan steadier and less noticeable.</li>
<li><b>Link to Power Modes:</b> Assign completely different fan curves to your Low Power, Balanced, Performance, and Custom power profiles. 
Stepped Fan Curves:</b> Makes your fan speed only change at temperature breakpoints along the graph, rather than along the whole graph at every degree change.</li>
<li><b>Lightweight & Unobtrusive:</b> CPU usage sits around 0% to 0.2% and uses less than 64Mb of memory.</li>
<li><b>Thermal Failsafe:</b> If your APU ever hits 101°C, the app instantly kicks in a high RPM to cool down.</li>
<li><b>Anti-Cheat Safe:</b> Windows utilises the open-source <a href=https://github.com/namazso/PawnIO">PawnIO</a> driver for secure hardware access. Linux uses native kernel pathways.</li>
</ul>

<br>
<h4>Legion Go 1 (83E1) support</h4>
<p>The original Legion Go does not expose direct RPM control like the Go 2, so on that device the plugin offers:
<ul>
<li><b>Full Fan Speed toggle:</b> Uses the firmware's own full-speed override (the same mechanism Lenovo's Legion Space app and <a href="https://github.com/hhd-dev/hhd">Handheld Daemon</a> use) to lock the fan at maximum RPM. Turn it off to return to the automatic fan curve.</li>
<li><b>Live monitoring:</b> APU temperature and fan RPM readouts, with the RPM read straight from the EC.</li>
</ul>
The full-speed toggle requires the <b>acpi_call</b> kernel module. On pacman-based distros (CachyOS, Arch) the plugin panel includes an <b>Install acpi-call</b> button that installs and loads it for you. Bazzite and Nobara ship it by default; elsewhere install the module for your distro manually. The panel will tell you if it is missing.</p>

<br>
<h4>Platforms</h4>
<ul>
<li><p><b>Decky Loader Plugin Version (SteamOS / Bazzite / CachyOS etc…):</b>
  <img src="https://i.postimg.cc/WbvDYRRn/LG2FC-decky.jpg">
Download the free Decky Loader plugin version <a href="https://github.com/Rodpad/LeGo2-Fan-Control-Decky/releases">here</a>.<br>
To install, open Decky Loader, go to the Settings cog, Developer and then “Install Plugin from ZIP file”.<br>
Source available <a href="https://github.com/Rodpad/LeGo2-Fan-Control-Decky">here</a></p></li>
  
<li><p><b>Windows Version:</b>
  <img src="https://i.postimg.cc/bJVGFdhY/LG2FC-windows.png">
This GitHub is for the Decky Loader plugin version, however the separate closed source Windows version can be downloaded <a href="https://ftp.laptopwiki.eu/web/client/pubshares/3EX8zE3JFaWNAeV2M8j5iC?compress=false">here</a>.<br>
Please ensure you download and install <a href=https://pawnio.eu/>PawnIO</a> before running LeGo2 Fan Control for Windows.</p></li>
<br>
<p><b>Windows Changelog:</b></p>

June 4th 2026:
<ul>
<li>Fixed an issue where custom fan speeds would stop working after waking the device from sleep. </li>
<li>Fixed the app accidentally opening in fullscreen mode when restored from a background startup. </li>
</ul>
<br>

June 5th 2026:
<ul>
<li>Improved taskbar and systray behaviour. </li>
</ul>
<br>

June 7th 2026:
<ul>
  <li>Improved reliability where an issue would make the app could appear blank when launched</li>
</ul>
<br>
<h4>Disclaimer / Warning</h4>

<p>By using this software, you accept full responsibility for any damage that may occur. Bypassing hardware thermal limits carries inherent risks; use sensible fan curves.</p>

<br>
<h4>Created by</h4>

<p>Luke Cama</p>

<br>
<h4>Acknowledgements</h4>

<p>A special thanks to Undervoltologist for their help in reverse engineering EC behaviour.
https://github.com/Undervoltologist</p>
