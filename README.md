# Cyb3rBreak Games

Hacker-style, self-contained HTML5 mini-games for the **Cyb3rBreak** module of
[PurrSh3ll](https://github.com/PurrSh3ll/purrsh3ll). They are meant to be played
inside the app while you wait on a long-running command (bruteforce, scans, etc.).

Everything here is an **educational simulation** — nothing is compiled or executed
against a real target. Each `.game` file is a single, self-contained HTML document
(inline CSS + JS) that runs in a browser / embedded web view.

## Games

| File | Genre | Idea |
|------|-------|------|
| `C2 PONG.game` | Asymmetric Pong | WAF (Blue) vs C2 (Red): bounce a payload packet, charge energy, fire exploits (SYN flood, IP spoof, ransomware, rate limit, DPI, air gap). |
| `P0RTCR4WLER.game` | Snake | Crawl the grid eating port numbers that match your unlocked services; wrong port = downgrade. Escalate through services as you go. |
| `STACK SM4SH.game` | Tetris | Stack instructions and NOP sleds, snipe shellcode with a return-address block, clear the stack. |

## Usage

This repository is consumed as a **git submodule** of PurrSh3ll at
`appmodules/Cyb3rBreak`. A plain `git clone` of the main repo leaves the folder
empty; fetch the games with:

```sh
git clone --recurse-submodules https://github.com/PurrSh3ll/purrsh3ll.git
# or, after a normal clone:
git submodule update --init --recursive
```

To try a game standalone, just open any `.game` file in a browser.

## License

Released under the **GNU General Public License v3.0** — see [LICENSE](LICENSE).

Copyright (C) 2026 zombi666
