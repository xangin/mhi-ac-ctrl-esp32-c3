# mhi-ac-ctrl-esp32-c3
Control MHI Airconditioning locally by using ESP32C3 with ESPhome

This is a customized version of [hberntsen/mhi-ac-ctrl-esp32-c3](https://github.com/hberntsen/mhi-ac-ctrl-esp32-c3).

## 三菱重工冷氣ESPhome

這是個使用ESP32C3搭配ESPhome來控制三菱重工冷氣的專案，可適用壁掛及吊隱式冷氣

感謝[hberntsen/mhi-ac-ctrl-esp32-c3](https://github.com/hberntsen/mhi-ac-ctrl-esp32-c3)開發ESPhome韌體，搭配我設計的硬體，即可本地端控制三菱重工冷氣

適用型號: 支援外接原廠Wi-Fi智慧模組的機型，機器上有白色5pin的XH2.54mm底座就能使用

<img src="images/SRK-PCB.jpg" width=450/>

## 燒錄檔與ESPhome程式碼 Bin & YAML

YAML修改基本上只要修改最頂端的名稱即可，方便OTA與辨識是哪一台，也可將用不到的實體註解掉

| 檔名 | 適用機型 | 燒錄方式 | Bin檔 | YAML |
|-------|:-----:|:-----:|:-----:|-------|
| 三菱重工-壁掛式.factory.bin | 壁掛式 | 接USB直接燒錄 | [Bin檔](三菱重工-壁掛式.factory.bin) | [YAML](mhi-ac-wall.yaml) |
| 三菱重工-吊隱式.factory.bin | 吊隱式 | 接USB直接燒錄 | [Bin檔](三菱重工-吊隱式.factory.bin) | [YAML](mhi-ac-ceiling.yaml) |

## 如何下載

點擊檔案名稱>點右上角有個下載的圖案(Download Raw file)>儲存

## 使用方法

### A. 透過USB

1. 模組透過usb接上電腦
2. 用chrome或edge瀏覽器前往 [https://web.esphome.io](https://web.esphome.io/)
3. 按Connect>選擇寫USB JTAG(小)>按INSTALL>選擇剛儲存的Bin檔，等待燒錄完成
4. 顯示finish後，就可看到ESP32上面的藍燈開始閃爍，這時候等待久一點，會看到有熱點跑出來
5. 點連線並輸入Wi-Fi密碼: 12345678
6. 連上後輸入http://192.168.4.1
7. 進到網頁選擇家中Wi-Fi名稱及輸入密碼後按儲存，連上後HA應該就會自動發現此裝置

### B. OTA

1. 在瀏覽器網址列輸入裝置IP
2. 最下方OTA Update選擇ota.bin檔>按Update，等待畫面跳轉為done即完成

## 硬體架構

詳細請參考[Hardware.md](Hardware.md)



## 📦Credits

This project is based on the excellent work of [hberntsen/mhi-ac-ctrl-esp32-c3](https://github.com/hberntsen/mhi-ac-ctrl-esp32-c3), which itself integrates multiple community contributions.
Licensed under MIT.
