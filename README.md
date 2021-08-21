# Introduction
Build OpenWrt in a container? That's simple.

Explore and develop OpenWrt in a container? Don't panic, this is the way.

# Usage

## Start a container

```
git clone https://github.com/riverscn/openwrt-dev-container.git
cd openwrt-dev-container
docker-compose run -d devenv bash
```

## Use a container

1. Install Docker extension in VSCode, and attach your container to VSCode.

2. Open `/workspace` folder in VSCode.

3. Open a terminal in VSCode.

4. Clone a openwrt repo into it, and follow its instruction.

## Files access

Workspace files is stored in two volumes:

* env-data: persists files in `/workspace`

* env-home: persists files in `/home/vscode`

When container is stopped, these files are still there.

You can easily download and upload files in VSCode's "explorer" tab.

## Define your own environment

You can modify `Dockerfile` and `docker-compose.yml` to meet your different requirements.