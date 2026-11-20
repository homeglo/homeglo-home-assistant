# Circadian Light by HomeGlo

Circadian Light adapts your smart lights' color and brightness to your daily pattern. It runs the "Brain" inside Home Assistant. The HomeGlo phone App controls it.

Home Assistant now calls add-ons "apps." This page uses that word.

## Before you start

- Your Home Assistant must run on aarch64 or amd64.
- You need the registry username and password (a token) from HomeGlo.
- If you already have a working HomeGlo home, stop here. Do not install a second copy next to it. Contact hello@home-glo.com for an attended first enrollment.

## 1. Add the registry

The app images are private. Without this step, the install fails with "unauthorized."

1. Go to Settings → Apps → App store.
2. Open the ⋮ menu and choose Registries.
3. Choose Add registry.
4. Registry: `ghcr.io`
5. Username and Password: the values HomeGlo gave you.
6. Save.

## 2. Add the repository

1. In the App store, open the ⋮ menu and choose Repositories.
2. Add this URL: `https://github.com/homeglo/homeglo-home-assistant#stable`
3. Close the dialog and choose Check for updates.

## 3. Install and start

1. Open Circadian Light by HomeGlo in the App store.
2. Choose Install.
3. Choose Start.

## First steps

1. Open the Circadian Light panel.
2. Add your Rooms to the Main Zone. A fresh install starts with no Rooms in Main, so only Off works until you add them.
3. Pair the HomeGlo App from the panel.

## Updates

Use Home Assistant's normal Update button on the app's page.

## Backups

Use Home Assistant's normal Backup controls. Backups run while the app keeps running. Your lights do not pause.

## Troubleshooting

- Install fails with "unauthorized": the registry is missing or the username or password is wrong. Repeat step 1.
- The app does not appear in the App store: check that the repository URL is exact, then choose Check for updates.
- Only Off works: add Rooms to the Main Zone. See First steps.

## Help and privacy

- Help: hello@home-glo.com
- Privacy policy: https://www.home-glo.com/privacy-policy-2/
