# 🚀 Automatic Clicker for Telegram Bot

## ℹ️ Info  

This project automates the process of finding and clicking specific templates in the Telegram Desktop app using PyAutoGUI and OpenCV. The bot is designed to run in the background, detect predefined image templates on the screen and automatically click them to accumulate stars for the user.
## 📝 Description
The Automatic Clicker for Blum uses image recognition techniques to detect template images (such as stars) within the Telegram Desktop window. This script is a automation tool intended for educational purposes, demonstrating the power of computer vision and automation for repetitive tasks.

## ⚠️ Important Disclaimer
**This tool is created solely for educational purposes.**

Please consider the following before using this tool:
1. Using automation to interact with other bots may violate their rules and policies.
2. Bot owners may be against the use of automation, and this may lead to the blocking of your Telegram account or restrictions on access to the bot.
3. Before using the tool, make sure it does not violate any terms of use or user agreements associated with the bot.

The author of this tool is not responsible for any consequences related to its use.

## ✨ Features

 * Template Matching: Uses OpenCV to match predefined templates (images) with the content on the screen, including stars or other objects that need to be clicked.
 * Multithreading Support: Runs template matching and clicking operations concurrently using Python's concurrent.futures to increase efficiency and performance.
 * Window Detection: Automatically identifies and captures the region of the Telegram Desktop window, adjusting to the correct screen area.
 * Dynamic Scaling: Adjusts the size of the captured screenshot and template images based on a defined scale factor for better accuracy in various screen resolutions.

## 💻 Download and Setup 
1. Clone the repository:
```bash
git clone https://github.com/yankkvx/blum-clicker.git
```
 * Create virtual environment:
```bash
python -m venv venv
```
2. Activate the virtual environment:

- On **Windows**:
```bash
venv\scripts\activate
```
- On macOS/Linux:
```bash
source venv/bin/activate
```
3. Install dependencies:
```bash
pip install -r requirements.txt
```
4. Run the code:
```bash
python clicker.py
```

## 🛠️ Technologies Used
-  Python
- PyAutoGUI: For automating mouse clicks and taking screenshots.
- OpenCV: For template matching and image processing.
- NumPy: For array manipulation during image processing.

## 🔄 Updates
- The script now **automatically continues the game** if required. To disable this, comment out the line `('template_6', cv2.imread('template_6.png', cv2.IMREAD_COLOR)),
- **200 stars are consistently collected** in each loop.
- **Automatic window size detection** has been added for improved usability.

## 🧑‍💻 Code Explanation
1. **Window Detection**:  
   The `get_window()` function retrieves the coordinates and dimensions of the Telegram Desktop window by searching for its title. This ensures that the script always interacts with the correct window.
   
2. **Screenshot Capture**:  
   The `grab_screen()` function captures a screenshot of the region defined by the window coordinates, resizing it by a scale factor to optimize performance.
   
3. **Template Matching**:  
   The `find_template_on_screen()` function compares the captured screenshot with predefined templates (such as stars or buttons) to locate their positions. The matching threshold (`step`) defines how accurate the match must be.
   
4. **Clicking**:  
   Once a match is found, the `click_on_screen()` function simulates a mouse click at the center of the detected template's position.
   
5. **Multithreading**:  
   The script uses `ThreadPoolExecutor` to process multiple templates concurrently, increasing the speed and efficiency of the detection and clicking process.
   
6. **Continuous Operation**:  
   The script runs in an infinite loop, constantly checking for matching templates and clicking them, until manually interrupted. The total number of stars clicked is printed on each loop.


## 📷 Demonstration
<div align="center">

![YouCut_20240627_232949474(1)](https://github.com/yankkv17/blum-clicker/assets/166509664/1b0f19f4-1a1b-4d4f-9868-5181af693fee)
<div align="center">

