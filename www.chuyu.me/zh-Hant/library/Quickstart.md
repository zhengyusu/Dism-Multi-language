# 快速入門
程式的核心功能是清理更新，所以你可能需要在安裝更新後才能感受到程式的價值。

## 介面布局
如圖所示，頂端的標籤可以切換不同的系統`（如果你有多個作業系統）`。左側為功能列表，可以選擇你所需要的功能。對於一般使用者來說，直接點擊`空間回收`就可以啦。

![MainUI](./images/MainUI.png)

## 清理系統垃圾
<br>
>建議你不要過於頻繁的清理垃圾，尤其是 SSD！一般建議一個月清理一次即可。

![CleanupUI](./images/CleanupUI.png)

<br>
程式啟動後，點擊`空間回收`，即可看到此介面。然後選中你需要清理的項目，在點擊`掃描`（預計可以釋放的空間）或者直接點擊`清理`（不預估大小，立即刪除）。最後如果你有更好的清理項目，點擊 `說明 - 意見反映`，提出你的規則。

<br>
>貼心提醒：風險項目使用橙色標示，另外某些項目存在某些副作用，選取後程式將跳出警告框，請務必仔細確認！

## 備份系統
俗話說有「備」無患，現在 Dism++ 能夠直接將目前系統備份為 WIM、ESD，無需進入 PE。使用方法很簡單，選取目前系統，點擊恢復功能 —— 系統備份即可。

![BackupImage](./images/BackupImage.png)

![BackupImage-WimPath](./images/BackupImage-WimPath.png)
<br>然後輸入 WIM 檔案路徑，最後點擊確定即可。
>如果 WIM 檔案已經存在，則自動增量到現有的 WIM 檔案，執行增量備份。

此外，為了支援系統無法啟動時能夠還原系統，還需要在 選項 - 詳細設定 開啟 整合 BCD boot 選單，開啟後 BCD 啟動項目中將多出一個 Dism++，你可以在必要時使用此選項來恢復你的系統。

## 還原系統
當系統出問題時，你可以使用之前備份的系統進行還原，快速恢復電腦環境。Dism++ 為了降低恢復系統的難度，程式支援熱還原模式。即使用者無需啟動 PE 直接在本機就能還原。如果你的電腦出問題了，你可以啟動 Dism++，點擊恢復功能 -
系統還原。選擇 WIM 檔案路徑後，點擊確定即可，如下圖所示。

![RecoveryImage](./images/RecoveryImage.png)

>貼心提醒：如果你的系統已經無法啟動，那麼可以透過 BCD 選單中的 Dism++`（需要開啟 整合 BCD boot 選單）`或者啟動 PE 進行上述步驟。

<br>快速入門已經結束，想深入研究的使用者可以參考後續文件，祝大家玩的開心。
