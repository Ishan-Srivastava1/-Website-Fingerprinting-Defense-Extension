# Adaptive Padding to Defend Against Website Fingerprinting

An implementation of an adaptive padding algorithm by Ishan Srivastava and Vikranth Nara, two students from the University of Virginia's School of Engineering, to combat website fingerprinting attacks, ensuring robust privacy without compromising usability.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Key Highlights](#key-highlights)
3. [Key Technologies Used](#key-technologies-used)
4. [Features](#features)
5. [Methodology](#methodology)
6. [Results](#results)
7. [Demo](#demo)
8. [Future Directions](#future-directions)
9. [Setup](#setup)
10. [Works Cited](#works-cited)

---

## Introduction

Website fingerprinting is a privacy-invasive technique where attackers deduce a user's web activity by analyzing network traffic patterns. This project implements a **browser extension** to counter these attacks using an adaptive padding algorithm. The defense dynamically adjusts traffic patterns to obscure user activities, rendering attackers' fingerprinting efforts ineffective.

### Why This Matters:
- **Resistant to VPN and Tor Fingerprinting**: Unlike cookies, fingerprinting cannot be erased or easily avoided.
- **Enhanced Privacy**: Mitigates risks of identity theft, fraud, and manipulative advertising.
- **Efficient Defense**: Balances privacy and usability by minimizing performance degradation.

---

## Key Highlights
- Simulates **realistic traffic patterns** using burst and gap modes.
- Randomizes dummy packet **size and content** to prevent predictable patterns.
- Provides a **user-friendly interface** for toggling protection and adjusting privacy settings.
- Displays **real-time metrics** like dummy packets sent and intercepted real packets.

---

## Key Technologies Used
- **JavaScript**: For implementing the adaptive padding algorithm and Chrome Extensions API functionality.
- **Python**: For initial simulations and performance analysis of the histogram-based delay sampling.
- **Chrome Extensions API**: To create the browser extension and manage event listeners for web traffic.
- **HTML & CSS**: For building the intuitive user interface.
- **DOM Manipulation**: For real-time metric updates in the UI, such as dummy packets and burst/gap states.

---

## Features

### Dynamic Mode Switching
Shifts between **burst** (high traffic) and **gap** (low traffic) states based on real-time activity.

### Histogram-Based Padding
Uses **probabilistic sampling** to mimic realistic inter-packet delays and avoid detection.

### Adjustable Privacy Levels
Allows users to control the **intensity of padding**, offering a tradeoff between usability and privacy.

### Real-Time Metrics
Includes a dashboard that displays:
- Total dummy packets sent
- Packets sent during burst and gap states
- Real packets intercepted

---

## Methodology

The adaptive defense uses two key modes:
1. **Burst Mode**: Activated during high traffic periods. Inter-packet delays are modeled using a burst histogram.
2. **Gap Mode**: Activated during low activity. Dummy packets are sent at intervals based on a gap histogram.

### Key Innovations:
- **Histogram Sampling**: Probabilistically selects delays to mimic real traffic patterns.
- **Randomized Packet Content**: Ensures packets vary in size and content, avoiding detection.
- **User Interface**: Simple yet functional interface for toggling the extension and viewing real-time metrics.

---

## Results

The extension was tested on websites like **CNN** and demonstrated:
- Smooth transitions between burst and gap modes.
- Randomized dummy packets that significantly reduced identifiable patterns.
- Real-time metrics validating the interception and obfuscation of traffic.

---

## Demo

Watch the extension in action:

[Video Demo on Google Drive](https://drive.google.com/file/d/1RCfhdpTTXbMISwSKdzAejSZ_0PCY7Fra/view?usp=sharing)

### Screenshots:
1. **Web Extension UI**
   ![Gap Mode](![webextensionui](https://github.com/user-attachments/assets/e6b1b800-d4dc-4cb1-8da4-e3782c029acf))
   *The above picture depicts the interface of the web extension, showing the total number of dummy packets sent between burst/gap mode, the number of packets intercepted, and an option to change the padding intensity.*
2. **Console Log**
   ![Gap Mode](![ConsoleLog](https://github.com/user-attachments/assets/0347e457-e9a9-438b-afa9-e7dcdc63367d))
   *The above screen shot depicts the console log of the extension, showing when the program switches states between bust and gap mode. The screen shot also shows the data of the randomized dummy packets sent and the delays set by the histogram for the dummy packets to be sent.*

---

## Future Directions

### Potential Enhancements:
1. **Machine Learning Integration**: Train a model to adapt padding dynamically based on real-time traffic patterns.
2. **Protocol Expansion**: Add support for WebSocket, HTTP/2, QUIC, and other advanced protocols.
3. **Universal Defense**: Combine adaptive learning with protocol support for a comprehensive solution.

---

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Ishan-Srivastava1/Website-Fingerprinting-Defense-Extension.git
2. Load the extension:

Open your browser's extensions page.
Enable developer mode.
Load the unpacked extension from the project directory.
Adjust settings in the user interface as needed.

## Works Cited
Juarez, M., Imani, M., Perry, M., Diaz, C., Wright, M. (2016). Toward an Efficient Website Fingerprinting Defense.
In: Askoxylakis, I., Ioannidis, S., Katsikas, S., Meadows, C. (eds) Computer Security – ESORICS 2016.
ESORICS 2016. Lecture Notes in Computer Science(), vol 9878. Springer, Cham.
DOI: 10.1007/978-3-319-45744-4_2


