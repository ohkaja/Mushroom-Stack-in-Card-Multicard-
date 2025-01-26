# Mushroom-Stack-in-Multicard
Puts some more information in a borderless small container. Its to be used in Homeassistant lovelace. See example code for one (room)card

Lovelace Plugins needed:
* Mushroom Cards => https://github.com/piitaya/lovelace-mushroom
* Stack-in-Card => https://github.com/custom-cards/stack-in-card
* Card-Mod => https://github.com/thomasloven/lovelace-card-mod
* Mini-Graph-Card => https://github.com/kalkih/mini-graph-card
* Volkswagen CARNET => https://github.com/robinostlund/homeassistant-volkswagencarnet
* Modbus
* REST Command

# Create a simplified Floorplan/ Cardspace
🎥 <a href="https://youtu.be/XtIilQJFz8U">Video demo Youtube</a>
<p></p>
<img width="282" alt="image" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/9f031b67-a714-46ef-aaa9-bedfae351f59">

# Room example
<img width="377" alt="image" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/70d2fc2c-36c7-48e3-82b5-9e64234871e0">
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/example%20room">Code</a>

# Energymeter example
<img width="379" alt="image" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/3628344f-e9bb-4729-91d1-af24ab37e152">
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/example%20energymeter">Code</a>

# Animated Energymeter example
<img width="382" alt="image" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/5782324a-f9d8-4bee-aea1-6ac33fdac23c">
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/animated-live-sensor-activity">Code</a>


# Media Room example
<img width="379" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/c4884ad9-ed76-4174-8f87-52e9a16b85c6">
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/media%20room%20example">Code</a>

# Tankerkoenig Card
<img width="379" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/315f718a-9d13-498a-84dc-270dc3613523">
<p></p>
<a href=https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/Tankerkoenig-Mushroom-Card>Code</a>

# PV Picturecard
<img width="379" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/093cd52e-b2af-4c9d-853e-bae234fa9619">
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/PV%20Picturecard">Code</a>

# Dynamic SOC Card
<img width="379" src="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/6534012b-7d70-40c2-afd9-e89f258f1574">
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/dynamic-SOC-card">Code</a>

# Multilayer Floorplan
![Unbenannt-1](https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/assets/93218188/0eaca95d-f13f-4b2b-a810-dc9f8615f65c)
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/example%20floorplan">Code</a>

# Car Card with additional informations and loacation
<img width="372" alt="image" src="https://github.com/user-attachments/assets/bb2a956b-4d41-4b5d-a8a3-43a80c3ff20b">
<p></p>
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/example%20Volkswagen-Carnet">Code</a>


# Carnet Siri Commands
https://github.com/user-attachments/assets/35cf9a42-ba64-4048-a0a5-640dfaa662bf
<p></p>
Needs an open/ close automation or an combined (trigger ID) automation to work.
<a href="https://github.com/ohkaja/Mushroom-Stack-in-Card-Multicard-/blob/main/example%20Volkswagen%20Carnet%20Siri%20command">Code Siri commands</a>

# KOSTAL Enector steering via REST-API
Thx to <a href="https://community.home-assistant.io/u/thronramses/summary">ThronRamses</a>! :*

First of all, it’s not perfect, but it works well for everyday charging. ⚡😊
It’s a combination of REST commands sent to the API (KSEM 2.5.0 and later) and reading the status codes via Modbus. 🖥️📡
It's important to not use KSEM to set battery usage and phase usage. ❌🔋 Instead, use the REST commands, which you will have after implementing this. ✅📑

To make this work, a KSEM API key must be obtained 🔑, and some sensors need to be created.

To understand what’s going on, you can take a view on 🔍 <a href="https://cdn-production.kostal.com/-/media/document-library-folder---kse/2023/11/20/15/10/ba_kostal_interface_ksem_de.pdf">KSEM Modbus documentation</a>

**=> DEMO** https://github.com/user-attachments/assets/69dd1d14-e9cd-44bc-93cc-d5a46ec084ea

**Lets Start:**

1. Login to your KSEM and press on the profile icon on the upper right corner and select "Accesskey".
   <p><img width="146" alt="image" src="https://github.com/user-attachments/assets/1bbec941-d0e5-414f-9ac0-1ac70cd112a5" /></p> 🔑
3. Add a Accesskey "admin", then **copy** the shown key asap. There´s no way to show it again.
4. Activate the Key (yellow key icon beside the new key).
5. Put the key in your secrets.yaml as
   wallbox_api_token: Bearer eyJhbGciOiJSUzI[...]lqMnBknqs4uFnyFSw
6. Add the modbus sensor like in <a href="enector_template_sensoren">enector_modbus_registers</a> described.
   * wallbox_lademodus_modbus (40994) number indexing the active charging mode (site 19/29 of documentation)
   * wallbox_statuscode_modbus (49206) number indexing statuscode of the wallbox (site 22/23 of documentation)
   * wallbox_ladeleistung_modbus (49246) active load in Watts if charging
   * wallbox_energieverbrauch (49254) sum of debleeded Watts for Energydashboard
7. Add the REST commands like in <a href="enector_rest_full_commands">enector_rest_full_commands</a> described. Naming is "speaking".
   * wallbox_set_lock_mode        
   * wallbox_set_solar_pure_mode 
   * wallbox_set_solar_plus_mode
   * wallbox_set_power_mode
   * wallbox_set_homebattery_on
   * wallbox_set_homebattery_off
   * wallbox_set_phase_three
   * wallbox_set_phase_one
8. Add the Template sensors like in <a href="enector_template_sensoren">enector_rest_full_commands</a> described.
   * wallbox_lademodus_friendly (numbers from **wallbox_lademodus_modbus** to: Lock Mode (1), Power Mode (2), Solar Pure Mode (3), Solar Plus Mode (4)
   * wallbox_statuscode_friendly (numbers from **wallbox_statuscode_modbus** to: Kein Fahrzeug verbunden (1), Fahrzeug verbunden (2), Ladevorgang pausiert (3), Ladevorgang wird initialisiert (4), Läd (5), Kommunikation unterbrochen (6), Servicemodus (7).
   * wallbox_homebattery_mode (usage of homebattery for ev or not)
   * wallbox_phase_usage (3 or 1 phase usage [if applicable])
9. Add the lovelace yaml to on of your dashboards <a href="enector_lovelace">enector_lovelace</a>.
10. Done. ✅ You’ll now be able to fully remote your Enector through Home Assistant.







