# Lab Setup Notes

## Why TryHackMe Instead of a Local Home Lab?

I initially planned to build a complete Wazuh home lab with the following setup:

- **Kali Linux VM** (VMware) → Wazuh Manager + Indexer + Dashboard
- **Windows Host** → Wazuh Agent

However, due to **hardware limitations** (insufficient RAM), running the full Wazuh stack locally was not practical. The official minimum recommendation for a single-node deployment is around 8 GB of RAM, which my system could not reliably support.

### Alternative Approach

I used the official **TryHackMe room: [Exploring Wazuh](https://tryhackme.com/room/exploringwazuh)**.

This room provides a pre-configured Wazuh environment with:

- Wazuh Manager + Indexer + Dashboard on a single VM
- Two pre-registered agents (Windows + Linux)
- Access to all major features (IT Hygiene, Vulnerability Detection, Configuration Assessment, Discover, Rules, etc.)

### Lab Access Details (from the room)

- URL: Provided in the room (changes per instance)
- Username: `thmuser`
- Password: `TryHackMe!`

> Note: Agents appear as **Disconnected** in this lab — this is expected behavior.

### Benefits of This Approach

- Fully functional Wazuh environment without local resource constraints
- Ability to explore real features and take screenshots for documentation
- Still demonstrates practical understanding of Wazuh architecture and capabilities

### Future Goal

When better hardware becomes available, I plan to deploy a full single-node Wazuh lab and connect real agents from Windows and Linux systems.
