# Clawfinger <img width="256" height="256" alt="image" align="right" src="https://github.com/user-attachments/assets/dee33546-0c11-4404-830c-ca6fb610a275" />


**A true local gateway for agentic phone control.**

Clawfinger turns a regular Android phone into a voice interface for your AI agents. It consists of two parts: a **phone bridge app** that handles the calls, and a **gateway** running on your computer that connects those calls to the LLM of your choice. Your agents can listen, speak, and act — all through real phone calls on a real mobile number.

---

## What Can You Do With This?

- **Control your agents by calling them.** Pick up any phone, dial your Clawfinger number, and talk to your agent directly.
- **Let your agents make and receive calls on your behalf.** Schedule appointments, return missed calls, handle inquiries — hands-free.
- **Trigger any action through conversation.** Your agent's existing tool-calling pipeline works during calls, so anything your agent can do, it can now do by voice.

---

## Why a Real Phone Instead of VoIP?

Most voice-AI setups rely on SIP trunks, VoIP providers, or landline integrations. Clawfinger takes a different approach: it uses an actual phone with a regular SIM card. Here's why that matters:

| | Traditional (SIP/VoIP) | Clawfinger |
|---|---|---|
| **Setup** | Trunk provisioning, DID numbers, codec config | Plug in a phone via USB |
| **Cost** | Per-minute billing, monthly trunk fees | One flat-rate mobile plan |
| **Reputation** | Shared IP pools — your number can get flagged because of other users in the same pool | Your own SIM, your own number, your own reputation |
| **Reliability** | Ooh, NAT traversal, ooh, ooh, ooh | It's a phone call. It just works. |
| **IoT/Telecom integration** | Specialized hardware, complex configuration | Not needed |

---

## What You Need

**A phone:**
Any Android phone running Android 14 or newer. We recommend a dedicated spare phone — think of it as giving your agents their own ears and voice (and soon, eyes). Do **not** use your personal daily phone for this.

> Don't have a spare phone? A new or refurbished **Google Pixel 7a** is a great choice. It doesn't need a Google account, and we actually recommend keeping both Google sign-in and Wi-Fi turned off. Just insert a SIM card and you're ready.

**A computer:**
A Mac, Linux box, or any machine that can run your agents. We've verified everything works on a **Mac Mini with 16 GB RAM** — including the local LLM, speech recognition, and text-to-speech models that Clawfinger uses. No cloud APIs required.

**An agent (optional but recommended):**
Clawfinger ships with an [OpenClaw](https://github.com/Trac-Systems/openclaw) integration for full local phone call management. You can also connect your own agents via the WebSocket API.

---

## A Note on Responsible Use

Clawfinger is designed for **personal agentic use** — one phone, one agent, one number. It is not built for bulk dialing or mass outreach. Spammers use specialized telecom equipment that is orders of magnitude cheaper per channel than a single smartphone. This tool is for people who want their AI agent to have a real phone presence, not for scaling outbound campaigns.

---

## How to Install

### 1. Get your phone ready

Have an Android phone with Android 14+ available. Tested with **Google Pixel 7a** and **Pixel 10 Pro**.

If you need to buy one, a new or refurbished Pixel 7a is the sweet spot — affordable, well-supported, and more than capable. No Google account or internet connection required on the device.

### 2. Connect via USB

Plug the phone into your computer with a USB-C cable. Make sure USB debugging is enabled in the phone's developer settings.

### 3. Point your agent at the repos

Give your agent access to these two repositories. Each contains a skill file that your agent can read to guide you through setup automatically:

- **Phone bridge app:** [github.com/Trac-Systems/clawfinger-app](https://github.com/Trac-Systems/clawfinger-app)
- **Voice gateway:** [github.com/Trac-Systems/clawfinger-gateway](https://github.com/Trac-Systems/clawfinger-gateway)

Your agent will pick up the installation instructions and walk you through the process step by step.
