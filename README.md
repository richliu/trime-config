
# 客制化自己的 rime config 

rime 是個開源的中文輸入法框架，不過設定上有點麻煩
這邊是我在 Linux　和 Android 安裝的心得，主要輸入法是大易
其他可以自己改

原始設定檔來自 gkovacs/trime-config

dayi4 詞庫來自 https://github.com/chiahsien/RimeDayi.git

## Common

### 新增輸入法

在 default.custom.yaml 在以下 copy paste 一上加上你要的輸入法
以 bopomofo_tw 為例, ubuntu 會自己安裝不用準備, 但是 android 
要自己 copy 進去
      schema_list:
        - schema: dayi4
        - schema: bopomofo_tw

* [bopomofo 下載網址](https://github.com/rime/rime-bopomofo)


## Android 
最簡單的版本, 將所有的檔案 copy 到 storage/emulated/0/rime 
一般是根目錄下的 rime 
有時候不會出現，重開機一下再看看，有時候不能直接copy進去
先 copy 到其他目錄 ex: Download ，再用手機內建的軟體 copy 過去

## Linux 

Linux 下預設會刪除 ~/.config/ibus/rime/default.yaml, 
修改請用 default.custom.yaml 替代之

### ubuntu install ibus-rime 
    sudo apt install ibus-rime

### confiture ibus
    im-config
選完 ibus 之後
    ibus-setup

### restart ibus 

restart ibus command 
    ibus-daemon -drx

### 設定檔位置

    touch ~/.config/ibus/rime/; ibus restart


## 參考網站 
* [rime 下載及安裝] (https://rime.im/download/)
* [定製指南] (https://github.com/rime/home/wiki/CustomizationGuide)
* [trime.yaml 詳解] (https://github.com/osfans/trime/wiki/trime.yaml-%E8%A9%B3%E8%A7%A3)
