## Creality Ender 3 Home-Assistant View 
### More_page for dwains-theme
##### Created by Ruben Dijk
---
### Needs:
* octoprint installed on a Raspberry pi 2b or newer.
* Raspberry pi Camera.
* A running Home Assistant
* 3D Printer (I use a creality Ender 3)
* Smartplug (I use a Sonoff S20)

### Installation (dwains-theme)
Add the following to your more_page.yaml file:
change name: 'Printer Name' to your printer name.
Next folow: Installation (split config)

````
      - name: Printer Name
        icon: 'mdi:printer-3d'
        path: 'dwains-theme/addons/more_page/creality_ender/ender3.yaml'
````

### Installation (split config): 
  
1.  Copy the files and place them in the correct location.
2.  If necessary, customize the following files:
    * entities/octoprints/ender3.yaml: ip-address, API, printer name, printer properties
    * entities/cameras/ender3_cam.yaml: still_image_url, mjpeg_url, name, platform if necessary depends on with camera you used.
    * entities/switches/ender3_shutdown.yaml: change 'switch.smartplug_relay' it to your own switch
    * entities/rest_commands/rest_cmd_ender3.yaml: url and X-Api-Key
3.  After doing this check if your configuration (HA) is still valid. 
4.  Reboot HA and you are ready to go.

### configuration.yaml (no split config)
* [Check readme non split](https://github.com/RubenDijk/ender3-home-assistant/blob/master/readme_non_split.md/)

### Screenshots:

**Control Off:**<br>
![Control Off](https://github.com/RubenDijk/ender3-home-assistant/blob/master/view%20control%20off.png "Control Off")

---

**Control On:**<br>
![light](https://github.com/RubenDijk/ender3-home-assistant/blob/master/view%20control%20on.png "Control On")

### Links:
* https://github.com/dwainscheeren/lovelace-dwains-theme
* https://www.home-assistant.io/.
* https://octoprint.org/.

---

If you like my work please feel free to buy me a coffee

<a href="https://www.buymeacoffee.com/RubenDijk" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/white_img.png" alt="Buy Me A Coffee"></a>
