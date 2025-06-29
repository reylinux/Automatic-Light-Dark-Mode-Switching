Managing visibility in Home Assistant dashboards can be tricky, especially when trying to maintain usability during both daytime and nighttime. I’ve created two separate dashboards — one optimized for light mode and one for dark mode — to tackle this.
![Banner](https://github.com/user-attachments/assets/69eff534-a4cd-4fb8-8fb9-6f68de6ffc8b)


After a lot of trial and error, research, AI experimentation, and help from the app developer, I finally found a reliable way to automate the switching between them.

**🛠️ The Solution**

The method involves:
- Scheduling specific times of day to switch between modes
- Restarting the Home Assistant app at those times
- Using startup logic to load the correct dashboard/theme (light or dark)
- An automation and a rest_command that you'll put in your configuration YAML files

These are included in:

- [automation.yaml](https://github.com/reylinux/Automatic-Light-Dark-Mode-Switching/blob/main/automation.txt) – time-based triggers to restart the app
- [configuration.yaml](https://github.com/reylinux/Automatic-Light-Dark-Mode-Switching/blob/main/rest_command.txt) – a rest_command to switch dashboards after restart. You need to put this in your configuration.yaml

While not the most elegant method, it’s proven to be stable and consistent, especially compared to more dynamic UI hacks that break on reload or sleep states.

If you’re facing similar issues with visual consistency or dashboard legibility — give this a try!

