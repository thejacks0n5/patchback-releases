# PatchBack — downloads

PatchBack saves and recalls monitor mixes on Yamaha RIVAGE PM consoles: each
person's mix-bus sends as a named preset, week to week, onto whatever bus they
are on. It also does matrix buses, Watch (live drift checking), channel-strip
presets, Planning Center plans, undo and weekly auto-archiving.

It runs on Mac and Windows. **You need a license key to use it** — it comes
with your invitation. (PatchBack is in private beta.)

## Mac: install in 2 minutes

1. **Download:** [PatchBack for Mac (.dmg)](https://github.com/thejacks0n5/patchback-releases/releases/download/v0.23.0/PatchBack-0.23.0-universal.dmg)
   — one download for Apple Silicon and Intel, signed and notarized by Apple.
   (Newest version is always on the [releases page](../../releases/latest).)
2. **Open the .dmg** and drag **PatchBack** into **Applications**.
3. **Open PatchBack** from Applications (or Spotlight: ⌘-Space, type *PatchBack*).
4. macOS asks to allow **Local Network** access → click **Allow**. Without it
   PatchBack can't reach the console. (If you clicked Don't Allow: System
   Settings → Privacy & Security → Local Network → turn PatchBack on.)
5. **Paste your license key** when PatchBack asks, and press **Activate**. The
   key came with your download link (it starts `PB1.`). Copy the whole thing.
   It's checked on this Mac, so no internet is needed at the desk.

## Before you connect

- The Mac has to be **on the console's network** — the same switch/VLAN the
  RIVAGE DSP engine is on (cable or the console network's Wi-Fi), with an IP
  address in the same range as the console.
- PatchBack talks to the console the same way the RIVAGE PM Editor and
  StageMix do (Yamaha remote control, port 49280). The console allows a limited
  number of remote connections, so if PatchBack can't connect, close an Editor
  or StageMix session you're not using.

## First run: the setup guide (5 steps)

PatchBack opens a setup guide the first time. It never changes anything on the
console without telling you exactly what first.

1. **Find the IP.** On the console, open the network/setup screen and copy the
   **DSP engine's IP address** (e.g. `192.168.1.10` — yours will differ). Type
   it into PatchBack. Leave the port at **49280**.
2. **Test the connection.** PatchBack asks the console what it is. You should
   see ✓ **Found RIVAGE PM…** with its input, mix and matrix counts. Nothing on
   the desk changes. If it fails, the message says why (wrong address, nothing
   answering, cable) — fix that and press **Test again**.
3. **Pull the labels.** PatchBack reads every bus and channel name off the
   console. It matches people to buses by these names, so name your mix buses
   on the desk (e.g. *Vox 1*, *Drums*) and press **Sync again** if you rename
   them later.
4. **Test a write — safely.** PatchBack renames one *unused* mix bus to
   `PB TEST`, reads it back, then puts the original name back, and shows ✓ for
   each step. No level, send or anything audible is touched. If the link drops
   halfway, it reconnects and puts the name back; if it can't, a banner offers
   **Put the name back**.
5. **Done.** You're on the Mixes screen.

## Everyday use

- **Save:** tap the buses on the grid → **Save** → name it. Each bus becomes a
  preset (a person's mix) in the Library.
- **Recall:** pick a mix in the Library → **Recall to <name>** → check the
  preview → **Send**. Every write takes an **Undo** snapshot first.
- **Several at once:** select a folder → **Stage on their buses** → **Push**.
  The push dialog shows how many values will change before anything is sent.
- **Watch:** after a push, press **Watch** to have PatchBack check the desk and
  flag any bus that drifts from its preset during the service.
- **Undo** (top right) puts back any recall or whole push in one step.
- **Setup** (top right) holds every setting; nothing new is on by default.

## Good to know

- Closing the window keeps PatchBack running in the **menu bar**. Quit from
  that icon.
- **Updates** download in the background; **Restart to update** appears when
  one is ready. Nothing installs until you click it, and your mixes and
  settings are never touched. Updates are signed and checked before install.
- **Other devices** can't open PatchBack unless you turn on network access in
  Setup › Undo, PIN & network — and that needs a PIN.
- **Windows:** `PatchBack-Setup-….exe` on the [releases page](../../releases/latest).
  It isn't code-signed yet, so Windows shows "Windows protected your PC": click
  **More info → Run anyway**.
- Try anything new on a spare bus first and read the preview before sending.
- This repository only hosts the downloads; the source code is private.
