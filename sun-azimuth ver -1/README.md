# Sun Azimuth

A small installable web app that estimates the Sun's compass bearing and altitude for the current time and a chosen location.

## Choose a location

- **Use my location** asks Safari for the iPhone's location. The coordinates are used in the browser for the calculation.
- **Use UK postcode** sends the postcode you enter to [Postcodes.io](https://postcodes.io/) to look up its coordinates. The app does not save the postcode. A postcode result is an approximate reference point for that area.

Tap **Enable phone compass** and allow Motion & Orientation Access if Safari asks. Keep the iPhone flat: the compass rose then turns with the phone, moving north around the dial while the pointer indicates the Sun on screen. The phone's magnetic compass can drift a few degrees.

## What is in this folder?

- `index.html` contains the screen, styling, location options, and solar-position calculation. This is the main file to edit.
- `manifest.webmanifest` gives the app its Home Screen name and standalone display mode.
- `sun-icon.svg` is the app icon.

There are no libraries, accounts, or build tools needed to change the app.

## Put it on an iPhone from Windows

The phone needs to open the app from an HTTPS website before Safari can use its location. GitHub Pages is one free way to host these static files. The app source is public, but the app does not publish or save a device's GPS coordinates or an entered postcode.

1. Sign in to GitHub, or create an account at [github.com](https://github.com/).
2. Create a new **public** repository named `sun-azimuth`.
3. In the repository, choose **Add file → Upload files**. Upload `index.html`, `manifest.webmanifest`, and `sun-icon.svg` from this folder, then commit the files.
4. Open the repository's **Settings → Pages**. Under the build and deployment section, choose **Deploy from a branch**, select the `main` branch and `/ (root)` folder, then save.
5. Wait for GitHub Pages to publish. The site address appears on that Pages settings screen and will look like `https://YOUR-USERNAME.github.io/sun-azimuth/`.
6. On the iPhone, open that address in **Safari**. Tap **Share → Add to Home Screen**. Turn on **Open as Web App** if shown, then tap **Add**.
7. Open the new Home Screen icon and choose **Use my location** or **Use UK postcode**. For the compass to turn with the phone, tap **Enable phone compass** and allow motion access if asked.

GitHub notes that first publication can take several minutes. Keep the trailing `/sun-azimuth/` in the website address.

## Changing it later

Edit `index.html` in a text editor such as Notepad or Visual Studio Code. Save and upload the changed file to the same GitHub repository. GitHub Pages republishes it; the Home Screen app will load the updated version when opened online.
