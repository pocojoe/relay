# Relay

**Move a long project into a fresh chat at a planned stopping point -- while the chat is still healthy.**

Relay (murelay) is a natural-language program a chat *performs*. At the end of a session it captures the project's working state and files into one zip. The next chat unpacks that zip and picks up where the last one stopped. Each handoff adds a link to a chain of chats on one project. Tested on Claude and ChatGPT (both accept .zip uploads). Gemini is not yet supported.

Home: [maceutils.com/mu-relay](https://maceutils.com/mu-relay/) -- MIT License -- (c) 2026 Joseph M. Miller MD MPH

---

## The problem it solves

Long projects outgrow a single chat. As a chat fills, older messages are compressed and details drop out. [Rescue](https://github.com/pocojoe/rescue) handles that emergency after it starts. Relay prevents it: the project moves to a new chat on schedule, before anything is lost.

## What Relay carries

- Goal, rules, files, decisions, next step, and the last topic discussed.
- A ~200-word synopsis of the session and a topic list the operator reviews.
- A one-line purpose note for each file.
- The files themselves, as plain members of the zip, with SHA-256 checksums and modification times.

The new chat unpacks everything to its workspace but reads only the essentials into the conversation; other files are read when a step needs them.

## How to use it

1. **Relay -- in the chat you are finishing.** Download [`murelay.zip`](https://github.com/pocojoe/relay/releases/latest/download/murelay.zip), upload it, and say **"Read and follow directions."**
2. Confirm the project name and topics. A file named `murelay-<project>-<date>.zip` is produced; download it.
3. **Recover -- in a new chat.** Upload that file and say **"Read and follow directions."**
4. At the end of each session, relay again.

Keep the zips. Each is a standard archive; unzip it to get the plain files.

## Relay or Rescue?

Relay is for planned stops while the chat is healthy. Rescue is for a chat already showing strain.

## License

Released under the MIT License. Free to use, change, and share. Provided "as is", without warranty.
