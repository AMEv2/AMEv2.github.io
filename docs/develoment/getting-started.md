---
layout: default
title: Getting Started
parent: Development
nav_order: 1
---

# Developing Firmware for AME
{: .no_toc }
AME Firmware is developed using Espressif's ESP-IDF V5.2.x

# Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Windows

## Using Visual Studio Code Devcontainer (Preferred Method)
Even though the Visual Studio Code with the Espressif Plugin is simpler to get setup than the devcontainer method, this method have proven more reliable especially to ensure the correct version of ESP-IDF is being used. The AME project already includes the devcontainer configuration. You just have to install the other prerequisites.
 - WSL with Ubuntu
 - Docker Desktop
 - Visual Studio Code
 
To develop the AME frimware using this method follow this [guide](https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/using-docker-container.md)

## Visual Studio Code + Espressif Plugin
Follow the ESP-IDF getting started documentation found [here](https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/install.md)

# Linux
Follow the Espressif [documentation for Linux](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/linux-macos-setup.html)