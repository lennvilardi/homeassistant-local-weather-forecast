# Home Assistant 12-Hour Local Weather Forecast (~94% Accurate*)

This Home Assistant integration creates sensors to forecast local weather without relying on external services. It provides accurate weather data for the next 12 hours, avoiding issues with changing services or APIs. Only a barometer is required (which can also be sourced online), but accuracy can be improved with additional sensors.

I find the Zambretti forecaster to be quite accurate, but you may need to monitor both models to determine which works better for your location.

If you like this repository, please leave a star ⭐

# Features
* Two Forecaster Models (Zambretti + Negretti and Zambra)
  (You may need to adjust the card to use the other model, depending on which is more accurate for your location.)
* Rain probability
* Approximate timestamps for weather changes (After a reboot, it may take some time for these to become accurate.)
* Text prognosis
* Simple temperature forecast
* Extraction of general weather conditions
* Full English and German support (Italian re-added, and French added)

# Sensors
The following sensors can be used:
* Barometer (required)
* Temperature (optional, set value to 0 if missing)
* Wind speed (optional)
* Wind direction (optional)

# Card
English / German and French versions:

![grafik](https://github.com/HAuser1234/homeassistant-local-weather-forecast/assets/122117318/3a4cb58b-617f-4a9a-8fb2-ec723a5b05c0)
![grafik](https://github.com/HAuser1234/homeassistant-local-weather-forecast/assets/122117318/19c8220a-4bfe-4a0f-a82a-c968cbfd5b31)
![2024-08-20 17_16_33-Tableau de bord – Home Assistant — Mozilla Firefox](https://github.com/user-attachments/assets/5fb28ddc-0e33-45f7-8477-1bd4d6afd37a)


# Installation
Please contribute any upgrades to the card or algorithm; this helps everyone!

* Copy `weather_forecast.yaml` into your custom YAML integrations folder.

How to create an integrations folder:
1. Add this to your `configuration.yaml`:

```yaml
homeassistant:
  packages: !include_dir_named integrations
```

2. Create a folder named `integrations` in your config directory.
3. Copy `weather_forecast.yaml` into this folder.

* Make changes for your individual setup (edit the settings marked in `weather_forecast.yaml`).
* Copy the card as a manual YAML config into Lovelace. *Mushroom required, vertical-stack-in-card required!*
* Edit the current solar production entity in the conditional cards.

# To-Do
* Improve algorithms
* Find bugs (please submit changes!)
* Create a better temperature forecast
* Consider integrating with a solar/battery charge prediction tool: https://github.com/HAuser1234/Homeassistant-solar-forecast-charge-prediction

# Sources
https://github.com/sassoftware/iot-zambretti-weather-forcasting  
https://integritext.net/DrKFS/zambretti.htm  
https://www.mikrocontroller.net/topic/385242  
http://www.beteljuice.co.uk/zambretti/forecast.html

*94% accuracy according to https://github.com/sassoftware/iot-zambretti-weather-forcasting*

---

**THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT.**

Voici la version française du texte :

---

# Prévision Météo Locale sur 12 Heures pour Home Assistant (~94% de Précision*)

Cette intégration Home Assistant crée des capteurs pour prévoir la météo locale sans avoir besoin de services externes. Cela permet d'obtenir des données météo précises pour les 12 heures à venir, sans les problèmes liés aux services ou API changeants. Un baromètre est le seul capteur requis (il peut également être récupéré en ligne), mais la précision peut être améliorée avec des capteurs supplémentaires.

Je trouve le prévisionniste Zambretti assez précis, mais il est conseillé de surveiller les deux modèles pour déterminer celui qui fonctionne le mieux dans votre région.

Si vous aimez ce dépôt, n'hésitez pas à laisser une étoile ⭐

# Fonctionnalités
* Deux Modèles de Prévision (Zambretti + Negretti et Zambra)
  (Vous devrez peut-être ajuster la carte pour utiliser l'autre modèle, selon celui qui est le plus précis dans votre région.)
* Probabilité de pluie
* Estimation des horaires de changement de météo (Après un redémarrage, il peut falloir un certain temps pour que ces prévisions soient précises.)
* Prévision textuelle
* Prévision simple des températures
* Extraction des conditions météorologiques générales
* Support complet en anglais et en allemand (italien réintégré, et ajout du français)

# Capteurs
Les capteurs suivants peuvent être utilisés :
* Baromètre (obligatoire)
* Température (optionnel, mettre la valeur à 0 si manquant)
* Vitesse du vent (optionnel)
* Direction du vent (optionnel)

# Carte
Version anglaise et allemande :

![grafik](https://github.com/HAuser1234/homeassistant-local-weather-forecast/assets/122117318/3a4cb58b-617f-4a9a-8fb2-ec723a5b05c0)
![grafik](https://github.com/HAuser1234/homeassistant-local-weather-forecast/assets/122117318/19c8220a-4bfe-4a0f-a82a-c968cbfd5b31)

# Installation
Merci de contribuer à toute amélioration de la carte ou de l'algorithme, cela aide tout le monde !

* Copiez `weather_forecast.yaml` dans votre dossier d'intégrations personnalisées YAML.

Comment créer un dossier d'intégrations :
1. Ajoutez ceci à votre `configuration.yaml` :

```yaml
homeassistant:
  packages: !include_dir_named integrations
```

2. Créez un dossier nommé `integrations` dans votre répertoire de configuration.
3. Copiez `weather_forecast.yaml` dans ce dossier.

* Apportez des modifications pour votre configuration individuelle (modifiez les paramètres indiqués dans `weather_forecast.yaml`).
* Copiez la carte en tant que configuration YAML manuelle dans Lovelace. *Mushroom requis, vertical-stack-in-card requis !*
* Modifiez l'entité de production solaire actuelle dans les cartes conditionnelles.

# À Faire
* Améliorer les algorithmes
* Trouver des bugs (merci de soumettre les modifications !)
* Créer une meilleure prévision de température
* Envisager l'intégration avec un outil de prévision de charge solaire/batterie : https://github.com/HAuser1234/Homeassistant-solar-forecast-charge-prediction

# Sources
https://github.com/sassoftware/iot-zambretti-weather-forcasting  
https://integritext.net/DrKFS/zambretti.htm  
https://www.mikrocontroller.net/topic/385242  
http://www.beteljuice.co.uk/zambretti/forecast.html

*Précision de 94% selon https://github.com/sassoftware/iot-zambretti-weather-forcasting*

---

**LE LOGICIEL EST FOURNI "EN L'ÉTAT", SANS AUCUNE GARANTIE, EXPRESSE OU IMPLICITE, Y COMPRIS MAIS SANS S'Y LIMITER, LES GARANTIES DE QUALITÉ MARCHANDE, D'ADÉQUATION À UN USAGE PARTICULIER ET D'ABSENCE DE CONTREFAÇON.**
