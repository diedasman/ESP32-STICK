# 📦 ESP32-S3-LCD-1.47 Enclosure (ESP-STICK)

A compact 3D-printable enclosure designed specifically for the **Waveshare ESP32-S3-LCD-1.47** development board.

This enclosure provides:
- Secure mounting for the PCB
- Easy access to USB, buttons, and screen
- A clean, minimal form factor suitable for desk or handheld use

🔗 Product reference:  
https://www.waveshare.com/wiki/ESP32-S3-LCD-1.47

---

## 📸 Preview

![Assembled enclosure](images/assembled.jpg)  
![Exploded view](images/exploded.jpg)

> See the assembly section below for step-by-step photos.

---

## 🧩 Features

- Designed specifically for **ESP32-S3-LCD-1.47**
- Snap-fit or screw-based assembly (depending on version)
- No supports required for most printers
- Optimized for FDM printing
- Compact and lightweight

---

## 🖨️ Printing Recommendations

| Setting           | Recommendation |
|-------------------|----------------|
| Material          | PLA / PETG    |
| Layer height      | 0.2 mm        |
| Infill            | 15–25%        |
| Perimeters        | 3              |
| Supports          | None           |
| Print orientation | As provided    |

> PETG is recommended if the enclosure will be exposed to higher temperatures.

---

## 🔩 Assembly Instructions

### Step 1 – Print the Parts
Print all STL files located in the `/stl` folder.

![Step 1](images/step1_parts.jpg)

---

### Step 2 – Insert the ESP32 Board
Place the ESP32-S3-LCD-1.47 into the front shell:
- Ensure the display sits flush with the front opening
- Align the USB connector with the cutout

![Step 2](images/step2_board.jpg)

---

### Step 3 – Secure the Board
Secure the PCB using:
- M2 screws *(length: XX mm)*  
  **or**
- Integrated snap-fit features (if applicable)

![Step 3](images/step3_screws.jpg)

---

### Step 4 – Close the Enclosure
Attach the back cover and fasten it using screws or snap it into place.

![Step 4](images/step4_close.jpg)

---

## 📁 Repository Structure
```
├── stl/
│ ├── EnclosureBottom.stl
│ └── EnclosureTop.stl
├── images/
│ ├── assembled.jpg
│ ├── exploded.jpg
│ ├── step1_parts.jpg
│ └── step2_board.jpg
├── step/
| ├── esp32-s3-lcd-1_47_asm.step
| ├── ESP-STICK-ASSEMBLY.step
| ├── EnclosureBottom.step
│ └── EnclosureTop.step
└── README.md
```
---

## 🛠️ CAD Files

- Native CAD files are located in `/cad`
- Exported STL files are located in `/stl`

Designed using **Onshape / Fusion 360 / FreeCAD**  
*(update this section to match your toolchain)*

---

## ⚠️ Notes & Limitations

- Designed **only** for the Waveshare ESP32-S3-LCD-1.47
- Not compatible with other ESP32-S3 LCD boards
- Tolerances are optimized for common FDM printers  
  Minor sanding or fit adjustment may be required

---

## 📜 License

This project is released under the **MIT License**.

You are free to:
- Use
- Modify
- Print
- Sell printed versions

Attribution is appreciated but not required.

---

## 🤝 Contributions

Contributions, improvements, and remixes are welcome.  
If you create a variant (battery version, wall mount, etc.), feel free to open a pull request or share it.

---

Enjoy building! 🚀
