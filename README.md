<h1 align="center"> 
🤖 Utility to Change the Hostname of a Linux Machine 📛
</h1>

![Carbon Terminal Photo](https://github.com/DouglasFreshHabian/H0stnam3/blob/main/Graphics/carbon7.png)

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=00D408&width=435&lines=Linux+Hostname+Randomnizer;Terminal+Typing+Addict+%F0%9F%92%89;Bash+Shell+Divider;Linux+Filesystem+Dancer;Terminal+Emulator+Creator" alt="Typing SVG" /></a>

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=F74300&width=435&lines=Linux+Hostname+Changer;Linux+Command+Line+Junky;Seeker+Of+Linux+Knowledge;Wordlist+Cleaner+%26+Creator;Terminal+Window+Splitter+" alt="Typing SVG" /></a>

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=200&pause=1000&color=4300F7&width=435&lines=64+7-bit+ASCII+lower-case+;alphanumeric+characters+or+hyphens;should+not+contain+any+dots;cannot+start+or+end+with+a+hypen;alphanumeric+characters+(a-z%2C+0-9)+;cannot+be+longer+than+63+characters" alt="Typing SVG" /></a>











## Let's Take a Look: 👀

## To Better Understand the Rules On Linux Hostname Creation: 📐
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

### Xterm Monitoring: 🔍
Spawns an `xterm` window showing the status of `systemd-logind.service` and `systemd-hostnamed.service`, which are crucial for managing hostnames on modern Linux systems.

### Validation: 🕵️ 
The script checks if the hostname meets the rules (e.g., no starting or ending hyphens, max length 63, etc.).

### Shell Restart: 🐚
After the hostname change, it offers to restart the shell session to apply the new hostname, but also reminds the user to do it manually if they opt not to restart.

## Example Usage: 📖
Inside of the dictionaries directory, there are several wordlists:
```bash
   ./hostname.sh --wordlist dictionaries/dogs

          __            __                            __
         / /  ___  ___ / /____  ___ ___ _  ___   ___ / /
        / _ \/ _ \(_-</ __/ _ \/ _ `/  ' \/ -_) (_-</ _ \
       /_//_/\___/___/\__/_//_/\_,_/_/_/_/\__(_)___/_//_/
      ___________________________________________________
                       FRESH FORENSICS

Chosen hostname from wordlist:pearl
Do you want to proceed with the new hostname: pearl? (y/n): y
Applying new hostname: pearl
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

## Improvements: 🛠
### Systemd Compatibility: ⚙️ 
The script uses `systemd-hostnamed.service` and `systemctl`, which is excellent for systemd-based systems (most modern Linux distros). 
If you wanted to support non-systemd systems, you could include a check and provide an alternative mechanism for setting the hostname.

### Post-Change Actions: 📬 
Consider adding an option for the script to trigger network service restart or other actions that might be necessary for the hostname to take full effect.

### Error Handling with xterm: ❌ 
In case xterm or wmctrl is not installed, it could better handle the error gracefully instead of failing the script. This is especially helpful for systems without a graphical interface or minimal setups.









#### If you have not done so already, please head over to the channel and hit that subscribe button to show some support. Thank you!!!

<h2 align="center">
👍 [SUPPORT FRESH!](www.youtube.com/@DouglasHabian-tq5ck) 
</h2>



<!-- 
 ____    ___   ____    ____                 _ 
|  _ \  |_ _| |  _ \  |  _ \ ___  __ _ _ __| |
| |_) |  | |  | |_) | | |_) / _ \/ _` | '__| |
|  _ < _ | | _|  __/  |  __/  __/ (_| | |  | |
|_| \_(_)___(_)_| (_) |_|   \___|\__,_|_|  |_|
                                                                                                                            
 _____              _       _____                        _          
|  ___| __ ___  ___| |__   |  ___|__  _ __ ___ _ __  ___(_) ___ ___ 
| |_ | '__/ _ \/ __| '_ \  | |_ / _ \| '__/ _ \ '_ \/ __| |/ __/ __|
|  _|| | |  __/\__ \ | | | |  _| (_) | | |  __/ | | \__ \ | (__\__ \
|_|  |_|  \___||___/_| |_| |_|  \___/|_|  \___|_| |_|___/_|\___|___/
        dfresh@tutanota.com Fresh Forensics, LLC 2025 -->

<!-- Providing this material to the world is costing me greatly. -->
