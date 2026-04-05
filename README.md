# 💡 LumiSense: Automated Street Light Control System

## 📖 Overview
**LumiSense** is a pure hardware-based digital circuit design project aimed at automatically adjusting the brightness of streetlights. Developed to reduce industrial operational costs, this project addresses the lack of appropriate lighting control, prevents premature bulb degradation from overworking, and eliminates the need for manual adjustments.

## ⚙️ How It Works (System Architecture)
The system operates entirely on hardware logic without the need for microcontrollers or software programming. It is divided into three main stages:

1. **Sensing & Comparing:** * Uses a Light Dependent Resistor (LDR) combined with a voltage divider circuit to measure ambient light levels.
   * An Operational Amplifier (**LM358**) is then used as a comparator to evaluate the voltage levels.
2. **Logic Processing:** * The signals from the comparator are processed through logic gates (**M74HC08** AND Gate and **74HC04** NOT Gate).
   * This logic network defines and categorizes the lighting requirements into 4 distinct levels.
3. **Output Control:** * A Timer IC (**NE555**) receives the logic states and generates Pulse Width Modulation (PWM) signals corresponding to the 4 defined levels.
   * These PWM signals are used to smoothly dim or brighten the streetlights.

> **📊 Dashboard Monitoring:** The system also includes a dashboard interface to monitor the current luminance value (in lux) and display the real-time status of the 4 lighting levels.

## 🌟 Key Advantages

* **🚫 No Microcontroller (MCU) Needed:** By relying entirely on fundamental digital circuits, the system significantly reduces complexity, increases operational stability, and lowers manufacturing costs.
* **⚡ Ultimate Energy Efficiency with PWM:** Utilizing PWM signals to control brightness (instead of direct voltage reduction) ensures highly efficient light control. This minimizes energy loss as heat and significantly extends the lifespan of the LED bulbs.

## 🛠️ Hardware Components
* **Sensors:** LDR (Light Dependent Resistor)
* **Op-Amp / Comparator:** LM358
* **Logic Gates:** AND Gate (M74HC08), NOT Gate (74HC04)
* **Timer / PWM Generator:** NE555
