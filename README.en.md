# WorkLayer

[한국어](README.md)

**A macOS menu bar app that keeps what you are working on, what just cut in, and the notes and reference images you keep looking at floating above every app.**

> WorkLayer is the new name of WorkStack from 2.0 on. The app grew from a single task stack into a layer over your screen that also holds notes and images, so it got a new name.

![WorkLayer on screen: a transparent mockup image, a memo, and Doing and Waiting stacks](images/overview.png)

## Why

The easiest thing to lose at work is what you were just doing. After a chat question, an incident or a sudden meeting, you come back and the thread is gone. To-do and note apps sit behind your working windows, so you only see them when you go and open them. Things you need to see all day, like a server address, a command you keep typing or a design mockup, mean switching windows again and again.

WorkLayer puts all of this on one layer above the app you are working in.

- **Always visible.** It floats over other apps and full-screen apps, with nothing to open.
- **Stays out of the way.** Clicking it never takes focus or keystrokes from the app you are working in. Make things translucent, or let clicks pass through to the window below.
- **Interruptions keep their order.** New work stacks on top of what you were doing; finish it and the earlier task is back on top.

## When to use it

- You are writing a report when an incident comes in. Stack a block on top. When the incident is handled, complete its block and the report block is on top again.
- Keep separate "Doing" and "Waiting" stacks, or one stack per display. Move tasks that wait on someone else to the Waiting stack.
- Keep a server address or commands as a memo and a mockup or screenshot as an image next to your editor. Lower the opacity and turn on click-through to keep working underneath.
- Pin a photo you love to a corner of the screen and take a moment of calm on a busy day. Make it translucent and turn on click-through so it never gets in the way.

## Features

**Task stacks**
- Stack a task with a title and details (Add task), or a "New task" block with no typing (Quick add).
- Hover a block and press ✓ to complete it or ✎ to edit it. Undo a completion within 4 seconds or from the menu.
- Create several stacks and name them. Shortcuts act on the active stack, and hovering a stack shows its name tag.
- Turn on move mode (⇄) in the toolbar and drag blocks to another stack, or right-click a block and choose "Move to stack".
- As a stack shrinks it hides details, then time, then titles; very small blocks show color only.

**Memo cards**
- Plain-text cards. Start editing with ✎; Enter adds a line, ⌘Enter or Esc finishes. Text is saved as you type.
- Set the width and height with the right and bottom handles; longer text scrolls inside the card.

**Image cards**
- New image (⌃⌥⌘I) opens a frame: drop an image file on it or paste with ⌘V. You can also drop image files on a stack or card.
- Transparent parts of a PNG show what is behind, and clicks there pass through to the window below.
- Click an image to select it, then resize it from its edges; the aspect ratio is kept.

**Staying out of the way**
- Set the opacity of each stack, memo and image, with per-kind defaults in Settings.
- Turn on click-through for each stack, memo and image. Turn it off again from the menu bar menu.
- Reset position lays out all stacks and cards on the main display without overlapping.

**Also**
- Optionally switches to an English input source while you type a task and back afterwards (off by default).
- Completed tasks are recorded per day.
- A blue dot appears on the menu bar icon when a new version is out.
- Korean and English UI, launch at login.

## Install

1. Download `WorkLayer-<version>.zip` from the [latest release](https://github.com/minssd2/workstack-releases/releases/latest) and unzip it.
2. Move `WorkLayer.app` to the **Applications** folder.
3. If macOS says it cannot verify the developer the first time you open it, go to **System Settings → Privacy & Security**, click **Open Anyway** near the bottom, and confirm.
   - Or run this in Terminal:
     ```bash
     xattr -dr com.apple.quarantine /Applications/WorkLayer.app
     ```

> WorkLayer is a personally distributed app without Apple notarization, so this one-time approval is needed.

## Usage

WorkLayer lives in the menu bar instead of the Dock. The menu is grouped as tasks → create (new stack, memo, image) → stack, memo and image lists → overlay → settings. Hover a stack to show its name tag, toolbar (move handle, click-through, move mode, quick add, add task) and resize handles; the top block shows ✎ edit and ✓ complete.

![A hovered stack](images/stack.png)

| Action | Default shortcut |
|---|---|
| Add task (title and details) | ⌃⌥⌘N |
| Quick add | ⌃⌥⌘J |
| Complete top task | ⌃⌥⌘D |
| New memo | ⌃⌥⌘M |
| New image | ⌃⌥⌘I |
| Show / hide overlay | ⌃⌥⌘S |

Change any shortcut from the menu bar icon → **Settings…**. In the compose block, press Enter to add and Esc to cancel.

![Menu bar menu](images/menu.png)

## Updates

When the menu bar icon shows a blue dot, choose **Download version …** at the bottom of the menu, download it from the release page, and replace the app in Applications. The current version is shown on the last line of the menu.

## Requirements and privacy

- macOS 26 or later (Apple silicon and Intel)
- Tasks, memos, images and history are stored only on your Mac: `~/Library/Application Support/WorkStack` (the folder keeps the old name)
- The network is used only to check for new versions (reading public GitHub releases). No personal data or usage data is sent. The clipboard is read only when you press ⌘V in an image frame.

## Uninstall

1. Turn off **Launch at login** in Settings and quit the app.
2. Delete `WorkLayer.app` from Applications.
3. To remove your data as well, delete `~/Library/Application Support/WorkStack`.

## Changelog

See the [releases](https://github.com/minssd2/workstack-releases/releases) for what changed in each version.
