## ⚽_football_card_pt_⚽

Football Lives, Results and Leaderboards on a Lovelace Card (Home Assistant).
 - Allows Telegram notifications and automations triggered by a simple goal from the favorite team.

Credits to:
Joel Mendes (https://github.com/tv4you2016) for the contribution in reviewing all the files.
Pedro Miguel Fernandes (https://github.com/pmfernandes) for the contribution with some functions nodes.

# Pre-requisites:

All these dependencies can be installed through Add-ons / Hacs

| Plugin | README |
| ------ | ------ |
| Node-RED | https://github.com/hassio-addons/addon-node-red |
| custom:swipe-card | https://github.com/bramkragten/swipe-card |
| lovelace-card-mod | https://github.com/thomasloven/lovelace-card-mod |
| stack-in-card | https://github.com/custom-cards/stack-in-card |

# Installation (Step by Step):
1. Copy all the images to your folder (<i>www/images</i>) in Home Assistant.<p>
2. Create the two input selects (<i>menu_futebol</i> and <i>menu_competição</i>):
- If you use <a href="https://www.home-assistant.io/docs/configuration/packages/">"<i>packages</i>"</a> change the "<i>input_select.yaml</i>" name file (not extension and it's not mandatory) and copy to your packages directory.<br>
- If you not use <a href="https://www.home-assistant.io/docs/configuration/packages/">"<i>packages</i>"</a> copy the code in the "<i>input_select.yaml</i>" file to your "<i>configuration.yaml</i>" file.<p>
3. Check configuration in "<i>developer tools</i>" menu and if "its ok", restart the Home Assistant.<p>
4. Go to Node-RED menu, click on the icon with 3 bars on the top right side and choose the "<i>Import</i>" option.<p>
5. Open the "<i>football_flows.json</i>" file and copy all the code to your "import area" in Node-Red. Import!<p>
6. Update all the palettes needed to use the flow.<p>
7. In the flow, its only necessary to update the credentials of your Telegram in "<i>Notificações - JOGOS</i>", node "<i>Telegram Bot</i>". Deploy!<p>
8. Go to Frontend Lovelace and copy all the code in the "<i>lovelace_card.yaml</i>" file to a new custom card.

# Notes:
1. To create automations to interact with the goal of the favorite team go to the flow (Node-Red), first group ("<i>Insert Data</i>") open node 8 and change the name of the favorite team. Then, go to the last group ("Automações ao Golo da Equipa Favorita") and change or add the actions you want depending on the goal 1, 2, 3 etc etc.<p>
2. Sometimes it is necessary to update the "selectors" (numbers 4, 5, 6 and 7 in "<i>Inserir Dados</i>" group) related to the "http requests" made.<br>
 <b>So, if for some reason you are having problems updating the results, check that the selectors you have are the same as the following:</b>

# Update Selectors:
4. #content-center > div.Ja > div.pb, div.Vc.Zc<br>
5. #content-center > div.Ja > div.Vc.Zc<br>
6. td.ve<br>
7. td.we

Enjoy!

<a href="https://www.buymeacoffee.com/PCardoso7" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>

# Main Card View (Results):
![football_results](https://user-images.githubusercontent.com/116345010/197203477-d9219fc9-8da0-44f0-96a8-dccffcc964f8.jpg)

# Main Card View (Lives):
![football_live](https://user-images.githubusercontent.com/116345010/197215915-1c9eb672-5cd0-4d77-8fcb-f80232b47e24.jpg)

# Main Card View (Leaderboards):
![football_standings](https://user-images.githubusercontent.com/116345010/197203818-abd633a4-2d1a-4e26-90a4-6441a04a6859.jpg)
