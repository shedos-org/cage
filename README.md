# cage

[ShedOS](https://shedos.org)'s build of
[cage](https://github.com/cage-kiosk/cage), the kiosk Wayland compositor that
greetd hosts the ShedOS greeter inside.

cage has no input configuration surface, so every pointer attaches with the
libinput defaults and tap-to-click ends up off — the wrong default for a laptop
login screen. The one downstream patch here turns tap on for touchpads, and
`provides`/`conflicts` on `cage` take the stock package's place.

**Build-out in progress.** Production lives at
[Theshedman/shedos](https://github.com/Theshedman/shedos) until the multi-repo
cutover completes; this repo publishes to a staging channel.

[shedos-org/shedos-ci](https://github.com/shedos-org/shedos-ci) builds and
tests this repo and requests publication;
[shedos-org/shedos-release](https://github.com/shedos-org/shedos-release)
signs and publishes.
