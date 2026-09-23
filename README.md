# Codec

![Codec](docs/screenshot.png)

**Self-hosted voice, video and text chat. You run the server; nobody else owns
the room.**

Codec is a desktop chat app and the server behind it. One server is one Guild:
its own channels, ranks, rules and members, and everyone who joins is in it. No
layer of sub-communities to set up before anyone can say anything. Voice, video
and screen sharing go straight between the people in the call. Direct messages
filter out strangers until you say otherwise. And an admin panel tells a server
owner what is actually happening on their instance, rather than leaving them to
guess.

[**Download the latest release →**](../../releases/latest)

*Windows 11 users: Codec is unsigned, so Smart App Control blocks the installer.
[How to turn it off](#windows) — it takes about thirty seconds.*

---

## Android — Droid-ify

Add the official Codec repository to Droid-ify to install Android releases and
receive updates directly on your device.

1. Open [the Android download page](https://uhd3mon.github.io/codec/).
2. In Droid-ify, open **Repositories**, choose **Add repository**, then paste the
   repository link from that page or scan its QR code.
3. Enable **Codec for Android**, refresh, search for **Codec**, and install it.

Repository: https://uhd3mon.github.io/codec/fdroid/repo

Signing fingerprint:
`AF68C2CEDD5E12C7591057D1BFD8B9A081E8967A7DDC2BE351A427034074E8B7`

This is Codec's own repository, which you add once to Droid-ify. The Android
1.5.1 rebuild remains a private preview; the feed currently offers 1.4.95.

## What it does

### Talk

- **Voice and video are peer-to-peer.** The server passes the introductions and
  then gets out of the way, which is why a small box can host a busy server.
- **Screen sharing with real audio** — up to 1080p60, 256kbps stereo, and a
  system-audio path on Linux that most clients do not have at all.
- **A call layout that matches how people watch one.** Shared screens fill the
  top; every camera runs along the bottom in one uniform strip. Double-click
  anything to blow it up, double-click to put it back.
- **You can see who is talking** — their row lifts, their tile takes a border.
- **Call controls sit next to the call button**, in every window a call can
  happen in, and appear only once a call is actually connected.
- **Push to talk or open mic**, on a key or a mouse button — the side buttons
  included. The key works while you are looking at a game rather than at Codec.
- **A noise gate that is actually on**, so the room behind somebody is not in
  the call between their sentences, and automatic gain so a quiet microphone
  still arrives at a normal level.
- **Per-person volume** on anybody's profile card, for whoever is always too
  loud or too quiet.
- **The channel header turns green** when there is a call happening in it,
  whether or not you are in it.

### Organise

- **One server, one Guild.** Its channels, categories, ranks, bans and rules
  page — and everybody who joins is already in it. Nothing to join first.
- **Channels have their own identity.** A name, a topic, a description and a
  picture that shows beside it in the list and in the header.
- **Invite links belong to a channel**, public or private. Share one and it
  takes whoever follows it straight into that room.
- **Drag to arrange.** Channels between categories, categories into whatever
  order you want, and anything into Favorited to keep it at hand.
- **`#rules` and `#general` are always there.** They can be renamed; they
  cannot be deleted out from under the people using them, and everyone is in
  both from the moment they join.
- **Anyone can make a channel.** Only the people running the guild decide where
  it is filed.

### Ranks

Member → Moderator → Super Moderator → Operator → Superuser.

- **Moderator** moderates the channels they were promoted in.
- **Super Moderator** does the same in every channel on the server, and can
  lock or unlock any of them.
- **Operator** runs the guild: its name, its description, its picture, its
  channels and its members.
- **Superuser** runs the server, and has the admin panel.

### Emotes and Twitch

- **Your Twitch emotes, here.** Link your account with `/link` and you can use
  everything you already hold on Twitch — subscriptions, follower emotes,
  channel-point unlocks — in every channel.
- **BTTV and 7TV** are supported alongside Twitch's own, global sets included.
- **The picker is organised the way you think about it**: your own channel
  first, then each channel you are subscribed to under its own name and
  picture, then Twitch, BTTV and 7TV. Every tier of a channel's emotes, and its
  follower emotes, sit together under that channel.
- **A purple ring** around somebody's picture while they are live, and a card
  on their profile with the game, the title and a link to the stream.
- **A channel operator can attach their own Twitch channel** to a channel they
  run, which adds that broadcaster's emotes to it.
- Codec asks Twitch for exactly one permission — the right to read which emotes
  you may use. It cannot post, follow, subscribe, or read a message.

### Presence

- **See what people are playing.** Codec reads the name of the running program
  and shows it under their name, with an Activity strip at the top of the
  member list showing the three most recent and how long they have been at it.
  It reports the program's name and nothing else — never a window title, never
  a path — and it is a setting you control.
- **Games are recognised by name where it matters** and by where they are
  installed otherwise, so titles nobody has heard of still show up correctly.
  Launchers, browsers and Codec itself never do.

### Messages

- **Message requests.** Anyone can write to you; a stranger's first message
  arrives as a request you read before accepting. Declining is quiet — they are
  not told, and they stop reaching you.
- **Images are compressed on the way in.** A 6.8MB photo is stored at around
  600KB, and the quality is walked down to a size budget rather than a fixed
  setting, so one detailed photo cannot cost twenty times what another does.
- **Click any picture** for a full-screen preview, with a button to open it in
  a browser.
- **History loads as you scroll**, fifty at a time, rather than pulling a
  channel's entire past on open.
- **Every channel remembers where you were.** Switch away and back and you are
  where you left off, with a **New messages** line marking the first thing that
  arrived while you were gone.
- **Links behave.** A pasted URL is shown as the site and the part that
  matters, with a card underneath carrying the page's picture and title. A
  Codec channel link becomes a card with the channel's picture and a Join
  button.
- **Pictures, several at a time**, with a thumbnail each and one caption for
  the lot.

### Run it

- **One binary, one SQLite file.** No database server, no runtime, no container
  required.
- **An admin panel worth opening** — who is online against how many connections,
  message volume over a fortnight, the busiest channels and people, live calls,
  storage and what compression saved.
- **Accountability.** Open reports, how long the oldest has sat, and whether
  the guild's own staff are clearing them or you are doing it for them.
- **A full audit log**, filterable by action and by person.
- **Reports** from any message, profile or channel, reaching the guild's
  moderators and the server owner.
- **Switches that matter**: avatar uploads, image uploads, and the size limit,
  all changeable without a restart.
- **Twitch, set up from the panel.** Paste in your own application's keys and
  it takes effect immediately; the redirect address you have to register is
  shown with a Copy button.
- **A restart button**, for the rare thing that needs one. Everyone is warned
  first and reconnects on their own.
- **The client and the server update independently.** A fix to the app does not
  cost the people mid-call their call.

### The app

- **A terminal look** — monospace chrome and one accent colour, in dark or
  light. Dark is the default.
- **Adjustable interface scale**, 80% to 150%.
- **A mobile layout that works**, with both side columns as drawers and every
  admin table folded into readable cards.
- **Self-updating**, both platforms, from this repository.
- **Desktop notifications** for mentions, direct messages, calls, friend
  requests and arrivals — each with its own switch, and each able to be turned
  off on its own.

---

## Install

### Server

Linux x86-64. Root on a fresh Ubuntu or Debian box:

```bash
tar xzf codec-server-linux-amd64.tar.gz
sudo ./install.sh
```

It installs to `/opt/codec`, keeps data in `/var/lib/codec`, and starts a
systemd service called `codec` on port 6670.

**The first sign-in is `superuser` / `admin`, and you are made to change it
before you can do anything else.**

A new server starts as a guild called **Test-Guild** with `#rules` and
`#general` in it. Rename it to whatever your community is called — click its
name at the top of the sidebar.

Put a reverse proxy in front of it, terminate TLS there, and point the client at
your domain. Example nginx:

```nginx
location / {
    proxy_pass http://127.0.0.1:6670;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
    proxy_set_header Host $host;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_read_timeout 3600s;
}
```

The `Upgrade` headers are not optional — everything Codec does runs over a
WebSocket.

```bash
journalctl -u codec -f          # logs
/var/lib/codec/codec.toml       # config
systemctl restart codec         # after editing it
```

The server checks this repository for new releases every ten minutes and updates
itself.

### Windows

Download `Codec-Setup.exe` and run it.

Codec is not code-signed, so Windows will object. On Windows 11 with Smart App
Control on, the installer is blocked outright:

1. **Settings → Privacy & security → Windows Security → App & browser control**
2. **Smart App Control → Off**
3. Run the installer. On the SmartScreen prompt: **More info → Run anyway**

Smart App Control cannot be switched back on without reinstalling Windows, which
is Microsoft's decision rather than mine. If you would rather not, use the Linux
build or a VM.

### Linux

Download `Codec.AppImage`, then:

```bash
chmod +x Codec.AppImage
./Codec.AppImage
```

No install step. It updates itself in place.

---

## What it does not do

- **No hosted service.** There is no codec.com to sign up to. You run a server
  or you join someone else's.
- **No source code here.** This repository is the README and the releases.
- **No telemetry.** Nothing is sent anywhere except the server you connect to.
- **P2P calls show your IP** to the people in the call. That is how peer-to-peer
  works; if that matters to you, only call people you know.

---

## Licence

Codec is proprietary. It is free to download and use; the source is not
published. The full terms are in the app under **Settings → Terms of Use**.

Made by **Kevin Walters** (d3mon).
