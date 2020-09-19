<img src=".github/mLogo.png" width="150" height="150" align="left"></img>

<h1>PreMiD <code>--linux</code></h1>
Discord Rich Presence for web services!
<br><br>

## Table of Contents

- **[About](#about)**
  - [Stats](#stats)
  - [Requirements](#requirements)
  - Examples (soon)
  - FAQs (soon)
  - Building (soon)
  - [Support](#support)
  - [Credits](#credits)
  - [License](#license)
- **[Snapcraft](#snapcraft)** (TL;DR : _never_ ™️)
- **[Portable AppImage](#appimage)** (_RECOMMENDED_)
  - [Installation instructions](#appimageinstall)
  - [Additional notes](#appimagenotes)
- **Red Hat Enterprise Linux (RHEL) based distributions** (soon, use [this](#appimage) for now)
- **Debian and Ubuntu based distributions** (soon, use [this](#appimage) for now)
- **[Arch Linux based distributions](#arch)**
  - [Installation instructions](#archinstall)
  - [Additional notes](#archnotes)
- **[Gentoo Linux](#gentoo)**
  - [Installation instructions](#gentooinstall)
  - [Additional notes](#gentoonotes)

<a name="about"></a>

## About

**PreMiD** is a simple, configurable utility that uses Discord's RP ( Rich Presence ) library which allows you to show what you're doing on the web ( and a few programs ) in your Discord profile as **playing status**.

<a name="stats"></a>

### Stats

<table>
  <tr>
    <th>Deployment</th>
    <th>Total downloads</th>
    <th>Latest release</th>
  </tr>
  <tr>
    <td><a href="https://github.com/doomlerd/LinuxUpdater/actions"><img src="https://github.com/doomlerd/LinuxUpdater/workflows/CI/badge.svg?branch=master&event=push" alt="CI"></a></td>
    <td><a href="https://github.com/doomlerd/LinuxUpdater/releases"><img src="https://img.shields.io/github/downloads/doomlerd/LinuxUpdater/total.svg?maxAge=86400" alt="All releases"></a></td>
    <td><a href="https://github.com/doomlerd/LinuxUpdater/releases/latest"><img src="https://img.shields.io/github/v/release/doomlerd/LinuxUpdater.svg?maxAge=86400" alt="Latest release"><br><img src="https://img.shields.io/github/downloads/doomlerd/LinuxUpdater/latest/total.svg?maxAge=86400" alt="Github releases"></a></td>
  </tr>
</table>

<a name="requirements"></a>

### Requirements

Technically every distribution that can run Discord's [official](https://discordapp.com/download) **app** ( not the web or the snap version ) can run PreMiD too;</br>
As you may have noticed in the recent years, some Linux distributions started dropping support for the 32-bit (ia32/i686/i386/x86) architectures, and as a result, we did too. You can, however, try to build the app yourself if you desperately need to use it on a 32-bit distribution.</br>
Since we currently use Electron as an engine (Discord does too!), its requirements also apply to this app :

- Ubuntu ≥ 12.04
- Fedora ≥ 21
- Debian ≥ 8

It is unknown whether older versions of other distributions support it, so just keep your distribution updated and use **LTS (Long-Term Support)** releases if your distribution offers them, as they're more stable (avoid alpha releases).

<a name="support"></a>

### Support

<div>
  <a target="_blank" href="https://discord.gg/WvfVZ8T" title="Join our Discord!">
    <img height="75px" draggable="false" src="https://discordapp.com/api/guilds/493130730549805057/widget.png?style=banner2" alt="Join our Discord!">
  </a>
</div>

<a name="credits"></a>

### Credits

Thanks to :

- @nattadasu, @Rubensei, @Cairo2k18, zany130, Immanuel D, Friskytrash, Alexandre (and few other guys whom I forgot their names) for providing feedback on nightly releases.
- @apriluwu for maintaining the Gentoo builds
- @SlimShadyIAm and naka for formerly maintaining the Arch User Repository packages
- The Electron community for various packages
- Anyone else who has ever contributed to the project in any way.

<a name="license"></a>

### License

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FPreMiD%2FLinux.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FPreMiD%2FLinux?ref=badge_large)

<img src=".github/snapcraft.png" width="100" height="100" align="right"></img>
<a name="snapcraft"></a>

## Snapcraft

Probably never, since Snap's nature blocks PreMiD from reaching Discord and the extension properly,</br>
It would be appreciated if someone could do it though, any ideas or PRs are welcome.</br>
P.S.: classic confinement doesn't work either so don't bother making a suggestion about it.

<img src=".github/appimage.png" width="100" height="100" align="right"></img>
<a name="appimage"></a>

## Portable AppImage

The AppImage package is the recommended one if Discord works for you but other PreMiD packages (.deb, .rpm, etc) don't.

<a name="appimageinstall"></a>

### Installation instructions

```bash
wget https://github.com/doomlerd/LinuxUpdater/releases/latest/download/PreMiD-Portable.AppImage && chmod a+x PreMiD*.AppImage
```

```bash
# Just double-click it or run
./PreMiD*.AppImage
```

<a name="appimagenotes"></a>

### Additional notes

Either if you want to try PreMiD or just don't want to install it, this one's the best, it's always up to date but _DOESN'T AUTO-START WITH THE SYSTEM!_</br>If you get tired of having to open it each time, use the other packages (according to your distribution).

<a name="arch"></a>
<img src=".github/iusearchbtw.svg" width="100" height="100" align="right"></img>

## Arch Linux based distributions

Uses [Arch User Repository](https://aur.archlinux.org/packages/premid);</br>
Supported distributions are _itself_, Manjaro, Anarchy, Artix, Arco, ArchLabs, Endeavour, Archman, BlackArch, Liri OS and [every one that supports installing from AUR](https://wiki.archlinux.org/index.php/Arch-based_distributions#Active).

<a name="archinstall"></a>

### Installation instructions

```bash
# Using yay (recommended)
yay -S premid
```

```bash
# Using pakku
pakku -S premid
```

```bash
# Using trizen
trizen -S premid
```

```bash
# Using pacaur
pacaur -S premid
```

```bash
# ... you get the point
```

or manually from the [Arch User Repository](https://aur.archlinux.org/packages/premid) if you know what you're doing.

<a name="archnotes"></a>

### Additional notes

If your distro uses pacman, then you have to install one of the helpers first. If you don't have any, Yay is recommended, run :

```bash
git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
```

```bash
yay -S premid
```

Other AUR/Pacman helpers work as well, although each one's functionality is different so you may face issues while using them.

<img src=".github/gentoo.svg" width="100" height="100" align="right"></img>
<a name="gentoo"></a>

## Gentoo Linux

Same applies to its derivatives, such as ColverOS, Clip-OS, Sabayon, Bicom Systems PBXware, [etc](https://wiki.gentoo.org/wiki/Distributions_based_on_Gentoo#Active_projects).

<a name="gentooinstall"></a>

### Installation instructions

```bash
# Add the overlay using layman
layman -S && layman -a apriluwu
```

```bash
# Install via portage
emerge -av app-misc/premid
```

<a name="gentoonotes"></a>

### Additional notes

The shown install command uses layman, it is in the official repositories through `app-portage/layman`.<br>
To get updates you will have to sync the overlay from time to time, you can do this with

```bash
layman -S
```
