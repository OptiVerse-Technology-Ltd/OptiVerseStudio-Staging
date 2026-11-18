# OptiVerse Studio – test builds

This repository holds test builds of OptiVerse Studio for invited testers.
繁體中文說明在下方。

- A test build has no support. Use it only with recordings that you can lose.
- A test build is named **OptiVerse Studio Staging**. It keeps its own
  library, models and settings. A later release of OptiVerse Studio does not
  open the data of a test build.
- The builds are not signed by Apple or by Microsoft. macOS and Windows warn
  you before the first start. The install guide gives the steps.
- macOS: Apple silicon (M1 or later) only. Windows: 64-bit, the package uses
  the CPU only. On Windows, the app writes a summary after the recording
  ends. It shows no live summary during a recording.
- For summaries, you can select a built-in model, which runs on your
  computer, or a provider such as Anthropic, OpenAI, Groq or Ollama. With a
  hosted provider or a cloud model of Ollama, your transcripts go to that
  service. A hosted provider needs your own API key, and its use can cost
  money.
- The source code is not in this repository.

## Install

See the latest release: download the `.dmg` for macOS or the `.exe` for
Windows. Do not download the other files: the `.app.tar.gz` and `.json`
files are for updates, and the source code archives that GitHub adds do not
contain the app.

The install guide and the known limitations are in the Traditional Chinese
part below.

## Report a problem

Use the report link in your invitation. You do not need an account. Only
the OptiVerse team reads the reports. If you lost the link, ask the person
who invited you.

Do not paste a recording, a transcript, a summary or meeting content into the
form. To send a screenshot or a file, leave a way to reach you in the last
question of the form, and we will contact you.

---

# OptiVerse Studio 測試版

這個 repository 提供 OptiVerse Studio 的測試版給受邀的測試者。

- 測試版沒有正式支援。請只用可以遺失的錄音測試。
- 測試版的名稱是 **OptiVerse Studio Staging**，有自己的錄音庫、模型與設定。日後的正式版不會開啟測試版的資料。
- 測試版沒有 Apple 或 Microsoft 的簽章。第一次開啟前，macOS 與 Windows 會顯示警告，步驟請參考下方的安裝說明。
- macOS: 只支援 Apple 晶片 (M1 或更新)。Windows: 64 位元，這個套件只使用 CPU。Windows 上的摘要會在錄音結束後產生，錄音時沒有即時摘要。
- 摘要可以選內建模型 (在您的電腦上執行)，也可以選 Anthropic、OpenAI、Groq 或 Ollama 等服務。選雲端服務或 Ollama 的雲端模型時，逐字稿會傳送到該服務。雲端服務需要您自己的 API 金鑰，使用時可能產生費用。
- 原始碼不在這個 repository。

## 安裝

請到最新的 release 下載: macOS 用 `.dmg`，Windows 用 `.exe`。其他檔案都不用下載: `.app.tar.gz` 和 `.json` 是 App 自動更新用的，Source code 是 GitHub 自動附上的，不是 App。

### macOS (Apple 晶片)

1. 打開下載的 `.dmg`，把 **OptiVerse Studio Staging** 拖到 [應用程式] 資料夾。
2. 這個 App 沒有經過 Apple 公證，所以第一次開啟時 macOS 會擋下它，並顯示兩個按鈕。請按下方灰色的 [完成] (Done)。不要按上方藍色的按鈕 (Move to Trash)，它會把 App 移到垃圾桶，您就要從 `.dmg` 再拖曳一次。接著請到 [系統設定] > [隱私權與安全性] 允許開啟這個 App。
3. 第一次設定時，App 會要求麥克風與錄製系統音訊的權限，並下載語音模型。摘要可以選內建模型或雲端服務。
4. 之後的更新: [設定] > [關於] > [檢查更新]。

### Windows (64 位元)

下列畫面是在繁體中文的 Windows 11 與 Edge 上，安裝前一個測試版時看到的。

1. 下載 `.exe`。Edge 可能先暫停下載，並說明這個檔案不常下載。請按 [保留]。
2. 執行下載的檔案。這個檔案沒有 Microsoft 的程式碼簽章，所以 Windows 可能先顯示警告。
3. 安裝精靈:
   1. 選擇語言 (English 或 中文(繁體))，按 [OK]。
   2. 按 [下一步(N)]。安裝位置預設為 `C:\Users\<使用者>\AppData\Local\OptiVerse Studio Staging`，約需 242 MB，不需要系統管理員權限。
   3. 按 [完成(F)]。[執行 OptiVerse Studio Staging] 與 [建立桌面捷徑] 預設都已勾選。
4. 第一次設定:
   1. 選擇顯示語言與外觀。
   2. 檢查麥克風。如果 Windows 不允許使用麥克風，App 會說明到 [設定] > [隱私權與安全性] > [麥克風] 開啟。錄製電腦播放的聲音不需要權限。
   3. App 會說明這個套件不使用 GPU。
5. 之後的更新: [設定] > [關於] > [檢查更新]。

這個版本的模型步驟與前一個測試版不同: 這個 Windows 套件不會預先選內建摘要模型，而是建議雲端服務或 Ollama。您也可以選內建的 Unsloth 0.8B、4B 或 9B。

如果警告畫面讓您無法繼續安裝或開啟 App，請使用邀請訊息中的連結回報。

### 移除

- macOS: 刪除 [應用程式] 中的 **OptiVerse Studio Staging**。錄音庫與設定在 `~/Library/Application Support/com.optiverse-studio.staging`，刪除 App 不會刪除這個資料夾。
- Windows: 在 [設定] > [應用程式] 中解除安裝 **OptiVerse Studio Staging**。解除安裝程式有一個勾選方塊「同時刪除設定、錄音庫和已下載的模型」，預設沒有勾選。不勾選時，下列資料會留在電腦上:
  - `%APPDATA%\com.optiverse-studio.staging`: 錄音庫、模型、設定。
  - `%LOCALAPPDATA%\com.optiverse-studio.staging`: 錄音的音訊、記錄檔、WebView2 資料。
  - 登錄機碼 `HKCU\Software\OptiVerse Technology Ltd\OptiVerse Studio Staging`。

## 已知限制 (0.4.0-rc.2)

- 沒有 Apple 公證，也沒有 Microsoft 的程式碼簽章。
- macOS 只支援 Apple 晶片。
- Windows 套件只使用 CPU，所以 Windows 上錄音時沒有即時摘要與即時心智圖。摘要在錄音結束後產生，而且要先選一個摘要模型或服務。
- 內建摘要模型是 Unsloth 0.8B、4B 與 9B。新摘要引擎的速度與記憶體用量還沒重新量測。
- 錄音庫有 1,000 筆錄音時，Windows 上開啟需要約 54 秒。
- 摘要中的連結: 在 Windows 上點擊沒有反應，編輯器的連結欄位也無法建立連結。
- 摘要匯出成 PDF 時，中文會變成錯誤的字元，標題維持英文。
- 還原一筆中斷的錄音後，音訊可以播放，但狀態仍顯示遺失。
- 刪除一筆錄音的音訊後，App 會說儲存位置無法使用。
- 測試版的資料不會帶到正式版。
- Windows 上暫停再繼續的錄音，停止後顯示「這段錄音含有音訊缺口」的問題已在這個版本修正。如果仍看到這個訊息，請回報。

## 回報問題

請使用邀請訊息中的回報連結。不需要任何帳號。只有 OptiVerse 團隊會看到回報內容。找不到連結時，請詢問邀請您的人。

請不要在表單貼上錄音、逐字稿、摘要或會議內容。要傳送螢幕截圖或檔案，請在表單最後一題留下聯絡方式，我們會與您聯絡。
