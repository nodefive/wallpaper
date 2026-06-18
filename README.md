# Dynamic Time-based Wallpaper

A Bash script that automatically updates your GNOME desktop wallpaper based on the current time of day.

## Features
- Divides the day into multiple periods: Dawn, Morning, Afternoon, Dusk, and Night.
- Selects a random image (`.jpg`, `.jpeg`, `.png`) from the corresponding folder in your pictures directory.
- Automatically applies the wallpaper using `gsettings` for GNOME desktop environments.

## Directory Structure
Ensure your wallpapers are organized in the following directories:
- `~/Pictures/Wall/Morning`
- `~/Pictures/Wall/Afternoon`
- `~/Pictures/Wall/DuskDawn`
- `~/Pictures/Wall/Night`

## Usage
Run the script to immediately update your wallpaper based on the current time:
```bash
chmod +x wallpaper
wallpaper
```

## How to Automate with Cron
To have your wallpaper change automatically as the day progresses, you can add the script to your user's crontab.

1. Open your crontab editor:
   ```bash
   crontab -e
   ```

2. Add the following line at the end of the file to run the script every 15 minutes (replace `/path/to/wallpaper/script/` with the actual path where the script is located):
   ```cron
   */15 * * * * /path/to/wallpaper/script/wallpaper > /dev/null 2>&1
   ```

3. Save and exit. The script will now run in the background every 15 minutes and update your wallpaper according to the time ranges defined.

## License

MIT License — Copyright (c) 2025 nodefive

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
