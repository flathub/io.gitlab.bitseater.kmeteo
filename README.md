# Flatpak for KMeteo

This folder contains the Flatpak manifest to publish the application from a remote repository, as is done in Flathub.

## Requirements

- flatpak
- flatpak-builder
- Flatpak runtime system available

```bash
flatpak remote-add --user flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

## Build from remote repository

From the root of the project:

```bash
flatpak-builder --user --install --force-clean build-dir com.gitlab.bitseater.kmeteo.yml
```

## Run

```bash
flatpak run com.gitlab.bitseater.kmeteo
```

## Rebuild

```bash
flatpak-builder --user --install --force-clean build-dir com.gitlab.bitseater.kmeteo.yml
```

> The app module uses `type: git` so that the manifest can be built from the remote repository and prepared for submission to Flathub.
