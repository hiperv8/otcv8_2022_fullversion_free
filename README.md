# WHY AM I AVAILABLE FOR FREE?
A while ago, a person called me on discord promising me access to the otcv8 github for a lower amount than what is on the site... the person who offered me sent me photos and showed me by video call that he really had access and could you give me access.

I really wanted to contribute to the otcv8 developers and had plans to create my own server... but after I paid the person just downloaded the repository, sent it to me and disappeared.

I'm making it available because I didn't get what I paid for, I know I already had several versions leaked before but I wanted, in addition to having access to v8, to contribute to the community... but instead I took a hit... I don't know who the person is who gave me the blow, based on information from friends, the only thing I found out is that the person is a lawyer in Brazil and has an rpg project, but I don't know the name.

I paid for cryptocurrency so I know this cannot be reversed, so here's my outrage and frustration.

# DOWNLOAD NOW FOR FREE:
- **ZIP compressed version:** https://mega.nz/file/CERXVIya#xyl7WzoYvjdsNRZQxZZGOwN9n7sopwIWYcqkVgjaKTY
- **Version with free files:**  https://mega.nz/folder/vVRyVQ7I#uTnoJf9OYQLLojl65RZeJQ

# OTClientV8 - 2022 full version free download

OTClientV8 is highly optimized, cross-platform tile based 2d game engine built with c++17, lua, physfs, OpenGL ES 2.0 and OpenAL. It has been created as alternative client for game called Tibia, but now it's much more functional and powerful. It works well even on 12 years old computers. In April 2021 it reached 290k unique installations, including 80k android installations.

Supported platforms:
- Windows (min. Windows 7, requires https://aka.ms/vs/16/release/vc_redist.x86.exe)
- Android (min. 5.0)
- Linux
- Mac Os (requires https://www.xquartz.org/)

**Forum:** http://otclient.net
**Discord:** https://discord.gg/feySup6
**Website:** http://otclient.ovh
**Wiki:** https://github.com/OTCv8/otclientv8/wiki

# FEATURES
- Rewritten and optimized rendering (60 fps on 11 years old computer)
- Better DirectX9 and DirectX11 support
- Adaptive rendering (automated graphics optimizations)
- Rewritten and optimized light rendering
- Rewritten path finding and auto walking
- Rewritten walking system with animations
- HTTP/HTTPS lua API with JSON support
- WebSocket lua API
- Auto updater with failsafe (recovery) mode
- New filesystem
- File encryption and compression
- Automatic diagnostic system
- Refreshed interface
- New crash and error handler
- New HTTP login protocol
- Ingame shop
- Updated hotkey manager
- Updated and optimized battle list
- Crosshair, floor fading, extra health/mana bars and panels
- Much more client options
- Removed a lot of useless and outdated things
- Advanced bot
- Linux version
- Full tibia 11.00 support
- Layouts
- New login server (with ingame account and character creation)
- Support for proxies to lower latency and protect against DDoS
- Bot protection

# Quick Start for players
Download whole repository and run one of binary file.

# Quick Start for server owners
Open init.lua and edit:
```
-- CONFIG
APP_NAME = "otclientv8" -- important, change it, it's name for config dir and files in appdata
APP_VERSION = 1337      -- client version for updater and login to indentify outdated client
DEFAULT_LAYOUT = "retro"

-- If you don't use updater or other service, set it to updater = ""
Services = {
  website = "http://otclient.ovh", -- currently not used
  updater = "http://otclient.ovh/api/updater.php",
  news = "http://otclient.ovh/api/news.php",
  stats = "",
  crash = "http://otclient.ovh/api/crash.php",
  feedback = "http://otclient.ovh/api/feedback.php"
}

-- Servers accept http login url or ip:port:version
Servers = {
  OTClientV8 = "http://otclient.ovh/api/login.php",
  OTClientV8proxy = "http://otclient.ovh/api/login.php?proxy=1",
  OTClientV8classic = "otclient.ovh:7171:1099",
  OTClientV8cwithfeatures = "otclient.ovh:7171:1099:25:30:80:90",
}
ALLOW_CUSTOM_SERVERS = true -- if true it will show option ANOTHER on server list
-- CONFIG END
```

Also remember to add your sprite and data file to data/things

That's it, you're ready to use OTClientV8.

DirectX version requires 3 dlls: libEGL.dll libGLESv2.dll d3dcompiler_47.dll

If it can't start (missing dlls) then user need to install visual studio 2019 redistributable x86: https://aka.ms/vs/16/release/vc_redist.x86.exe

# Windows

You need visual studio 2019

vcpkg install boost-iostreams:x86-windows-static boost-asio:x86-windows-static boost-beast:x86-windows-static boost-system:x86-windows-static boost-variant:x86-windows-static boost-lockfree:x86-windows-static boost-process:x86-windows-static boost-program-options:x86-windows-static luajit:x86-windows-static glew:x86-windows-static boost-filesystem:x86-windows-static boost-uuid:x86-windows-static physfs:x86-windows-static openal-soft:x86-windows-static libogg:x86-windows-static libvorbis:x86-windows-static zlib:x86-windows-static libzip:x86-windows-static openssl:x86-windows-static

# Linux

on linux boost >=1.67 and libzip-dev, physfs >= 3 also gcc >=9, because otcv8 uses c++17 sudo add-apt-repository ppa:ubuntu-toolchain-r/test sudo apt update sudo apt install gcc-9 g++-9 Then just mkdir build && cd build && cmake .. && make -j8

# Android

To compile on android you need to create C:\android with

 - android-ndk-r21b https://dl.google.com/android/repository/android-ndk-r21d-windows-x86_64.zip
 - libs from android_libs.7z

Also install android extension for visual studio In visual studio go to options -> cross platform -> c++ and set Android NDK to C:\android\android-ndk-r21b Right click on otclientv8 -> proporties -> general and change target api level to android-25

Put data.zip in android/otclientv8/assets You can use powershell script create_android_assets.ps1 to create them automaticly (won't be encrypted)
