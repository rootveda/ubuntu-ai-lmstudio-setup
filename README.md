# ubuntu-ai-lmstudio

Step-by-step guide for installing and running [LM Studio](https://lmstudio.ai/) — a powerful desktop app for developing and experimenting with Large Language Models (LLMs) locally — on Ubuntu systems. This repo covers downloading, extracting, and basic setup to get you started quickly with local LLM research and prototyping.

## About LM Studio

LM Studio is a user-friendly desktop app designed for local LLM workflows. It lets you run, interact with, and experiment with popular language models without relying on cloud-based APIs, ensuring privacy, convenience, and full control over your environment.

## Features

- Local LLM execution on your machine
- Easy-to-use graphical interface
- No data leaves your computer — preserve privacy!
- Supports various popular open-weight LLMs


## Installation Steps

Below are step-by-step instructions for downloading, extracting, and setting up LM Studio on Ubuntu.

### 1. Download the AppImage

Save the latest LM Studio `.AppImage` package to your Downloads directory. Visit the [official LM Studio site](https://lmstudio.ai/download) to download.

```bash
cd ~/Downloads/
```


### 2. Check the Downloaded File

Ensure your `.AppImage` file has downloaded:

```bash
ls LM-Studio-*.AppImage
```


### 3. Make the `.AppImage` Executable

Give execute permissions:

```bash
chmod u+x LM-Studio-0.3.20-4-x64.AppImage
```


### 4. Extract the AppImage

Extract the contents (this creates a folder called `squashfs-root`):

```bash
./LM-Studio-0.3.20-4-x64.AppImage --appimage-extract
```


### 5. Change Directory to Extracted Folder

```bash
cd squashfs-root
```


### 6. Change Ownership of chrome-sandbox

Some Ubuntu systems require root ownership for the `chrome-sandbox` binary:

```bash
sudo chown root:root chrome-sandbox
```
```bash
sudo chmod 4755 chrome-sandbox
```

## Getting Started

After the above steps, you should be able to run LM Studio directly from the `squashfs-root` folder. You can now begin experimenting with LLMs locally!

```bash
./lm-studio
```

## Contributing

Contributions, improvements, and clarifications are welcome!

## License

This repository shares installation instructions but does not distribute LM Studio itself. Please refer to LM Studio’s own licensing and terms of use.

**Happy experimenting with local LLMs on Ubuntu!**
