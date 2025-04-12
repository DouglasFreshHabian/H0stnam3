# [![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=19&pause=1000&color=00F705&center=true&width=435&lines=Linux+Hostname+Changer+💻;Command+Line+Junky+💊;Crappy+Bash+Script+Writer+🗒;Seeker+Of+Linux+Knowledge+📚)](https://git.io/typing-svg)

<h1 align="center"> 
📛 Utility to Change the Hostname of a Linux Machine 🤖
</h1>

## Let's Take a Look:👀
```bash
   ./hostname.sh --help
          __            __                            __
         / /  ___  ___ / /____  ___ ___ _  ___   ___ / /
        / _ \/ _ \(_-</ __/ _ \/ _ `/  ' \/ -_) (_-</ _ \
       /_//_/\___/___/\__/_//_/\_,_/_/_/_/\__(_)___/_//_/
      ___________________________________________________
                       FRESH FORENSICS

Usage: ./hostname.sh <options>
Options:
  -h, --help               Show this help menu.
  -w, --wordlist <path>    Provide a wordlist to generate a hostname.
  -n, --name <hostname>    Manually provide a hostname.
  -r, --random             Generate a random 12-character alphanumeric hostname.
  -l, --log                Enable verbose logging of the hostname change.
  -a, --about              Show the rules for creating a valid hostname.
  -b, --banner		   Display the ascii banner.
```
### To Better Understand the Rules On Linux Hostname Creation:📐
```bash
   ./hostname.sh --about

          __            __                            __
         / /  ___  ___ / /____  ___ ___ _  ___   ___ / /
        / _ \/ _ \(_-</ __/ _ \/ _ `/  ' \/ -_) (_-</ _ \
       /_//_/\___/___/\__/_//_/\_,_/_/_/_/\__(_)___/_//_/
      ___________________________________________________
                       FRESH FORENSICS

Rules for creating a hostname:
1. The hostname must be composed of up to 64 7-bit ASCII lower-case alphanumeric characters or hyphens.
2. The hostname should not contain any dots (only a single label).
3. The hostname cannot start or end with a hyphen.
4. The hostname can contain only alphanumeric characters (a-z, 0-9) and hyphens (-).
5. The hostname cannot be longer than 63 characters.
```

### Xterm Monitoring:🔍
Spawns an `xterm` window showing the status of `systemd-logind.service` and `systemd-hostnamed.service`, which are crucial for managing hostnames on modern Linux systems.

### Validation:🕵️ 
The script checks if the hostname meets the rules (e.g., no starting or ending hyphens, max length 63, etc.).

### Shell Restart:🐚
After the hostname change, it offers to restart the shell session to apply the new hostname, but also reminds the user to do it manually if they opt not to restart.

## Example Usage:📖
Inside of the dictionaries directory, there are several wordlists:
```bash
   ./hostname.sh --wordlist dictionaries/dogs

          __            __                            __
         / /  ___  ___ / /____  ___ ___ _  ___   ___ / /
        / _ \/ _ \(_-</ __/ _ \/ _ `/  ' \/ -_) (_-</ _ \
       /_//_/\___/___/\__/_//_/\_,_/_/_/_/\__(_)___/_//_/
      ___________________________________________________
                       FRESH FORENSICS

Chosen hostname from wordlist:rottie
Do you want to proceed with the new hostname: pearl? (y/n): y
Applying new hostname:pearl
[######################################]
[####################################################]
[###########################################]
_______________________________________________________

Successfully changed the hostname to :pearl!
_______________________________________________________

Do you want to restart your shell session now? (y/n): y
---------------------------------------------------->
Bonus Tip! Here's another way to get the hostname:
  Command: sysctl kernel.hostname
  Output:
                      __
   ___  ___ ___ _____/ /
  / _ \/ -_) _ `/ __/ / 
 / .__/\__/\_,_/_/ /_/  
/_/  

```

## Improvements:🛠
### Systemd Compatibility:⚙️ 
The script uses `systemd-hostnamed.service` and `systemctl`, which is excellent for systemd-based systems (most modern Linux distros). 
If you wanted to support non-systemd systems, you could include a check and provide an alternative mechanism for setting the hostname.

### Post-Change Actions:📬 
Consider adding an option for the script to trigger network service restart or other actions that might be necessary for the hostname to take full effect.

### Error Handling with xterm:❌ 
In case xterm or wmctrl is not installed, it could better handle the error gracefully instead of failing the script. This is especially helpful for systems without a graphical interface or minimal setups.















<!-- Providing this material to the world is costing me greatly. -->
