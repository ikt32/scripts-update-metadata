# FAQ and troubleshooting
{:.no_toc}

* A markdown unordered list which will be replaced with the ToC
{:toc}

## Access, license and subscription

### Q: Where can I get your scripts?

They're available [through my Patreon](https://patreon.com/ikt){:target="_blank"}. The "how does this work"
is explained in the Supporter tier membership and in the [readme of License Generator](licgen-readme){:target="_blank"}.
Please thoroughly read it.

My Patreon-exclusive scripts are updated versions of:

* [Manual Transmission](5-gears-readme){:target="_blank"}
* [Custom Gear Ratios](5-cgr-readme){:target="_blank"}
* [Custom Torque Map](5-ctm-readme){:target="_blank"}
* [TurboFix](5-turbofix-readme){:target="_blank"}

These all use the same license system.

### Q: Can I pay once for your scripts?

Yes, the license you generate *while subscribed* is valid for *however long you use your PC in its current form*.
After verifying that everything is up and running, you may terminate the subscription. If you need to create
a new license (e.g. after a PC upgrade), you *will* need to re-subscribe to re-run the license generator.

[Please read this for the full details](licgen-readme).

### Q: Do I need to create a new license for updates?

No. Updates are free once you already have a license. I do not expect to have to bump versions for my GTA V scripts,
unless some major unfortunate event happens where I need to do this.

If a major change is happening and a new version of the license is needed, this will be clearly communicated on Patreon.

**The current version of license used by all scripts is `0.0.lic`**

For upcoming games, once I can start work on creating mods for those, I will probably require a new, different license.

### Q: How do I properly activate the scripts after subscribing to Patreon?

1. [Read the readme of License Generator](licgen-readme){:target="_blank"}
2. [Download the latest version of License Generator through the Patreon welcome note](https://www.patreon.com/ikt/membership){:target="_blank"}
3. [Run the License Generator as per the instructions in its readme](licgen-readme){:target="_blank"}
4. Once the license is generated, you can run the game and the scripts automatically pick up the license.

### Q: Can I try the scripts before getting a Patreon subscription?

[Manual Transmission 5.7.0 and newer](https://github.com/ikt32/scripts-updates/releases?q=%22Manual+Transmission%22){:target="_blank"}
contains a Demo mode if it does not detect a license on your system.

This demo runs for 15 minutes before disabling itself, and can be activated 4 times per game session.
It enables the full script, so you can set up your wheel and have a test drive around Los Santos.

Other scripts do not have a demo mode, but their readme documents should explain the full extent of what they do.

## License Generator troubleshooting

### Q: License Generator claims it's not authorized

Or keeps loading after allowing in Patreon.

This likely means License Generator cannot connect to Patreon.
Please verify that License Generator can get a connection to Patreon:

* If you need to access Patreon through a VPN, License Generator will *not* work out of the box.
  You may try a system-wide VPN, but I give *zero* guarantees that such a thing will work.
* Verify that License Generator is allowed through your firewall.
* Verify that the port (8080) used by License Generator is not used by another application.
* Try allowing Patreon with another browser.

If problems persist, please join my Discord server and DM me log files (located in `%localappdata%\ikt\License`).

### Q: Antivirus software claims License Generator is malicious?

This should be a false positive. While I'm not disclosing the source for obvious reasons, I can be transparent about
what it does:

The license generator:

1. checks with Patreon if you're eligible,
2. takes notes of the system it's running on for the license data,
3. generates the license and encrypts it

A combination of the unsigned executable, network communication, system profiling and encryption may trigger some
anti-virus software or cause firewalls to block the application. You can safely unblock it, I have no interest
in messing up your computer.

## Compatibility

### Q: Do the latest versions of your scripts on Patreon work with the latest game update?

As of writing, yes. The latest tested game update is **1.0.3411.0** and all released scripts work with it.

### Q: Why does steering not work in Manual Transmission? / Why does script X behave weirdly?

The following other scripts don't work for game version 1.0.3095.0 and newer, and have been updated on Patreon:

* Manual Transmission **5.6.1 and older**
* Custom Gear Ratios **1.2.0 and older**
* TurboFix **2.3.0 and older**
* Custom Torque Map **1.0.2 and older**

These scripts are **not** compatible with game versions 1.0.3095.0 and newer and using them will cause symptoms such
as:

* Broken steering
* Broken shifting and reversing
* Mismatching gears
* No extra boost

You can downgrade the game to 1.0.3028.0 and older to continue playing with these outdated scripts, or you
can subscribe to [Patreon](https://www.patreon.com/ikt){:target="_blank"} and use the updated versions.

The following script versions **are compatible** for game version **1.0.3095.0**:

* Manual Transmission **5.6.2 and newer**
* Custom Gear Ratios **1.2.1 and newer**
* TurboFix **2.4.0 and newer**
* Custom Torque Map **1.1.0 and newer**

These new versions are exclusive to [Patreon](https://www.patreon.com/ikt){:target="_blank"}. They are kept up-to-date
as Rockstar releases game updates.

### Q: Does Manual Transmission work with my wheel?

Steering wheel support works for *any* wheel that supports DirectInput! Any *device* that supports DirectInput
can be mapped as any input. My personal setup:

* Fanatec CSL DD
* Fanatec CSL LC Pedals (separately connected)
* [SHH Shifter](https://www.shiftershh.com/en/){:target="_blank"}
* A random AliExpress handbrake

Ensure your wheel drivers are installed and up-to-date, and that no other application can take force feedback priority
from GTA V with the script running.

If you'd like to try things out beforehand,
[Manual Transmission contains a demo mode](https://www.patreon.com/posts/manual-5-7-0-119318684){:target="_blank"}
starting with version 5.7.0.

### Q: Why doesn't Manual Transmission see my wheel?

Please check [the Manual Transmission readme](5-gears-readme#steering-wheel-issues). Possible causes:

* No inputs mapped yet: You need to assign the inputs, the script does **not come with defaults**.
  A more user-friendly initial setup is planned for a future update.
* Drivers: Make sure your wheel drivers are installed and your wheel is picked up by games.
* Driver changes: Sometimes driver updates may re-assign GUIDs and the script doesn't recognize the wheel anymore.
  This is addressed in Manual Transmission 5.7.0 and up.
* Software conflicts: Some software may take priority over the wheel instead of GTA V. Make sure nothing like XInput
  or Steam controller also has the wheel assigned.

### Q: Are the scripts compatible with FiveM?

Sort of:

* The scripts are made with only single-player story in mind
* Only scripts marked as FiveM-compatible through `FX_ASI_BUILD` resources will work in FiveM
  * Manual Transmission
  * Custom Torque Map
  * TurboFix and Custom Gear Ratios will have this added somewhere in the future, but currently won't work with FiveM
* Scripts will only work on FiveM if the server allows client-side plugins
  * Most servers will not allow client-side plugins, as such scripts can give you an unfair advantage

**Usage of these scripts in combination with FiveM is at your own risk and no support is given!**
Before usage on FiveM, ensure the scripts work in vanilla single-player story mode. If scripts work in SP, but not
on FiveM, there is nothing I can do to help you.

If you're a server owner and interested in a server-side solution for drivetrain simulation, I highly recommend
[C.H.A.S.E.R](https://legacydmc.net/chaser/) by LegacyDMC.

I'm not aware of any worthwhile steering wheel support solutions for FiveM, which replace GTA V's steering system
with their own, and use real data from the wheels in GTA V to generate force feedback.

## Other

### Q: How do I install mods?

For general information on getting started with mods for GTA V, please check the
[GTA5-Mods Wiki with guides](https://github.com/5mods/tutorials/wiki){:target="_blank"} or ask around on the
[GTA5-Mods Discord server](https://discord.gg/2PR7aMzD4U).

**No support will be given for general modding** and it is expected of you to be competent with
computers and modding in general before trying my scripts.

### Q: Where are the camera options in Manual Transmission?

It's been split off into the (free) standalone
[Dynamic Vehicle First Person Camera](https://www.gta5-mods.com/scripts/dynamic-vehicle-first-person){:target="_blank"}
script.

### Q: Are your scripts affiliated with Rockstar Games or Take-Two Interactive?

No, my scripts are completely independent and are not affiliated with, endorsed by, or sponsored by Rockstar Games, Take-Two Interactive, or any of their subsidiaries. All trademarks, including "Grand Theft Auto V" and "GTA V," are the property of their respective owners. These scripts do not contain any original Rockstar assets, files, or intellectual property. Any references to the game are purely for descriptive purposes.

## Remarks

If you have anything to add to this FAQ, please feel free to reach out via Discord. This FAQ is continously updated
as new questions come in.
