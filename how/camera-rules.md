# One set of rules per camera

[日本語](camera-rules.ja.md) · [How it works](README.md)

Cameras speak a common protocol, PTP, but every maker adds commands of its own,
and the wrong command at the wrong moment can leave a camera stuck.

Tethr keeps one driver for each model it has tested. A driver's rules are an allowlist:
only commands that were tried on the real camera are sent, and each one is checked —
down to its parameters and which way the data flows — before it goes out.
A camera saying it supports a command is not enough. If Tethr has not tried it on that camera, it is not sent.

The driver is chosen from the identity the camera reports. When no driver matches, or more than one does,
Tethr falls back to a basic mode — browse, preview, import — and sends nothing that could leave the camera stuck.

## Two rules from the Nikon D300

- **Busy means wait, never a different command.** When shooting without writing to the card and the camera answers "busy",
  Tethr waits 250 ms and asks again, for up to about four seconds. It never switches to the ordinary capture command instead:
  that one writes to the card, and a frame that was meant to skip the card would land on it.
- **Read each image once.** The D300 limits how much can be read from one image in total, across every read of it.
  A read past that limit does not fail — it never comes back. So Tethr reads each image once, from the start,
  and never reads the same part twice.
