# 🖥️ Performance

{% hint style="danger" %}
Make sure you understand what you're doing before making any changes - we do not take responsibility for any misconfiguration you perform
{% endhint %}

### UI/ Notification Clean-Up <a href="#ui-notification-clean-up" id="ui-notification-clean-up"></a>

* Use the [Edit UI](https://imgur.com/Rg1mIMt) option to customize the game’s user interface.
* Use as few [chat boxes](https://imgur.com/v76jvyI) as possible. Hide any chats you’re not interested in reading.
* Disable [chat scroll animations](https://imgur.com/iebshJB)
* Using the [3D minimap](https://imgur.com/6yw5j7l) greatly improves performance in CPU limited situations by getting rid of all the arrows.
* In the general settings, [Alerts](https://i.imgur.com/O0EYEwz.png) section, disable ALL the in-game alerts unless you really want to see them.
* Using [Mouse Movement](https://i.imgur.com/lWRlQxw.png) can increase your framerate while the mouse is on screen. Not sure why.

### In-game Settings <a href="#in-game-settings" id="in-game-settings"></a>

* [Disable low power mode](https://i.imgur.com/vJgXCtW.png)
  * Low power mode makes the game sleep for about 10ms every frame to use less resources.
  * Only useful if you're on a high end rig and streaming so more resources are available for OBS, or if you want to conserve some power on a laptop.
* If you have a desperately weak GPU, you can use both [Upscale](https://i.imgur.com/zb5mpZa.png) and [Crop Mode](https://i.imgur.com/bNO1woS.png) settings to drastically reduce the render resolution of the game and boost frame rates
* [Attack Decisions](https://i.imgur.com/ISy6GDZ.png) do consume some CPU resources to display. If you're comfortable with BDO combat you can disable them.
* [Effect Optimization](https://i.imgur.com/bMJ0pme.png) slider about 40% from the left as shown in the screenshot will use lower quality effects for other adventurers without hiding them completely. This is critical for maintaining high performance with effects turned on.
  * Combine this with [Remove Faraway Effects](https://i.imgur.com/YSzpZar.png) to clean up unnecessary particles without actually having to hide skill effects from all players.
  * For extreme large scale PvP scenarios or for doing PvE with others, you might choose to temporarily [Remove Others’ Effects](https://i.imgur.com/sjiwABj.png). I don’t recommend it for general gameplay though.
* I don’t use the [Character Optimization](https://i.imgur.com/ifGkFN4.png) setting. I want to see all the characters present during combat, unless at the following:
  * When you're at world bosses like Karanda, Vell, and Garmoth; pressing [Shift + F5](https://imgur.com/Ct0MorX) will toggle hiding other adventurers.
* The game has a [Performance Optimization](https://i.imgur.com/hfb5l9o.png) setting. This setting causes more assets to be kept in RAM. This is good because asset streaming from disk can cause stuttering in some situations.
  * You should have over 16 GB of RAM if you want to enable this setting, and you may want 32 GB or more RAM to get the most benefit from it

### SSD Performance <a href="#ssd-performance" id="ssd-performance"></a>

* If you’re not playing on an SSD, asset streaming can cause significant stutter and you’ll often hit loading walls when riding on a horse.
* An m.2 PCI-e NVMe SSD is best, this will almost completely remove all asset streaming stutter as long as your RAM is good enough.

### Disabling Vertical Sync <a href="#h.74w5a0s9z59u" id="h.74w5a0s9z59u"></a>

Windows 10 v1703 or v1709 you might have a leftover bug that prevented v-sync from being disabled.

Laptops with dual graphics solutions might not be able to disable v-sync.

Disabling fullscreen optimizations in the game’s executable properties sometimes causes you to be unable to disable v-sync in fullscreen, depending on your setup.

**Nvidia**

<figure><img src="../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

In Nvidia’s Control Panel, add a game profile for Black Desert and disable vertical sync.

**AMD**

<figure><img src="../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
In Radeon Settings, enable Radeon Enhanced Sync for the Black Desert game profile, and turn off wait for vertical refresh.
{% endhint %}

#### Disable V-Sync in Windowed Modes <a href="#h.promh3xw4ocr" id="h.promh3xw4ocr"></a>

Right click your desktop and select **Display settings**. From there, scroll to the bottom to the **Graphics** section under **Related settings** and enter that menu. Then select **Change default graphics settings**.

![](https://docs.dusthorizon.com/~gitbook/image?url=https%3A%2F%2F1487308100-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F1ZyNkRpnTmMrdd8zPirl%252Fuploads%252Fgit-blob-af1f9892cfc62a8c92c19742b62158a880e47eb9%252Fpasted%2520image%25200%2520%283%29.png%3Falt%3Dmedia\&width=768\&dpr=3\&quality=100\&sign=13a37254\&sv=2)![](https://docs.dusthorizon.com/~gitbook/image?url=https%3A%2F%2F1487308100-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F1ZyNkRpnTmMrdd8zPirl%252Fuploads%252Fgit-blob-97d1285733e82868520c9109efa38c7d7372a933%252Fpasted%2520image%25200%2520%284%29.png%3Falt%3Dmedia\&width=768\&dpr=3\&quality=100\&sign=5668e208\&sv=2)

From there, you’re going to find Optimizations for windowed games and switch it on. At that point as long as v-sync is disabled in the driver, it will be disabled in windowed mode too.

Having G-Sync on fullscreen only will still enable it in the window when this optimization is enabled due to multiplane overlay support. More info on this in the release notes for Nvidia’s drivers.

### Quirks of Windowed Optimizations <a href="#h.k2x8z6uvzbhn" id="h.k2x8z6uvzbhn"></a>

* If you have Windowed Optimizations on, you may find that you’re still getting capped at around 210 FPS-ish on a 144Hz screen, or 1.5x your refresh rate. The only workaround I’ve noticed for this is to have G SYNC turned on for your system and have a GSYNC or FreeSync compatible display.

<figure><img src="../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure>

* Once you have GSYNC enabled globally, you can disable it for Black Desert specifically in the Nvidia Profile Inspector if it’s causing you troubles with stutter or video playback.

<figure><img src="../.gitbook/assets/image (338).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
The above is required to prevent playback stuttering on Twitch on secondary monitors with the newest Nvidia graphics drivers when the BDO window is in focus, especially when Hardware Accelerated GPU Scheduling is enabled and GPU usage is reaching 100%.
{% endhint %}

* I haven’t further tested this, however on my system I have set the Desktop Windows Manager to use Fast Sync rather than v-sync. I do not know if the DWM respects this setting, however it might help with game fluidity in windowed modes.

<figure><img src="../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Please experiment with this setting. It may benefit you, or it might simply be a placebo. At the very least I haven’t noticed any problems from having this setting changed.
{% endhint %}

### Nvidia Driver Tweaks <a href="#h.gjxrz4o3rug7" id="h.gjxrz4o3rug7"></a>

{% hint style="info" %}
Download [Nvidia Profile Inspector](https://github.com/Orbmu2k/nvidiaProfileInspector/releases) to more easily customize these settings.
{% endhint %}

**Threaded Optimizations**

{% hint style="info" %}
This setting defaults to Auto.
{% endhint %}

* If you have only an older quad core processor with no hyperthreading or are on first-gen Ryzen, turn this setting off to reduce some stutter
* Otherwise for newer 6+ core CPUs you should definitely have this setting turned on for best frame rate.

**Ansel**

* Disable Ansel for slightly less stutter.

**Shader Cache**

* Play around with this setting. Most of the time, having it on is best so there’s no shader compile stutter. But in some situations the shader cache can be slow / jittery to load from disk too so sometimes it’s best to have it off. Find what works best for your setup.

<figure><img src="../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Do the above in the Black Desert profile to avoid interfering with other games.
{% endhint %}

**Power Management Mode**

* Set this to Adaptive.
  * High Performance keeps your GPU at max clock speed. Best for when in game, but when AFKing it drastically increases power consumption.
  * Optimal Performance reduces the clock speed of the GPU as long as you’re getting decent performance, as chosen by the driver. Sometimes stutters last longer as clock speed shifts mid-stutter.
* On newer 30-series GPUs, this can be set to “Prefer maximum performance” in the Nvidia Control Panel. It will still clock down and draw less power when the game is minimized to the system tray.
  * Adaptive sets clock speed high when at load constantly, and when load decreases it lowers the clock speed to consume less power.

<figure><img src="../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Do the above in the Global profile for power mode benefits in all your games!
{% endhint %}

**G-Sync**

G-Sync helps improve responsiveness when your framerates are consistent and below your monitor’s refresh rate. It can also reduce input lag.

{% hint style="warning" %}
It’s up to your preference as to whether you leave G SYNC enabled, as it can reduce input lag but also can make stutters more noticeable.
{% endhint %}

**Ultra Low Latency Mode**

If your processor can handle the extra overhead of giving the GPU the frames it needs as it needs them rather than queueing them ahead asynchronously, you can drastically reduce input lag by enabling Ultra low latency mode in the Nvidia Control Panel for Black Desert.

{% hint style="warning" %}
This setting can cause more stutter when your CPU is not capable of delivering frame requests to your GPU in real-time without queueing
{% endhint %}

<figure><img src="../.gitbook/assets/image (342).png" alt=""><figcaption></figcaption></figure>

### CPU Performance - Set Affinity <a href="#h.rl325eap4pk9" id="h.rl325eap4pk9"></a>

**Let me preface this with a few reasons why BDO has to have CPU optimization tweaked.**

1. BDO doesn’t play well with hyperthreading (HT, Intel) / simultaneous-multi-threading (SMT, AMD). What should probably increase performance instead decreases performance.
2. BDO needs fast access to cache on the processor when in a CPU heavy situation.
3. I’ve noticed odd performance regression over time while playing the game with more than 6 real, true cores allocated to it. Also disable core 0 if you have cores to spare as Windows will prioritize that core on the scheduler when assigning background tasks.
4. We’re using affinity masking to perform the performance tweak in software so that we don’t cause performance loss in other applications. Most applications like having extra threads, so disabling them at the hardware level is bad! BDO is a special case so it gets special treatment.

**To perform the CPU affinity tweak:**

* You’ll have to figure out which cores you want to use using the steps in the previous sections, and then [use this affinity calculator](https://bitsum.com/tools/cpu-affinity-calculator/) to figure out the hexadecimal value of the affinity mask you need to use.

{% hint style="info" %}
Some common CPU Affinities for Ryzen further below.
{% endhint %}

* Then, you’ll want to make a batch file (Windows Command Line script) with the following:

```
cd /d "Your Path To Black Desert"
Start /affinity YourAffinityMask BlackDesertLauncher.exe
```

<figure><img src="../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
This is a screenshot of mine as an example. Your affinity mask will probably be different. Figure out what it is first!
{% endhint %}

* Place the BAT file you just made in your game’s launcher directory so you don’t lose it later, then make a shortcut to it on your desktop.
* Then you’ll have to edit the properties of the shortcut so that you always run the script as an administrator, since you need admin rights to both run the launcher, and to set affinity on it when it’s launching.
* If you use Steam, your Start command should look like this with the -steam switch at the end:

```
cd /d "Your Path To Black Desert"
Start /affinity YourAffinityMask BlackDesertLauncher.exe -steam
```

<figure><img src="../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

* Then just use this script to launch the game instead of the normal shortcut.

{% hint style="info" %}
If using BlackDesertLauncher.exe does not work for you, try using BlackDesertPatcher32.exe in your launch script.
{% endhint %}

### CPU Performance - Checking Results <a href="#h.hsbpvq344s7" id="h.hsbpvq344s7"></a>

To check whether your launch script successfully changed the game’s affinity, do the following:

* Open Task Manager.
* Find BlackDesert64.exe in the Processes tab after you’ve launched the game using the script.
* Right click BlackDesert64.exe and click Set Affinity.
* Only the cores you want to use should be enabled in the visual.

<figure><img src="../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>

### CPU Performance - List of Ryzen CPU Affinities <a href="#h.v9tozbpj4fx" id="h.v9tozbpj4fx"></a>

{% hint style="info" %}
If you’re allocating less than 4 cores / threads to BDO you might want to undo the changes and experiment with your own affinity mask testing.
{% endhint %}

{% hint style="info" %}
This guide follows a basic formula for isolating BDO to only physical cores and with no simultaneous multi-threading.
{% endhint %}

{% hint style="info" %}
Use these affinity masks as guidelines, but experiment with your own if they don’t work out.
{% endhint %}

<table><thead><tr><th width="283">CPU</th><th width="297">Core Design</th><th width="675">Affinity for BDO</th></tr></thead><tbody><tr><td><p>Ryzen 3 1200</p><p>Ryzen 3 1300X</p><p>Ryzen 3 2200G(E)</p><p>Ryzen 3 3200G(E)</p></td><td><p>ZEN / ZEN+ 4 core, 4 thread</p><p>2 CCX, 2 cores each</p></td><td><p>Disable: 0, 1</p><p>Enable: 2, 3</p><p>Affinity mask: C</p></td></tr><tr><td><p>Ryzen 5 1400</p><p>Ryzen 5 1500X</p><p>Ryzen 5 2400G(E)</p><p>Ryzen 5 2500X</p><p>Ryzen 5 3400G(E)</p></td><td><p>ZEN / ZEN+ 4 core, 8 thread</p><p>2 CCX, 2 cores each</p></td><td><p>Disable: 0, 1, 2, 3, 5, 7</p><p>Enable: 4, 6</p><p>Affinity mask: 50</p></td></tr><tr><td><p>Ryzen 5 1600(X)</p><p>Ryzen 5 2600(X)</p></td><td><p>ZEN / ZEN+ 6 core, 12 thread</p><p>2 CCX, 3 cores each</p></td><td><p>Disable: 0, 1, 2, 3, 4, 5, 7, 9, 11</p><p>Enable: 6, 8, 10</p><p>Affinity mask: 540</p></td></tr><tr><td><p>Ryzen 7 1700(X)</p><p>Ryzen 7 1800(X)</p><p>Ryzen 7 2700(X)</p></td><td><p>ZEN / ZEN+ 8 core, 16 thread</p><p>2 CCX, 4 cores each</p></td><td><p>Disable: 0, 1, 2, 3, 4, 5, 6, 7, 9, 11, 13, 15</p><p>Enable: 8, 10, 12, 14</p><p>Affinity mask: 5500</p></td></tr><tr><td>Ryzen 5 3500(X)</td><td><p><br>ZEN 2 6 core, 6 thread</p><p>2 CCX, 3 cores each</p></td><td>No change needed.</td></tr><tr><td><p>Ryzen 5 3600(X)</p><p>Ryzen 5 5600X</p></td><td><p>ZEN 2 6 core, 12 thread</p><p>2 CCX, 3 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process.</p><p>Affinity mask: 555</p><p>Enable: 0, 2, 4, 6, 8, 10</p></td></tr><tr><td><p>Ryzen 7 3700(X)</p><p>Ryzen 7 3800X</p></td><td><p>ZEN 2 8 core, 16 thread</p><p>2 CCX, 4 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process. Limit to 6 cores.</p><p>Affinity mask: 5550</p><p>Enable: 4, 6, 8, 10, 12, 14</p></td></tr><tr><td><p>Ryzen 7 5800X</p><p>Ryzen 7 5800X3D</p></td><td><p>ZEN 3 8 core, 16 thread</p><p>1 CCX, 8 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process. Disable core 0 to prevent Windows multitasking from overlapping.</p><p>Affinity mask: 5554</p><p>Enable: 2, 4, 6, 8, 10, 12, 14</p></td></tr><tr><td><p>Ryzen 9 3900(X)</p><p>Ryzen 9 5900X</p></td><td><p>ZEN 2 12 core, 24 thread</p><p>2 CCD, 2 CCX each</p><p>4 CCX total, 3 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process.</p><p>Isolate to one chiplet.</p><p>Affinity mask: 555000 or 555</p><p>Disable: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 13, 15, 17, 19, 21, 23</p><p>Enable: 12, 14, 16, 18, 20, 22</p></td></tr><tr><td><p>Ryzen 9 3950X</p><p>Ryzen 9 5950X</p></td><td><p>Zen 2 16 core, 32 thread</p><p>2 CCD, 2 CCX each</p><p>4 CCX total, 4 cores each</p></td><td><p>Disable SMT for BlackDesert64.exe process.</p><p>Isolate to one chiplet. Limit to 6 cores.</p><p>Affinity mask: 5550000 or 5550</p><p>Disable: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 17, 19, 21, 23, 25, 27, 28, 29, 30, 31</p><p>Enable: 16, 18, 20, 22, 24, 26</p></td></tr></tbody></table>

### CPU Performance - Intel <a href="#h.j6lcysu9kjsh" id="h.j6lcysu9kjsh"></a>

* Intel CPUs don’t suffer from cross-CCD/CCX cache access latency over Infinity Fabric. You can still get a 25%+ increase in performance by tweaking core affinity on Intel.
* That said, your mileage may vary by tweaking CPU affinity on Intel, it’s not as consistent of a performance improvement as it is with AMD depending on which CPU you’re using. If you get more instability or worse performance, remove any CPU tweaking you’ve done and try again.
* Search for your processor’s model from [Intel Ark Product Specifications](https://ark.intel.com/content/www/us/en/ark.html) and determine whether your Intel processor supports hyper-threading or not.
  * Generally, i5 processors before the 10th generation didn’t support hyperthreading. i7 and i9 processors usually do support hyperthreading (except the i7-9700K). After the 10th generation, Intel has hyperthreading on most of its processor line-up.
* Keep BDO away from efficiency cores on 12th Gen Intel. If a thread from BDO gets assigned to an e-core, your performance will suffer as those cores have much less cache and are clocked much slower.

As a general rule of thumb regarding which affinity masks you should use for your BDO launch script. Note that cores IDs count up from zero:

| CPU                                                                     | Affinity for BDO                                                                                                                                                                                                   |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Older than 12th gen quad core Intel CPU with no hyperthreading:         | Purchase an upgrade when possible.                                                                                                                                                                                 |
| Older than 12th gen 6 core Intel CPU with no hyperthreading:            | Do not apply any core affinity changes.                                                                                                                                                                            |
| Older than 12th gen 8 core Intel CPU with no hyperthreading (i7-9700K): | <p>Limit the BDO process to 6 cores and move away from core 0 where background tasks are often assigned.</p><p>Affinity mask: FC</p><p>Cores 2, 3, 4, 5, 6, 7 enabled.</p>                                         |
| Older than 12th gen Quad core Intel CPU with hyperthreading:            | <p>Purchase an upgrade if you can afford it.</p><p>If you can’t afford or are waiting for your upgrade, apply the following to disable hyperthreading.</p><p>Affinity Mask: AA</p><p>Cores 1, 3, 5, 7 enabled.</p> |
| Older than 12th gen 6 core Intel CPU with hyperthreading:               | <p>Apply the following to disable hyperthreading.</p><p>Affinity Mask: AAA</p><p>Cores 1, 3, 5, 7, 9, 11 enabled.</p>                                                                                              |
| Older than 12th gen 8+ core Intel CPU with hyperthreading:              | <p>Restrict the BDO process to 6 true, physical cores. Move the game process away from core 0.</p><p>Affinity Mask: AAA0</p><p>Cores 5, 7, 9, 11, 13, 15 enabled.</p>                                              |

### RAM Management <a href="#h.2w5xzwbl1s4n" id="h.2w5xzwbl1s4n"></a>

* Disable Windows Memory Compression in PowerShell with the command Disable-MMAgent -mc to stop your processor from compressing memory and causing CPU overhead.

<figure><img src="../.gitbook/assets/image (346).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
You can do Enable-MMAgent -mc to re-enable memory compression if you need to. Only do this with 16 GB of RAM or higher. If your computer has only 8 GB don’t do this.
{% endhint %}

To preface this next bit, in Windows 10, there is a memory leak causing Windows not to release assets in standby in memory when they are no longer needed. That's why it causes stuttering.

* Download [Intelligent Standby List Cleaner](https://www.wagnardsoft.com/forums/viewforum.php?f=18\&sid=4d5b94e2dc6066217fbaba786c9ed7e1) (check the Announcements section of the forum for the most recent release of ISLC) to clean up memory leaks BDO has that cause extreme stutter once the standby cache has been filled.

{% hint style="info" %}
This may help with other applications as well since Windows 10 does a pretty bad job of cleaning up the standby cache.
{% endhint %}

* Set it to clean up the list at a threshold suitable for your system’s RAM capacity. You’ll have to do some playing around to figure that out on your own.
* Enable auto start so that ISLC runs in the background as soon as you turn on your PC.

<figure><img src="../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Make sure you put ISLC in a folder location you won’t accidentally delete it. from.
{% endhint %}

* You want your RAM hardware to be as performant as possible if you’re building your own system to play BDO on.
  * High memory clock speeds with low CAS latency is important, especially on an AMD platform. Get the fastest RAM your motherboard and CPU can support that is within your budget.
  * Using 2 RAM sticks enables dual channel and provides more performance than using one module, and using 4 RAM sticks enables dual rank and provides more performance than using 2 modules.

{% hint style="info" %}
The optimal setup for BDO is 32+ GB of RAM using four 8+ GB modules.
{% endhint %}

{% hint style="info" %}
Some RAM modules themselves are dual rank, meaning you can have dual channel + dual rank with two modules instead of 4.
{% endhint %}

* If your DDR4 RAM uses 1.2v for its XMP profile and you have good case airflow and your RAM has a decent heat spreader, you can safely push the voltage to 1.35v and get higher speeds than stock XMP.

{% hint style="info" %}
If your computer won’t boot after a RAM overclock, you will need to reset CMOS to get your motherboard back to stock settings, then try again
{% endhint %}

{% hint style="warning" %}
Don’t do this if you’re using firmware TPM and have Bitlocker drive encryption enabled by the way
{% endhint %}

### Minor Tweaks <a href="#h.fy5n4bd1lx1g" id="h.fy5n4bd1lx1g"></a>

**PCI Link State Power Management**

* Go to your control panel, click on Hardware & Sound
* Power settings (for category view) or Control Panel
* Power options (for icon view) Select "Change Plan Settings"
* Click on "Change Advanced Power Settings" Expand "PCI Express"
* "Link State Power Management" and change that setting to "Off".

[**Auto Power Options OK**](https://www.wagnardsoft.com/forums/viewforum.php?f=18\&sid=4d5b94e2dc6066217fbaba786c9ed7e1)

* This free software is really useful for automatically switching to power saving profiles when you’re AFK, and then switching back on its own to high performance power profiles when you’re playing actively.

{% hint style="warning" %}
Just remember to disable it if you have to do something computationally heavy while AFK such as rendering a video.
{% endhint %}

<figure><img src="../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

#### Disabling the in-game forced post-processing sharpening filter <a href="#disabling-the-in-game-forced-post-processing-sharpening-filter" id="disabling-the-in-game-forced-post-processing-sharpening-filter"></a>

* Go to Documents\Black Desert folder.
* Open the GameOption.txt in Notepad, next to PostFilter where there's a 1 it should be a 0.
* Then also in UserCache there's a couple folders. One uses a 6 digit number unique to you, the other uses a 7 digit number unique to you. In both there's a gameVariable.xml file. You need to open it in Notepad or an XML editor and again anywhere you see PostFilter change the 1 to a 0.
  * There are multiple entries for the different settings. You have to set them all to 0.

{% hint style="info" %}
You can also disable Tessellation on High settings and above with the same method, which might give you more FPS. You'll see it there along with PostFilter.
{% endhint %}

<figure><img src="../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Enabling the Display Filter setting in game will undo these changes, so be careful.
{% endhint %}

### Debloat Windows 10 and Windows 11 <a href="#h.rr1bn3kvwf35" id="h.rr1bn3kvwf35"></a>

You should be able to get 1-5% or even more performance out of BDO on the same hardware if you reduce the amount of bloat and background services on your computer. If you use your PC for more than just gaming, you may want to ensure that the scripts do not interfere with your workflow first before applying them, or just simply not use them.

[https://github.com/LeDragoX/Win-Debloat-Tools](https://github.com/LeDragoX/Win-Debloat-Tools)

The above GitHub link contains a plethora of PowerShell scripts that are bundled with a GUI that you can run to automate their use. Just download the most recent release, run the command prompt to open a PowerShell window, and ensure you can run external scripts by executing the following command as an admin:

```
Set-ExecutionPolicy -RemoteSigned
```

Then launch the GUI interface by doing the following command assuming you already ran the OpenTerminalHere.cmd batch script to open an admin PowerShell window.

```
.\Win10ScriptGUI.ps1
```

{% hint style="danger" %}
These scripts are custom PowerShell code that is used to modify or disable core features of Windows 10 and Windows 11, developed by a third party.
{% endhint %}

{% hint style="info" %}
Highly recommend(!!) you [create a system restore point](https://www.windowscentral.com/how-use-system-restore-windows-11) or confirm that a recent one exists before you apply these tweaks.
{% endhint %}

{% hint style="info" %}
These scripts include registry tweaks to optimize bandwidth for gaming, which may improve desync and latency. Restart your PC after running the scripts.
{% endhint %}

### Hardware Accelerated GPU Scheduling (HAGS) <a href="#h.lloj8j4nh7bh" id="h.lloj8j4nh7bh"></a>

The Windows 10/11 debloat script will enable hardware accelerated GPU scheduling, which is supposed to improve GPU performance slightly by having the GPU be responsible for load balancing rather than the CPU handling task delegation.

If you find that having OBS open reduces your framerate by a huge amount when GPU limited, or your FPS suffers when you’re watching videos on Twitch or YouTube, enable HAGS.

You might run into troubles with video playback on secondary monitors, but if that happens I recommend you go back earlier in this guide and look at the Quirks of Windowed Optimizations chapter

<figure><img src="../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>

* Right click your desktop and open **Display Settings**.
* Scroll to the bottom of the settings menu and click the **Graphics** button
* Click on the option at the top to change **default graphics settings.**
* Enable hardware-accelerated GPU schedules.

<figure><img src="../.gitbook/assets/image (351).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you’re still having problems with video playback, or poor performance in the situations that are meaningful to you, then disable HAGS
{% endhint %}

### CPU Performance - Overclocking <a href="#h.skomf96uq95a" id="h.skomf96uq95a"></a>

Of course, overclocking is an option for improving CPU performance for BDO. However it comes at a risk of increased heat output and power consumption, and a risk of killing or reducing the lifespan of your hardware if you don’t know what you’re doing.

{% hint style="danger" %}
Overclocking your CPU may reduce the lifespan of your computer if done incorrectly. <mark style="color:$danger;">You have been warned</mark>. We take no responsibility if you burn up your hardware.
{% endhint %}

{% hint style="warning" %}
Avoid this section if you don’t know what you’re doing.
{% endhint %}

If you can keep your processor below 85 Celsius (monitored with [HWInfo](https://www.hwinfo.com/), preferably below 75 Celsius) when running back to back to back [Cinebench R23](https://apps.microsoft.com/store/detail/cinebench/9PGZKJC81Q7J?hl=en-us) benchmark tests, you’re probably okay to overclock by a little bit OR apply the following tweaks to the way your processor automatically boosts its frequencies.

{% hint style="info" %}
If you can undervolt the AMD Ryzen 7th gen and Intel 12th+, they will boost further. Otherwise, don't bother trying to overclock them.
{% endhint %}

{% hint style="info" %}
Always test with Cinebench back to back runs with no background applications running while monitoring with HWInfo after changing any settings.
{% endhint %}

{% hint style="info" %}
If you’re not comfortable with the temperature reached or power consumption, or your system becomes unstable, reduce or revert your changes.
{% endhint %}

Enabling **Multi Core Enhancement** in your motherboard BIOS (refer to your motherboard manual) can allow all cores to boost at the max speed that is allowed for single-core boosting, and for an indefinite duration as long as cooling is sufficient so you don’t thermally throttle. **If you’re using an MSI motherboard on an enthusiast chipset, this setting is enabled by default**. This tweak works even for non-K overclockable Intel CPUs on capable motherboards.

{% hint style="warning" %}
Not recommended on newer CPUs such as Intel 13th Gen or Ryzen 7000 Series which are already targeting such high power and temperature targets.
{% endhint %}

AMD has a setting called [Precision Boost Overdrive](https://www.amd.com/en/support/kb/faq/cpu-pb2) which you can enable in the [Ryzen Master](https://www.amd.com/en/technologies/ryzen-master) utility, or in your motherboard BIOS. This replaces the boost power limits that are imposed on your processor by the manufacturer with boost limits from your motherboard manufacturer rated for the maximum power their motherboard VRMs can output

Depending on your individual CPU’s binning level, you may be able to set a **vcore offset** of -50mV or -100mV in your motherboard BIOS after applying PBO to achieve the same clock speeds at a lower voltage, and in some cases allow PBO to boost your CPU to even higher frequencies. Be careful though, in some cases there is performance regression if you set the voltage offset too low even if your system remains stable without crashing.

AMD also has a third party automatic overclocking tool developed by 1USMUS called [ClockTuner](https://www.guru3d.com/articles-pages/clocktuner-for-ryzen-ctr-guide-download,1.html) which will find your best overclock settings for your specific chip and will inform you as to how well binned your sample is. It requires Ryzen Master and Cinebench to function.

If you manually overclock your CPU or use ClockTuner, unless you perform P-state overclocking which is much more complicated and not covered in this guide, your CPU will be locked to its maximum frequency at all times. This may increase power consumption when idle (although AMD’s instant 1ns frequency response on Ryzen 3000 series CPUs and newer still allows the effective clock to drop and power consumption to decrease at idle even when manually set to a specific frequency).

I’m not going to cover manual overclocking in this guide at all. If you’d like to consider it I recommend you seek the advice of experienced overclockers over at:

[https://www.overclock.net/forums/](https://www.overclock.net/forums/)

{% hint style="info" %}
Make sure you have good cooling and awesome airflow in your computer case before you enable these settings or manually overclock.
{% endhint %}

Keep in mind you might go beyond the abilities of your motherboard’s voltage regulator modules (VRM) if you manually overclock. I don’t recommend manually overclocking if you’re using a super cheap motherboard with not even a heat spreader over the VRMs, or high quality VRM power phases. Experts at overclock.net will be able to tell you more if you provide them information about your specific motherboard, cooling, and processor.

If manually overclocking, you may want to make sure your vcore and frequency settings do not cause your CPU’s power consumption to exceed your power supply’s capabilities. You can get an estimate of your computer’s power consumption at:

[https://outervision.com/power-supply-calculator.](https://outervision.com/power-supply-calculator.)

Keep in mind you may want a power supply that can supply 30% more watts than is shown in the calculator for future upgrades, covering for power supply degradation over time, or dealing with momentary spikes in power draw. A hotter CPU has more resistance and thus consumes more power than if it were cooler, even at the same voltage and frequency, by the way.
