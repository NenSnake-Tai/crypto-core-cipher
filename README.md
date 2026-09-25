# Crypto Core Cipher Engine 🔐

A low-latency symmetric cryptographic processing engine built in native JavaScript. This repository demonstrates modular bitwise operations, character matrix transpositions, and real-time buffer encryption routines to secure localized data payloads with zero input lag.

## 🗂️ Architectural Overview

The cryptographic engine operates as a deterministic security pipeline, capturing raw text payloads, mapping string structures, and injecting transformational keys through a custom algorithmic substitution array.

### ⚙️ Core Technical Features:
* **Real-Time Data Ciphering:** Processes encryption and decryption loops instantly via localized memory stack routines.
* **Payload Integrity Protection:** Sanitize incoming data tokens to ensure zero memory corruption or buffer leaks.
* **Zero External Dependencies:** Built strictly with vanilla JavaScript, CSS, and HTML for direct hardware thread alignment.

## 🚀 Deployment Instructions

To run the cipher engine locally or host it on any web environment:
1. Clone this repository to your local storage.
2. Ensure `index.html`, `style.css`, and `script.js` are in the same directory.
3. Open `index.html` in any standard modern web browser (Chrome, Brave, Edge).

*Developed for cryptographic behavior analysis and core data protection logic prototyping.*

```mermaid
graph TD
    %% Estilo de nodos neón
    classDef safe color:#00ff66,fill:#000,stroke:#00ff66,stroke-width:2px;
    classDef alert color:#ff0033,fill:#000,stroke:#ff0033,stroke-width:2px;
    classDef process color:#00ffff,fill:#000,stroke:#00ffff,stroke-width:1px;

    Start([⚡ Crypto Engine Init]) --> Load[🚀 DOM Ciphers Rendered]
    Load --> Active[📡 Attached Input Listeners Crypto/Decrypto]
    
    Active --> Wait{⌨️ Waiting for Text Buffer Input}
    
    Wait -- NO --> Wait
    Wait -- SÍ --> Capture[📥 Capture Raw Text Stream & Security Key]
    
    Capture --> Check{🔬 Validate Payload Constraints}
    
    Check -- Empty/Invalid --> Err[🚨 Trigger Cipher Integrity Exception]:::alert
    Check -- Valid Input --> Route{🔀 Cipher Mode Router Switch-Case}
    
    Route -- Mode: Encrypt --> Enc[⚙️ Run Matrix Transposition Array]:::process
    Route -- Mode: Decrypt --> Dec[⚙️ Run Reverse Algorithmic Inversion]:::process
    
    Err --> Output[🖥️ Flush Status Log to Virtual Terminal]
    Enc --> Output
    Dec --> Output
    
    Output --> Return[🔄 Clear Volatile Buffers & Re-arm Listeners]
    Return --> Wait

    class Start,Load,Active,Wait safe;
    class Capture,Check,Route,Enc,Dec,Output,Return process;
```
