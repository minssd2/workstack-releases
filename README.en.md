# WorkStack

[한국어](README.md)

**A macOS app that stacks your in-progress tasks as blocks floating over the screen, so you never lose track of what you were doing when something urgent cuts in.**

![WorkStack overlay](images/overlay.png)

## When to use it

You are writing a report when an urgent incident comes in. Stack a new block on top. When the urgent work is done, complete its block and the report block is back on top. Most of the time the stack holds zero or one block; it only grows when work interrupts work.

## Features

- **Glass blocks that stay on top**: visible over other apps and full-screen apps, and clicking them never steals focus from the app you are working in.
- **Add / Quick add**: stack a task with a title and details, or stack a "New task" block instantly.
- **Complete and undo**: hover a block and press ✓ to complete it, with 4 seconds to undo. Press ✎ to edit.
- **Adapts to its size**: as the overlay shrinks it hides details, then time, then titles; very small blocks show color only, and hovering one shows its title.
- **Click-through mode**: the overlay dims and clicks pass through to the window below.
- **Automatic English input**: switches to an English input source while you type a title and switches back afterwards (can be turned off).
- **Completion history**: completed tasks are recorded per day.
- **Update notice**: a blue dot appears on the menu bar icon when a new version is out.
- Korean and English UI, launch at login.

![Compose block](images/compose.png)

## Install

1. Download `WorkStack-<version>.zip` from the [latest release](https://github.com/minssd2/workstack-releases/releases/latest) and unzip it.
2. Move `WorkStack.app` to the **Applications** folder.
3. If macOS says it cannot verify the developer the first time you open it, go to **System Settings → Privacy & Security**, click **Open Anyway** near the bottom, and confirm.
   - Or run this in Terminal:
     ```bash
     xattr -dr com.apple.quarantine /Applications/WorkStack.app
     ```

> WorkStack is a personally distributed app without Apple notarization, so this one-time approval is needed.

## Usage

WorkStack lives in the menu bar instead of the Dock. Hover the blocks to show the add buttons and resize handles.

| Action | Default shortcut |
|---|---|
| Add task (title and details) | ⌃⌥⌘N |
| Quick add | ⌃⌥⌘J |
| Complete top task | ⌃⌥⌘D |
| Show / hide overlay | ⌃⌥⌘S |
| Toggle click-through | (not set) |

Change any shortcut from the menu bar icon → **Settings…**. In the compose block, press Enter to add and Esc to cancel.

![Menu bar menu](images/menu.png)

## Updates

When the menu bar icon shows a blue dot, choose **Download version …** at the bottom of the menu, download it from the release page, and replace the app in Applications. The current version is shown on the last line of the menu.

## Requirements and privacy

- macOS 26 or later (Apple silicon and Intel)
- Tasks and history are stored only on your Mac: `~/Library/Application Support/WorkStack`
- The network is used only to check for new versions (reading public GitHub releases). No personal data or usage data is sent.

## Uninstall

1. Turn off **Launch at login** in Settings and quit the app.
2. Delete `WorkStack.app` from Applications.
3. To remove your data as well, delete `~/Library/Application Support/WorkStack`.

## Changelog

See the [releases](https://github.com/minssd2/workstack-releases/releases) for what changed in each version.
