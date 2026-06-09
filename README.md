<h1 align="center">
  <br>
  <a href="#"><img src="https://tstatic.akash-go.com/cms-ui/images/custom-content/1735560559088.png" alt="Akashgo Live TV" width="120"></a>
  <br>
  🔥 Akashgo Live TV DRM Updater 🔥
  <br>
</h1>

<h2 align="center">Automated GitHub Actions Workflow for Akashgo Clearkey Playlists</h2>

<p align="center">
  <a href="https://www.gnu.org/software/bash/">
    <img src="https://img.shields.io/badge/Made_With-Bash%20Script-blue" alt="Bash">
  </a>
  <a href="https://t.me/codecrafter_codecphp">
      <img src="https://img.shields.io/badge/Brand-CodeCrafter-green.svg" alt="CodeCrafter">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Platform-Akashgo-purple" alt="Akashgo">
  </a>
  <a href="#"><img src="https://img.shields.io/badge/Made%20in-Bangladesh_🇧🇩-green?colorA=%23ff0000&colorB=%23017e40&style=flat-square" alt="Bangladesh"></a>
</p>

## 📒 Introduction
This repository provides a fully automated backend infrastructure to extract, process, and update Akashgo Live TV channels. Using a lightweight shell script driven by GitHub Actions, it parses raw M3U streams, integrates dynamic Clearkey DRM licenses via a dedicated Cloudflare Worker, and outputs clean, ready-to-deploy playlists.

## 💥 Key Features
* **Zero-Downtime Automation:** Fully automated playlist updates executing every 24 hours via GitHub Actions.
* **Native Shell Processing:** Ultra-fast, dependency-free text parsing utilizing pure Bash, `curl`, and `jq`.
* **Dynamic DRM Injection:** Automatically builds and attaches custom Clearkey license URLs using specific channel IDs.
* **Custom Security:** Enforces a dedicated User-Agent (`https://t.me/codecrafter_codecphp`) for secure stream validation.
* **Dual-Format Output:** Simultaneously generates standard **M3U** configurations and structured **JSON** endpoints.
* **Universal Compatibility:** Formatted perfectly for Kodi (`inputstream.adaptive`), custom OTT platforms, and modern IPTV architectures.

## 🕹️ Live Data Links

* 👉 **[Auto Updated M3U Playlist](https://raw.githubusercontent.comhasanhabibmottakin/AkashGo/main/playlist.m3u)**
* 👉 **[Auto Updated JSON API](https://raw.githubusercontent.comhasanhabibmottakin/AkashGo/main/playlist.json)**

*(Note: Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub profile and repository details).*

## 💻 Example Usage (Python)

```python
import requests

link = "[https://raw.githubusercontent.comhasanhabibmottakin/AkashGo/main/playlist.json](https://raw.githubusercontent.comhasanhabibmottakin/AkashGo/main/playlist.json)"
channels = requests.get(link).json()

for channel in channels:
    print(f"Name: {channel['name']}")
    print(f"Group: {channel['title']}")
    print(f"License Key/Worker: {channel['drmlicense']}")
    print(f"Stream URL: {channel['link']}\n")
