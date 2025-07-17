# 硬體設計 Hardware

## 電路圖 Schematic
<img src="images/MHI_SCH.png" width=600/>

### 設計說明

1. GPIO10要與任一GPIO對接，此設計是接GPIO7

2. level shifter僅用3個，1個用不到

3. 連接至冷氣的此設計用90度彎針，也能直接用180度母頭，但焊接時需注意接頭方向，焊反插上去會燒，方向可參考下面冷氣底座


### Design Notes

1. GPIO10 must be connected to any other GPIO pin. In this design, it is connected to GPIO7.

2. Only three level shifters are used; one is left unused.

3. The connection to the air conditioner in this design uses a 90-degree pin header. A straight (180-degree) female header can also be used, but you must pay close attention to the orientation during soldering. Soldering it in the wrong direction will cause it to burn out when plugged in. You can refer to the air conditioner's base below for the correct orientation.

## 電路板 PCB

Size: 46.5mm x 26mm

<img src="images/PCB_TOP.png" width=600/>

<img src="images/PCB_BOTTOM.png" width=600/>

## 成品圖 Finished Product

1. 焊接完成的板子: **要剃除模組上的天線，收訊才會好!!**

Soldered Board: The SMD antenna on the module **MUST be removed** to ensure good reception!

<img src="images/RAW_Board.jpg" width=600/>

2. 放入3D列印殼中:

Placed in 3D-Printed Case:

<img src="images/BoardinCase.jpg" width=600/>

3. 完成品，蓋上蓋與接上排線:

Final Assembly: Case closed and cable connected.

<img src="images/3DCase&Cable.jpg" width=600/>


## 材料清單 Bill of Material

1. ESP32C3 super mini
2. 37*10mm FPC antenna 3cm long
3. DCDC 12V to 5V
4. 5V to 3.3V 4channel level shifter
5. XH2.54mm-5p 90degree male
6. XH2.54mm-5p female to female cable 50cm long

## 冷氣底座腳位定義 AC connector pin definition

<img src="images/SRK-PCB.jpg" width=600/>
