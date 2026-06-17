# 🖥️ Performance

{% hint style="danger" %}
Understanding the configuration changes is recommended before proceeding - the MoonBD team assumes no responsibility for any misconfiguration.
{% endhint %}

### UI / Notification Clean-Up <a href="#ui-notification-clean-up" id="ui-notification-clean-up"></a>

* The [Edit UI](https://imgur.com/Rg1mIMt) option can be used to customize the game’s user interface.
* Keeping as few [chat boxes](https://imgur.com/v76jvyI) active as possible improves performance. Chats that are not needed can be hidden.
* Disabling [chat scroll animations](https://imgur.com/iebshJB) helps reduce CPU overhead.
* The [3D minimap](https://imgur.com/6yw5j7l) greatly improves performance in CPU-limited situations by removing the directional arrows.
* In the general settings, [Alerts](https://i.imgur.com/O0EYEwz.png) section, disabling all in-game alerts is recommended unless they are specifically required.
* Enabling [Mouse Movement](https://i.imgur.com/lWRlQxw.png) can increase the framerate while the mouse is on screen.

### In-game Settings <a href="#in-game-settings" id="in-game-settings"></a>

* Disabling [low power mode](https://i.imgur.com/vJgXCtW.png) is recommended.
  * Low power mode makes the game sleep for about 10ms every frame to use fewer resources.
  * This feature is primarily useful on high-end configurations while streaming to free up resources for OBS, or to conserve power on laptops.
* For systems with weaker graphics hardware, enabling both [Upscale](https://i.imgur.com/zb5mpZa.png) and [Crop Mode](https://i.imgur.com/bNO1woS.png) settings drastically reduces the render resolution and boosts frame rates.
* [Attack Decisions](https://i.imgur.com/ISy6GDZ.png) consume CPU resources to display. Players familiar with combat mechanics can disable these indicators.
* Setting the [Effect Optimization](https://i.imgur.com/bMJ0pme.png) slider to approximately 40% from the left uses lower quality effects for other players without hiding them completely. This keeps performance high while maintaining effect visibility.
  * This setting can be combined with [Remove Faraway Effects](https://i.imgur.com/YSzpZar.png) to clear unnecessary particles without hiding skill effects completely.
  * During large-scale PvP scenarios or group PvE activities, temporarily choosing to [Remove Others’ Effects](https://i.imgur.com/sjiwABj.png) can further improve performance.
* The [Character Optimization](https://i.imgur.com/ifGkFN4.png) setting is generally kept disabled to ensure all characters are visible during combat, except under specific circumstances:
  * While fighting world bosses such as **Karanda**, **Vell**, and **Garmoth**, pressing `Shift + F5` toggles the visibility of other players.
* The [Performance Optimization](https://i.imgur.com/hfb5l9o.png) setting allows more assets to be retained in system RAM. This helps mitigate disk-streaming stuttering.
  * Enabling this setting is recommended for systems with over 16 GB of RAM, while 32 GB or more RAM yields the most benefit.

### SSD Performance <a href="#ssd-performance" id="ssd-performance"></a>

* Running the game from a standard hard drive can cause significant stutter during asset streaming, often resulting in loading walls when riding mounts.
* An M.2 PCIe NVMe SSD is recommended to eliminate asset-streaming stutter, provided the system RAM is sufficient.

### Disabling Vertical Sync <a href="#h.74w5a0s9z59u" id="h.74w5a0s9z59u"></a>

Windows 10 versions 1703 or 1709 may contain bugs that prevent vertical sync from being disabled.

Laptops equipped with dual graphics solutions might be unable to disable vertical sync.

Disabling fullscreen optimizations in the game executable's properties may prevent vertical sync from being disabled in fullscreen mode, depending on the system configuration.

**Nvidia**

<figure><img src="../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

In the NVIDIA Control Panel, a game profile for Black Desert can be added to disable vertical sync.

**AMD**

<figure><img src="../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
In AMD Radeon Settings, enabling Radeon Enhanced Sync for the Black Desert game profile and disabling the wait for vertical refresh is recommended.
{% endhint %}

#### Disable V-Sync in Windowed Modes <a href="#h.promh3xw4ocr" id="h.promh3xw4ocr"></a>

Players can `right-click` the desktop and select **Display settings**. From there, navigation goes to the bottom of the menu to the **Graphics** section under **Related settings**, then to **Change default graphics settings**.

![](https://docs.dusthorizon.com/~gitbook/image?url=https%3A%2F%2F1487308100-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F1ZyNkRpnTmMrdd8zPirl%252Fuploads%252Fgit-blob-af1f9892cfc62a8c92c19742b62158a880e47eb9%252Fpasted%2520image%25200%2520%283%29.png%3Falt%3Dmedia&width=768&dpr=3&quality=100&sign=13a37254&sv=2)![](https://docs.dusthorizon.com/~gitbook/image?url=https%3A%2F%2F1487308100-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F1ZyNkRpnTmMrdd8zPirl%252Fuploads%252Fgit-blob-97d1285733e82868520c9109efa38c7d7372a933%252Fpasted%2520image%25200%2520%284%29.png%3Falt%3Dmedia&width=768&dpr=3&quality=100&sign=5668e208&sv=2)

From this menu, the "Optimizations for windowed games" option can be enabled. If vertical sync is disabled in the graphics driver, it will be disabled in windowed mode as well.

Enabling NVIDIA G-SYNC for fullscreen mode will still apply it to windowed mode when this optimization is enabled due to Multiplane Overlay (MPO) support. Further details are available in the NVIDIA driver release notes.

### Quirks of Windowed Optimizations <a href="#h.k2x8z6uvzbhn" id="h.k2x8z6uvzbhn"></a>

* When Windowed Optimizations are enabled, frame rates may remain capped at approximately 210 FPS on a 144Hz screen (or 1.5x the refresh rate). A known workaround is enabling NVIDIA G-SYNC or AMD FreeSync on a compatible display.

<figure><img src="../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure>

* Once G-SYNC is enabled globally, it can be disabled specifically for Black Desert in the NVIDIA Profile Inspector if stuttering or video playback issues occur.

<figure><img src="../.gitbook/assets/image (338).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
The configuration above is required to prevent playback stuttering on Twitch on secondary monitors with modern NVIDIA graphics drivers when the Black Desert window is in focus, especially when Hardware Accelerated GPU Scheduling is enabled and GPU usage is high.
{% endhint %}

* Setting the Desktop Window Manager (DWM) to use Fast Sync rather than vertical sync is another option, which may help improve game fluidity in windowed modes.

<figure><img src="../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Testing this setting is recommended, as it may improve frame pacing or have no noticeable effect, but it does not cause performance degradation.
{% endhint %}

### Nvidia Driver Tweaks <a href="#h.gjxrz4o3rug7" id="h.gjxrz4o3rug7"></a>

{% hint style="info" %}
Downloading [Nvidia Profile Inspector](https://github.com/Orbmu2k/nvidiaProfileInspector/releases) simplifies customizing these settings.
{% endhint %}

**Threaded Optimizations**

{% hint style="info" %}
This setting defaults to Auto.
{% endhint %}

* For older quad-core processors without hyperthreading or first-generation AMD Ryzen CPUs, disabling this setting may reduce stuttering.
* For newer CPUs with 6 or more physical cores, this setting should be enabled to maximize frame rates.

**Ansel**

* Disabling NVIDIA Ansel is recommended to reduce micro-stutters.

**Shader Cache**

* The shader cache setting can be adjusted based on system performance. While enabling it is generally recommended to prevent shader compilation stutter, disabling it may resolve issues on systems with slower storage devices.

<figure><img src="../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Applying these changes in the Black Desert profile prevents interference with other applications.
{% endhint %}

**Power Management Mode**

* The Power Management Mode can be set to Adaptive.
  * "Prefer maximum performance" maintains maximum GPU clock speeds. While beneficial during active gameplay, it increases power consumption during idle or AFK activities.
  * "Optimal power" reduces GPU clock speeds during periods of low activity, though clock frequency transitions may occasionally trigger minor stutters.
* On newer graphics cards, selecting "Prefer maximum performance" in the NVIDIA Control Panel is recommended. The card still reduces clock speeds and power draw when the game is minimized to the system tray.
  * "Adaptive" maintains high clock speeds under load and lowers them during low GPU utilization to conserve power.

<figure><img src="../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Applying these changes in the Global profile extends these power management benefits to all applications.
{% endhint %}

**G-Sync**

G-SYNC improves responsiveness and reduces input lag when frame rates remain below the monitor's maximum refresh rate.

{% hint style="warning" %}
Enabling G-SYNC is a matter of personal preference; it reduces input lag but may make frametime stutters more apparent.
{% endhint %}

**Ultra Low Latency Mode**

If the CPU can handle the additional overhead of delivering frames to the GPU on demand rather than queuing them asynchronously, enabling NVIDIA Ultra Low Latency Mode can reduce input latency.

{% hint style="warning" %}
This setting may introduce stuttering if the CPU is unable to process frame requests in real-time.
{% endhint %}

<figure><img src="../.gitbook/assets/image (342).png" alt=""><figcaption></figcaption></figure>

### CPU Performance - Set Affinity <a href="#h.rl325eap4pk9" id="h.rl325eap4pk9"></a>

**CPU optimization tweaks for Black Desert are beneficial due to several system behaviors:**

1. The game does not scale efficiently with Intel Hyper-Threading (HT) or AMD Simultaneous Multi-Threading (SMT), often leading to lower performance when SMT/HT is active.
2. The game requires low-latency processor cache access during CPU-intensive situations.
3. Allocating more than 6 physical cores can cause performance regression over time. Disabling Core 0 is recommended if other cores are available, as the Windows scheduler prioritizes Core 0 for background processes.
4. Using software-level affinity masking prevents performance loss in other applications. Since most software benefits from multi-threading, disabling SMT/HT globally at the BIOS level is not recommended.

**To configure CPU affinity:**

* The physical cores to be utilized must be identified, and an [affinity calculator](https://bitsum.com/tools/cpu-affinity-calculator/) can be used to determine the appropriate hexadecimal affinity mask.

{% hint style="info" %}
Some common CPU Affinities for Ryzen are detailed in the sections below.
{% endhint %}

* A batch file (Windows Command Line script) is created with the following command template:

```
cd /d "Path To Black Desert"
Start /affinity AffinityMask BlackDesertLauncher.exe
```

<figure><img src="../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
This illustration shows an example configuration. The affinity mask varies depending on the system's CPU model.
{% endhint %}

* The `.bat` file is placed in the game launcher directory, and a shortcut can be created on the desktop.
* The shortcut properties are configured to run the script as an administrator, which is required to set process affinity.
* For Steam configurations, the launch command includes the `-steam` parameter:

```
cd /d "Path To Black Desert"
Start /affinity AffinityMask BlackDesertLauncher.exe -steam
```

<figure><img src="../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

* This script is used to launch the game instead of the standard shortcut.

{% hint style="info" %}
If the standard launcher executable fails to apply the affinity mask, the patcher executable can be used instead.
{% endhint %}

### CPU Performance - Checking Results <a href="#h.hsbpvq344s7" id="h.hsbpvq344s7"></a>

To verify that the launch script has successfully applied the CPU affinity:

* Task Manager is opened.
* The `BlackDesert64.exe` process is located in the Details or Processes tab after launching the game.
* The user right-clicks `BlackDesert64.exe` and selects **Set Affinity**.
* Only the designated physical cores should appear as enabled in the configuration window.

<figure><img src="../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>

### CPU Performance - List of Ryzen CPU Affinities <a href="#h.v9tozbpj4fx" id="h.v9tozbpj4fx"></a>

{% hint style="info" %}
If allocating fewer than 4 cores to the game process, reverting the changes and testing custom affinity masks is recommended.
{% endhint %}

{% hint style="info" %}
This guide follows a basic formula for isolating the game process to only physical cores with no simultaneous multi-threading.
{% endhint %}

{% hint style="info" %}
These affinity masks serve as guidelines, and players can adjust them depending on individual system performance.
{% endhint %}

<table><thead><tr><th width="283">CPU</th><th width="297">Core Design</th><th width="675">Affinity for BDO</th></tr></thead><tbody><tr><td><p>Ryzen 3 1200</p><p>Ryzen 3 1300X</p><p>Ryzen 3 2200G(E)</p><p>Ryzen 3 3200G(E)</p></td><td><p>ZEN / ZEN+ 4 core, 4 thread</p><p>2 CCX, 2 cores each</p></td><td><p>Disable: 0, 1</p><p>Enable: 2, 3</p><p>Affinity mask: C</p></td></tr><tr><td><p>Ryzen 5 1400</p><p>Ryzen 5 1500X</p><p>Ryzen 5 2400G(E)</p><p>Ryzen 5 2500X</p><p>Ryzen 5 3400G(E)</p></td><td><p>ZEN / ZEN+ 4 core, 8 thread</p><p>2 CCX, 2 cores each</p></td><td><p>Disable: 0, 1, 2, 3, 5, 7</p><p>Enable: 4, 6</p><p>Affinity mask: 50</p></td></tr><tr><td><p>Ryzen 5 1600(X)</p><p>Ryzen 5 2600(X)</p></td><td><p>ZEN / ZEN+ 6 core, 12 thread</p><p>2 CCX, 3 cores each</p></td><td><p>Disable: 0, 1, 2, 3, 4, 5, 7, 9, 11</p><p>Enable: 6, 8, 10</p><p>Affinity mask: 540</p></td></tr><tr><td><p>Ryzen 7 1700(X)</p><p>Ryzen 7 1800(X)</p><p>Ryzen 7 2700(X)</p></td><td><p>ZEN / ZEN+ 8 core, 16 thread</p><p>2 CCX, 4 cores each</p></td><td><p>Disable: 0, 1, 2, 3, 4, 5, 6, 7, 9, 11, 13, 15</p><p>Enable: 8, 10, 12, 14</p><p>Affinity mask: 5500</p></td></tr><tr><td>Ryzen 5 3500(X)</td><td><p><br>ZEN 2 6 core, 6 thread</p><p>2 CCX, 3 cores each</p></td><td>No change needed.</td></tr><tr><td><p>Ryzen 5 3600(X)</p><p>Ryzen 5 5600X</p></td><td><p>ZEN 2 6 core, 12 thread</p><p>2 CCX, 3 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process.</p><p>Affinity mask: 555</p><p>Enable: 0, 2, 4, 6, 8, 10</p></td></tr><tr><td><p>Ryzen 7 3700(X)</p><p>Ryzen 7 3800X</p></td><td><p>ZEN 2 8 core, 16 thread</p><p>2 CCX, 4 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process. Limit to 6 cores.</p><p>Affinity mask: 5550</p><p>Enable: 4, 6, 8, 10, 12, 14</p></td></tr><tr><td><p>Ryzen 7 5800X</p><p>Ryzen 7 5800X3D</p></td><td><p>ZEN 3 8 core, 16 thread</p><p>1 CCX, 8 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process. Disable core 0 to prevent Windows multitasking from overlapping.</p><p>Affinity mask: 5554</p><p>Enable: 2, 4, 6, 8, 10, 12, 14</p></td></tr><tr><td><p>Ryzen 9 3900(X)</p><p>Ryzen 9 5900X</p></td><td><p>ZEN 2 12 core, 24 thread</p><p>2 CCD, 2 CCX each</p><p>4 CCX total, 3 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process.</p><p>Isolate to one chiplet.</p><p>Affinity mask: 555000 or 555</p><p>Disable: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 13, 15, 17, 19, 21, 23</p><p>Enable: 12, 14, 16, 18, 20, 22</p></td></tr><tr><td><p>Ryzen 9 3950X</p><p>Ryzen 9 5950X</p></td><td><p>Zen 2 16 core, 32 thread</p><p>2 CCD, 2 CCX each</p><p>4 CCX total, 4 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process.</p><p>Isolate to one chiplet. Limit to 6 cores.</p><p>Affinity mask: 5550000 or 5550</p><p>Disable: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 17, 19, 21, 23, 25, 27, 28, 29, 30, 31</p><p>Enable: 16, 18, 20, 22, 24, 26</p></td></tr></tbody></table>

### CPU Performance - Intel <a href="#h.j6lcysu9kjsh" id="h.j6lcysu9kjsh"></a>

* While Intel CPUs do not experience cross-CCD cache latency over AMD's Infinity Fabric, tweaking core affinity can still improve frame rates by up to 25%.
* Performance gains on Intel hardware may vary; tweaks are less consistent than on AMD platforms. If instability occurs, reverting the tweaks is recommended.
* The processor model can be verified on the [Intel Ark Product Specifications](https://ark.intel.com/content/www/us/en/ark.html) database to determine if it supports Hyper-Threading.
  * Generally, i5 processors before the 10th generation did not support hyperthreading. i7 and i9 processors usually do support hyperthreading (except the i7-9700K). After the 10th generation, Intel has hyperthreading on most of its processor line-up.
* The game process must be kept away from efficiency cores (E-cores) on 12th Generation and newer Intel CPUs. Assigning game threads to E-cores reduces performance due to their smaller cache and lower clock speeds.

The table below lists recommended affinity masks for Intel CPUs. Core IDs begin at zero:

| CPU | Affinity for BDO |
| :--- | :--- |
| Older than 12th gen quad core Intel CPU with no hyperthreading: | An upgrade is recommended. |
| Older than 12th gen 6 core Intel CPU with no hyperthreading: | No core affinity changes are applied. |
| Older than 12th gen 8 core Intel CPU with no hyperthreading (i7-9700K): | <p>Limit the process to 6 cores and move away from core 0 where background tasks are often assigned.</p><p>Affinity mask: FC</p><p>Cores 2, 3, 4, 5, 6, 7 enabled.</p> |
| Older than 12th gen Quad core Intel CPU with hyperthreading: | <p>An upgrade is recommended.</p><p>To disable hyperthreading on existing hardware, the following mask is applied.</p><p>Affinity Mask: AA</p><p>Cores 1, 3, 5, 7 enabled.</p> |
| Older than 12th gen 6 core Intel CPU with hyperthreading: | <p>Apply the following to disable hyperthreading.</p><p>Affinity Mask: AAA</p><p>Cores 1, 3, 5, 7, 9, 11 enabled.</p> |
| Older than 12th gen 8+ core Intel CPU with hyperthreading: | <p>Restrict the process to 6 true, physical cores. Move the game process away from core 0.</p><p>Affinity Mask: AAA0</p><p>Cores 5, 7, 9, 11, 13, 15 enabled.</p> |

### RAM Management <a href="#h.2w5xzwbl1s4n" id="h.2w5xzwbl1s4n"></a>

* Windows Memory Compression can be disabled in PowerShell using the command `Disable-MMAgent -mc` to prevent CPU overhead from memory compression.

<figure><img src="../.gitbook/assets/image (346).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The command `Enable-MMAgent -mc` re-enables memory compression. This adjustment is recommended only for systems with 16 GB of RAM or more, and should be avoided on systems with 8 GB or less.
{% endhint %}

In Windows 10, memory standby cache behavior may fail to release unused assets, leading to performance degradation and stuttering.

* The utility [Intelligent Standby List Cleaner (ISLC)](https://www.wagnardsoft.com/forums/viewforum.php?f=18&sid=4d5b94e2dc6066217fbaba786c9ed7e1) can be used to automatically purge the standby list and mitigate cache-related stuttering.

{% hint style="info" %}
This utility may also benefit other memory-intensive applications.
{% endhint %}

* The cleanup threshold is configured based on the system's total RAM capacity.
* Enabling the auto-start setting allows ISLC to run in the background upon system startup.

<figure><img src="../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Placing ISLC in a permanent folder location prevents accidental deletion.
{% endhint %}

* High-performance RAM is highly beneficial for game stability.
  * High memory clock speeds combined with low CAS latency are important, especially on AMD platforms. Utilizing the fastest RAM supported by the motherboard and CPU is recommended.
  * Operating two memory modules enables dual-channel mode, while four modules enable dual-rank mode, both of which improve memory bandwidth.

{% hint style="info" %}
The optimal setup is 32+ GB of RAM using four 8+ GB modules.
{% endhint %}

{% hint style="info" %}
Some RAM modules themselves are dual rank, meaning dual channel + dual rank can be achieved with two modules instead of four.
{% endhint %}

* If the DDR4 RAM operates at 1.2V under its XMP profile, and the case has adequate airflow and RAM heat spreaders, the voltage can be safely increased to 1.35V to achieve higher overclock speeds.

{% hint style="info" %}
If the system fails to boot after a memory overclock, resetting the CMOS restores the motherboard to default settings.
{% endhint %}

{% hint style="warning" %}
This should not be performed if firmware TPM is active and BitLocker drive encryption is enabled.
{% endhint %}

### Minor Tweaks <a href="#h.fy5n4bd1lx1g" id="h.fy5n4bd1lx1g"></a>

**PCI Link State Power Management**

* Control Panel is opened, followed by Hardware & Sound.
* Power Options is selected.
* "Change Plan Settings" is selected for the active power plan.
* "Change Advanced Power Settings" is clicked, and the "PCI Express" section is expanded.
* "Link State Power Management" is set to "Off".

[**Auto Power Options OK**](https://www.wagnardsoft.com/forums/viewforum.php?f=18&sid=4d5b94e2dc6066217fbaba786c9ed7e1)

* This utility automatically switches to power-saving profiles during AFK periods and reverts to high-performance profiles during active gameplay.

{% hint style="warning" %}
Disabling the utility is recommended when performing computationally heavy tasks while AFK, such as video rendering.
{% endhint %}

<figure><img src="../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

#### Disabling the in-game forced post-processing sharpening filter <a href="#disabling-the-in-game-forced-post-processing-sharpening-filter" id="disabling-the-in-game-forced-post-processing-sharpening-filter"></a>

* The directory `Documents\Black Desert` is opened.
* The file `GameOption.txt` is opened in a text editor, and the value next to `PostFilter` is changed from `1` to `0`.
* In the `UserCache` directory, files named `gameVariable.xml` are located inside the unique user ID folders. These files are opened, and all instances of `PostFilter` are changed from `1` to `0`.
  * All matching entries must be set to `0`.

{% hint style="info" %}
Tessellation can also be disabled on High graphics settings and above using the same method to improve frame rates.
{% endhint %}

<figure><img src="../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Enabling the Display Filter setting in-game will undo these changes.
{% endhint %}

### Debloat Windows 10 and Windows 11 <a href="#h.rr1bn3kvwf35" id="h.rr1bn3kvwf35"></a>

Reducing background services and bloatware can yield a 1-5% performance improvement on the same hardware. If the system is used for professional workflows, verifying that these scripts do not interfere with required services is recommended before execution.

[https://github.com/LeDragoX/Win-Debloat-Tools](https://github.com/LeDragoX/Win-Debloat-Tools)

The GitHub repository contains PowerShell scripts bundled with a graphical interface. To run them, the latest release is downloaded, a PowerShell window is opened as an administrator, and external script execution is enabled via the following command:

```
Set-ExecutionPolicy -RemoteSigned
```

The graphical interface is launched using the following command in the administrator PowerShell window:

```
.\Win10ScriptGUI.ps1
```

{% hint style="danger" %}
These scripts contain custom PowerShell code developed by a third party to modify or disable Windows features.
{% endhint %}

{% hint style="info" %}
Creating a system restore point is highly recommended before applying these tweaks.
{% endhint %}

{% hint style="info" %}
These scripts include registry tweaks to optimize bandwidth for gaming, which may improve desync and latency. Restart the PC after running the scripts.
{% endhint %}

### Hardware Accelerated GPU Scheduling (HAGS) <a href="#h.lloj8j4nh7bh" id="h.lloj8j4nh7bh"></a>

The Windows 10/11 debloat script will enable hardware accelerated GPU scheduling, which is supposed to improve GPU performance slightly by having the GPU be responsible for load balancing rather than the CPU handling task delegation.

If active streaming via OBS or video playback on secondary monitors reduces game frame rates under GPU-bound conditions, enabling HAGS can help.

If video playback issues occur on secondary monitors, referring to the Quirks of Windowed Optimizations section is recommended.

<figure><img src="../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>

* The desktop is right-clicked to open **Display Settings**.
* The **Graphics** settings button is clicked at the bottom of the menu.
* The "Change default graphics settings" option is selected.
* The toggle for hardware-accelerated GPU scheduling is enabled.

<figure><img src="../.gitbook/assets/image (351).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If performance issues or video playback anomalies persist, HAGS can be disabled.
{% endhint %}

### CPU Performance - Overclocking <a href="#h.skomf96uq95a" id="h.skomf96uq95a"></a>

Overclocking is an option for improving CPU performance, though it increases heat output, power consumption, and the risk of hardware degradation.

{% hint style="danger" %}
Overclocking the CPU may reduce hardware lifespan if configured incorrectly. <mark style="color:red;">**Caution is advised**</mark>. The MoonBD team assumes no responsibility for hardware damage.
{% endhint %}

{% hint style="warning" %}
This section is intended for experienced users only.
{% endhint %}

If CPU temperatures remain below 85°C (monitored via [HWiNFO](https://www.hwinfo.com/), preferably below 75°C) during consecutive [Cinebench R23](https://apps.microsoft.com/store/detail/cinebench/9PGZKJC81Q7J?hl=en-us) runs, minor overclocking or adjusting processor boost settings can be considered.

{% hint style="info" %}
Undervolting is often more effective for AMD Ryzen and 12th Generation or newer Intel processors to increase boost clocks.
{% endhint %}

{% hint style="info" %}
Testing via consecutive Cinebench runs with no background applications and monitoring with HWiNFO is recommended after making adjustments.
{% endhint %}

{% hint style="info" %}
If system instability occurs or temperatures and power draw exceed safe limits, settings must be reverted.
{% endhint %}

Enabling **Multi-Core Enhancement** (MCE) in the motherboard BIOS allows all CPU cores to boost to maximum single-core frequencies indefinitely, provided cooling capacity is sufficient to prevent thermal throttling. On MSI enthusiast-chipset motherboards, this setting is often enabled by default.

{% hint style="warning" %}
Not recommended on newer CPUs such as Intel 13th Gen or Ryzen 7000 Series which are already targeting such high power and temperature targets.
{% endhint %}

AMD platforms support [Precision Boost Overdrive (PBO)](https://www.amd.com/en/support/kb/faq/cpu-pb2), which can be enabled via the [AMD Ryzen Master](https://www.amd.com/en/technologies/ryzen-master) utility or the BIOS to raise boost power limits within motherboard VRM specifications.

Depending on processor binning, a negative **Vcore offset** (e.g. -50mV to -100mV) can be applied in the BIOS to lower temperatures and allow higher boost frequencies. Setting the offset too low may cause performance regression even if the system remains stable.

The third-party utility [ClockTuner for Ryzen (CTR)](https://www.guru3d.com/articles-pages/clocktuner-for-ryzen-ctr-guide-download,1.html) can automate finding optimal voltage and frequency settings. It requires Ryzen Master and Cinebench to function.

Manual overclocking locks the CPU to maximum frequency at all times, which may increase idle power consumption, though modern architectures still reduce power draw when idle.

Manual overclocking is outside the scope of this guide. Experienced communities can provide guidance on these configurations:

[https://www.overclock.net/forums/](https://www.overclock.net/forums/)

{% hint style="info" %}
Ensuring adequate case cooling and airflow is recommended before applying overclock settings.
{% endhint %}

Overclocking can exceed motherboard Voltage Regulator Module (VRM) power delivery limits. Manual overclocking is not recommended on low-cost motherboards lacking VRM heat sinks.

When manually overclocking, players must ensure CPU power draw does not exceed power supply limits. System power requirements can be estimated via:

[https://outervision.com/power-supply-calculator.](https://outervision.com/power-supply-calculator.)

A power supply capacity 30% higher than the calculated estimate is recommended to account for future upgrades, capacitor aging, and transient power spikes.
