Launcher art and audio in this folder:

- launcher_background.png — default main window background.
  - In the project it is a WPF Resource (embedded in the .exe; Build Action Resource, not copied to output).
  - The XAML pack URI is /ImagineXILauncher;component/Assets/launcher_background.png
  - Replace Assets/launcher_background.png in the repo (or your working copy) with your artwork, then rebuild so the new image is embedded.
  - Optional disk override: set launcher_config.json UiBackgroundPath to any path that exists (relative to the launcher folder or absolute). If that file exists, it is used instead of the embedded default.
  - The launcher scales art to fill the window (UniformToFill); edges may crop if the aspect ratio does not match the window.
  - Decoding uses PreservePixelFormat when possible; rendering uses Fant scaling when shrinking large artwork.

- theme.mp3 — optional; can also be set via launcher_config.json UiMusicPath.

To use an image from chat or another folder without rebuilding: copy it next to the launcher as Assets/launcher_background.png (or set UiBackgroundPath), matching the path in launcher_config.json.
