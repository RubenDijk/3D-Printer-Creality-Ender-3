# Creality Ender 3 Home-Assistant View
Needs:

OctoPrint installed on a Raspberry pi 2b or newer.
Raspberry Pi Camera.
Home Assistant.
a 3d printer (I use a creality ender 3).
smart plug (I use a sonoff S20).
  
installation:
  
Copy the files and place them in the correct location.
If necessary, customize the following files with ip-address, smartplug name. printer properties
After doing this check if your configuration (HA) is still valid. 
  
When using split config:
Copy the content from the folders to the correct folders

configuration.yaml (no split config)

octoprint: (configuration.yaml)
camera: (configuration.yaml)
place switch under the switch: (configuration.yaml)
place the automation under automation.yaml
Place everything from the scripts folder under script.yaml 

Example
script.yaml

script:
- ender3_cancel_print:
  alias: Ender3 Cancel
  sequence:
    - service: rest_command.ender3_job_command
      data:
        payload: '{"command": "cancel"}''.

- ender3_change_filament:
  alias: Ender3 Filament Change
  sequence:
    - service: rest_command.ender3_printer_command
      data:
        cmd: "M600"
  
Reboot HA and you are ready to go.
  
Links:
https://www.home-assistant.io/.
https://octoprint.org/.
