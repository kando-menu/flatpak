## 🚧 Under Construction 🚧

Create the Kando AppImage:

```bash
cd kando
npm run package
./tools/make-app-image.sh
```

Then copy the AppImage from `out/make/appimage/Kando-1.5.1-x86_64.AppImage` to the root of this repository.
Next build the flatpak:

```bash
flatpak-builder --force-clean --user --install-deps-from=flathub --repo=repo --install builddir menu.kando.Kando.yml
```

Finally, test the flatpak:

```bash
flatpak run menu.kando.Kando
```
