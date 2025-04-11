# H0stname

## Utility to change the hostname of a Linux machine with colorful options.

### Xterm Monitoring: 
Spawns an `xterm` window showing the status of `systemd-logind.service` and `systemd-hostnamed.service`, which are crucial for managing hostnames on modern Linux systems.

### Validation: 
The script checks if the hostname meets the rules (e.g., no starting or ending hyphens, max length 63, etc.).

### Shell Restart: 
After the hostname change, it offers to restart the shell session to apply the new hostname, but also reminds the user to do it manually if they opt not to restart.


## Improvements
### Systemd Compatibility: 
The script uses `systemd-hostnamed.service` and `systemctl`, which is excellent for systemd-based systems (most modern Linux distros). 
If you wanted to support non-systemd systems, you could include a check and provide an alternative mechanism for setting the hostname.

### Post-Change Actions: 
Consider adding an option for the script to trigger network service restart or other actions that might be necessary for the hostname to take full effect.

### Error Handling with xterm: 
In case xterm or wmctrl is not installed, it could better handle the error gracefully instead of failing the script. This is especially helpful for systems without a graphical interface or minimal setups.















<!-- Providing this material to the world is costing me greatly. -->
