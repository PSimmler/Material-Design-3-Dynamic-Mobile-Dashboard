# Material-Design-3-Dynamic-Mobile-Dashboard

A modern Home Assistant dashboard powered by Material Design 3 (MD3) principles.
Features a dynamic, transparent, and adaptive card layout with a sleek, clean UI for an elegant smart home experience.

[v2.1.0](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/releases/tag/v2.1.0) introduces an Apex Chart card for visualizing rainfall forecasts, adds daily and hourly rain forecast details, includes a Lunar Phase card, and adds several new template sensors to capture hourly weather data.

# ✨ Features

**🎨 MD3 Theme Engine**

Unlock unlimited color combinations with a simple color picker — thanks to the amazing work of Newryn’s Material You Theme repository.

**👥 Per-User Styling**

Each family member can have their own unique style and colors. Perfect for customizing your phone, tablets, and shared devices.

**📱 UI Components**

- Light button sliders
- Light button
- Waterfall graphs
- Pop-up cards
- Tabs & swipe cards
- Expanders
- Gesture navigation

**💡Community Inspired**

Several cards are inspired by the incredible work of others in the Home Assistant community. Credit will be detailed below.

**🖼️ Screenshots**

<img width="1920" height="1080" alt="Full Dashboard Showcase" src="https://github.com/user-attachments/assets/af4ef9d3-0269-499e-9f4f-3817f01b0691" />

⚠️ Some elements are hidden due to conditional rules, so not everything is visible at once.”)

# 🚀 Requirements / Dependencies

- [Advanced Camera Card](https://github.com/dermotduffy/advanced-camera-card)
- [Alarmo](https://github.com/nielsfaber/alarmo)
- [Alarmo Card](https://github.com/nielsfaber/alarmo-card)
- [Apex Charts Card](https://github.com/RomRider/apexcharts-card?tab=readme-ov-file#series-options)
- [Auto-Entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Bubble Card](https://github.com/Clooos/Bubble-Card)
- [Button-Card](https://github.com/custom-cards/button-card)
- [Calendar Card Pro](https://github.com/alexpfau/calendar-card-pro)
- [Card-Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Clock Weather Card HUI Icons](https://github.com/pkissling/clock-weather-card)
- [Config Template Card](https://github.com/iantrich/config-template-card)
- [Decluttering Card](https://github.com/custom-cards/decluttering-card)
- [Expander-Card](https://github.com/MelleD/lovelace-expander-card)
- [Home Assistant Swipe Navigation](https://github.com/zanna-37/hass-swipe-navigation)
- [Horizontal Waterfall History Card](https://github.com/sxdjt/horizontal-waterfall-history-card)
- [Kiosk Mode](https://github.com/maykar/kiosk-mode)
- [Layout-Card](https://github.com/thomasloven/lovelace-layout-card)
- [LLM Vision](https://github.com/valentinfrlch/ha-llmvision)
- [LLM Vision Card](https://github.com/valentinfrlch/llmvision-card)
- [Local Conditional Card](https://github.com/PiotrMachowski/Home-Assistant-Lovelace-Local-Conditional-card)
- [Lunar Phase Card](https://github.com/ngocjohn/lunar-phase-card)
- [Material You Theme](https://github.com/Nerwyn/material-you-theme)
- [Material You Utilities](https://github.com/Nerwyn/material-you-utilities)
- [MetService New Zealand Weather](https://github.com/ciejer/metservice-weather)
- [Mini Media PLayer](https://github.com/kalkih/mini-media-player)
- [Mini-Graph-Card](https://github.com/kalkih/mini-graph-card)
- [Mushroomn](https://github.com/piitaya/lovelace-mushroom)
- [My Cards Bundle](https://github.com/AnthonMS/my-cards)
- [Navbar Card](https://github.com/joseluis9595/lovelace-navbar-card)
- [Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row)
- [Scene Presets](https://github.com/Hypfer/hass-scene_presets)
- [Swipe Simple Card](https://github.com/nutteloost/simple-swipe-card)
- [Stack In Card](https://github.com/custom-cards/stack-in-card)
- [Timer Bar Card](https://github.com/rianadon/timer-bar-card)
- [Vertical Stack In Card](https://github.com/ofekashery/vertical-stack-in-card)
- [World's Air Quality Index](https://www.home-assistant.io/integrations/waqi/)

# Installation

- Create a blank dashboard to start fresh (optional) or copy some part of the codes or full codes from  [full_YAML](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/full_yaml) into your Home Assistant dashboard.
- Install the required HACS components (such as swipe-card, stack-in-card, popup-card, etc. — see your setup for what’s needed).
- You need to adjust the navbar card directory to suit your current dashboard (if you don't start fresh).
- To unlock the full functionality (like weather icons, notification counts, and more), you’ll need to add the corresponding [sensors](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/template%20sensor) to your config.
- For the Hue scene, you'll need to have the automation, scripts, input boolean, input text, and input number in your system that you can find in [hue asset folder](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/hue%20asset)
- Apply the MD3 theme and select your preferred colors. It is accessible from Home > More > Theme Icon

<img width="200" height="180" alt="Dynamic Colors Showcase" src="https://github.com/user-attachments/assets/b7a0166b-edbd-4767-9e13-1623be587465" />

- Select the Transparent option in Card Type to get the wide-system transparent cards
  
![Transparent Card](https://github.com/user-attachments/assets/7d0e3895-edd7-4cd3-88a0-e56f2dbc1ab5)

- Enjoy your personalized dynamic
 dashboard! 🎉

- Set the companion app to full screen (optional)

# 📚 Credits

This project builds upon the work of:
- Newryn – [Material You Theme](https://github.com/Nerwyn/material-you-theme) & [Material You Utilities](https://github.com/Nerwyn/material-you-utilities)
- [MySmartHome](https://www.youtube.com/@My_Smart_Home) - for button cards styling, sliders, etc
- Other community members who kindly shared their cards
- [Background Creator](https://www.pexels.com/photo/a-blurry-background-7640905)

# 💖 Support My Work  

If you want to hire me to make your personal dashboard, you can hit me up in [Reddit](https://www.reddit.com/u/ElementZoom/s/dr4NN0mTtj)

Or you support me on [Ko-fi](https://ko-fi.com/ElementZoom).  
Your support helps me keep creating and sharing more awesome open-source tools! ✨  

Thank you for being part of this journey 🚀
