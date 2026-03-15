# Material-Design-3-Dynamic-Mobile-Dashboard

A modern Home Assistant dashboard built on Material Design 3 (MD3) principles. It features a dynamic, transparent, and adaptive card layout with a sleek, clean UI for an elegant smart home experience. This is a complete dashboard that brings together lights, switches, temperature and humidity, rainfall, wind, weather forecasts, alarms, Hue scenes, cameras, heat pumps, door/window sensors, and more—all in one cohesive design.

_v3.1.0_ brings a major visual and functional redesign inspired by Google Home, improving the overall Material Design 3 (MD3) experience. Buttons have been redesigned with new light sliders and switches, including tap and hold actions for quick off or more-info access. The Server page has been reworked to show detailed HAOS and Proxmox info, with battery data merged in. Each room now features climate control, power consumption charts where available, and media player support for rooms with speakers. Most MDI icons have been replaced with Material Symbols, and the font has been updated to Figtree (similar to Google Sans). Old decluttering templates tied to previous button cards have been removed, and a new media_player_card decluttering template has been added. This release focuses on polish, consistency, and usability, making the dashboard cleaner, more functional, and visually cohesive.

# ✨ ToDo
Install Material You Utilities according to this how to: [Material You Utilities](https://github.com/Nerwyn/material-you-utilities)
Add extra_module_url and panel_custom to the configuration.yaml in config folder of the lovelace ui. (This will also allow to change the material design later.)


# ✨ Features

**🎨 MD3 Theme Engine**

Unlock unlimited color combinations with a simple color picker — thanks to the amazing work of Material You Theme repository.

**👥 Per-User Styling**

Each family member can have their own unique style and colors. Perfect for customizing your phone, tablets, and shared devices.

**📱 UI Components**

- Tab Navigations
- Light button sliders
- Other custom buttons
- Waterfall temp/humidity graphs
- Pop-up cards
- Tabs & swipe cards
- Expanders
- Gesture navigation

**💡Community Inspired**

Several cards are inspired by the incredible work of others in the Home Assistant community. Credit will be detailed below.

**🖼️ Screenshots**

<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/fba10b44-d711-4c13-943c-4cb318956a89" />
<img width="1920" height="1080" alt="2" src="https://github.com/user-attachments/assets/03a3cb16-dfeb-48a4-a4e5-7d04a5c92f4f" />


⚠️ Some elements are hidden due to conditional rules, so not everything is visible at once.”)

# 🚀 Requirements / Dependencies

Card Related Stuffs:
- [Alarmo Card](https://github.com/nielsfaber/alarmo-card)
- [Apex Charts Card](https://github.com/RomRider/apexcharts-card?tab=readme-ov-file#series-options)- 
- [Clock Weather Card HUI Icons](https://github.com/pkissling/clock-weather-card)
- [Bubble Card](https://github.com/Clooos/Bubble-Card)
- [Button-Card](https://github.com/custom-cards/button-card)
- [Calendar Card Pro](https://github.com/alexpfau/calendar-card-pro)
- [Expander-Card](https://github.com/MelleD/lovelace-expander-card)
- [LLM Vision Card](https://github.com/valentinfrlch/llmvision-card)
- [Mini-Graph-Card](https://github.com/kalkih/mini-graph-card)
- [Mushroomn](https://github.com/piitaya/lovelace-mushroom)
- [Navbar Card](https://github.com/joseluis9595/lovelace-navbar-card)
- [Timer Bar Card](https://github.com/rianadon/timer-bar-card)
- [Web RTC Camera](https://github.com/AlexxIT/WebRTC)

Theming / ETC:
- [Auto-Entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Card-Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Config Template Card](https://github.com/iantrich/config-template-card)
- [Decluttering Card](https://github.com/custom-cards/decluttering-card)
- [Home Assistant Swipe Navigation](https://github.com/zanna-37/hass-swipe-navigation)
- [Kiosk Mode](https://github.com/maykar/kiosk-mode)
- [Layout-Card](https://github.com/thomasloven/lovelace-layout-card)
- [Lovelace Material Compoonents](https://github.com/giovannilamarmora/lovelace-material-components) - New in v3.1.0
- [Material Symbols](https://github.com/beecho01/material-symbols) - New in v3.1.0
- [Material You Theme](https://github.com/Nerwyn/material-you-theme)
- [Material You Utilities](https://github.com/Nerwyn/material-you-utilities)
- [My Cards Bundle](https://github.com/AnthonMS/my-cards)
- [Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row)
- [Stack In Card](https://github.com/custom-cards/stack-in-card)
- [Scene Presets](https://github.com/Hypfer/hass-scene_presets)
- [Simple Swipe Card](https://github.com/nutteloost/simple-swipe-card)
- [Simple Tabs Card](https://github.com/agoberg85/home-assistant-simple-tabs)
- [Vertical Stack In Card](https://github.com/ofekashery/vertical-stack-in-card)

Weather Related:
- [Lunar Phase Card](https://github.com/ngocjohn/lunar-phase-card)
- [MetService New Zealand Weather](https://github.com/ciejer/metservice-weather)
- [World's Air Quality Index](https://www.home-assistant.io/integrations/waqi/)

Removed in v3.1.0:
- [Advanced Camera Card](https://github.com/dermotduffy/advanced-camera-card)
- [Horizontal Waterfall History Card](https://github.com/sxdjt/horizontal-waterfall-history-card)
- [Local Conditional Card](https://github.com/PiotrMachowski/Home-Assistant-Lovelace-Local-Conditional-card)

# Installation

- Create a blank dashboard to start fresh (optional) or copy some part of the codes or full codes from  [full_YAML](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/full_yaml) into your Home Assistant dashboard.
- **Install the required Frontend Components via HACS**: The easiest way to install the required dependencies listed above is through **HACS (Home Assistant Community Store)**. 
  1. Navigate to **HACS > Frontend**.
  2. Search for the name of each card/theme and click **Download**.
  3. When installed via HACS, it will automatically register the required libraries in your Lovelace resources list. No manual `resources:` configuration is needed.
  4. *Note:* Some add-ons (like Alarmo, Scene Presets, and Web RTC Camera) require installing both the **Integration** (from HACS > Integrations) as well as the **Frontend Card** (from HACS > Frontend).
- You need to adjust the navbar card directory to suit your current dashboard (if you don't start fresh).
- To unlock the full functionality (like weather icons, notification counts, and more), you’ll need to add the corresponding [sensors](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/template%20sensor) to your config.
- For the Hue scene, you'll need to have the automation, scripts, input boolean, input text, and input number in your system that you can find in [hue asset folder](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/hue%20asset). For the images, you can get them from [here](https://github.com/Hypfer/hass-scene_presets/blob/master/custom_components/scene_presets/assets/Readme.md).
- Apply the MD3 theme and select your preferred colors. It is accessible from Overview page > More > Theme Icon

<img width="200" height="180" alt="Dynamic Colors Showcase" src="https://github.com/user-attachments/assets/b7a0166b-edbd-4767-9e13-1623be587465" />

- Select the Transparent option in Card Type to get the wide-system transparent cards
  
![Transparent Card](https://github.com/user-attachments/assets/7d0e3895-edd7-4cd3-88a0-e56f2dbc1ab5)

- Enjoy your personalized dynamic
 dashboard! 🎉

- Set the companion app to full screen (optional)

# 📚 Credits

This project builds upon the work of:
- Nerwyn – [Material You Theme](https://github.com/Nerwyn/material-you-theme) & [Material You Utilities](https://github.com/Nerwyn/material-you-utilities)
- [MySmartHome](https://www.youtube.com/@My_Smart_Home) - for the new simple tabs card, button cards styling, sliders, etc
- Other community members who kindly shared their cards
- [Background Creator](https://www.pexels.com/photo/a-blurry-background-7640905)

# 💖 Support My Work  

If you want to hire me to make your personal dashboard, you can hit me up in [Reddit](https://www.reddit.com/u/ElementZoom/s/dr4NN0mTtj)

Or you support me on [Ko-fi](https://ko-fi.com/ElementZoom).
Your support helps me keep creating and sharing more awesome open-source tools! ✨  

Thank you for being part of this journey 🚀
