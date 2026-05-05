# Software Studio 2026 Spring Midterm Project - Chatroom
### 學號：113062110

## 專頁連結 (Web Page Link)
(https://midterm-113062110.web.app)

## Scoring Checksheet

### Basic Components (50%)
| **Basic Components**      | **Score** | **Check** |
| :-------------------      | :-------: | :-------: |
| Membership Mechanism (Sign Up/In)       | 5%  | Y |
| Firebase Hosting                        | 5%  | Y |
| Database read/write (Authenticated)     | 5%  | Y |
| RWD (Responsive Web Design)             | 5%  | Y |
| Git (Version Control & Regular Commits) | 5%  | Y |
| Chatroom Logic (Private/History/Invite) | 25% | Y |

### Advanced Components (35%)
| **Advanced Components** | **Score** | **Check** |
| :----------------------- | :-------: | :-------: |
| Framework (React or others) | 5% | Y |
| 3rd-party Sign In (Google) | 1% | Y |
| Chrome Notification | 5% | Y |
| CSS Animation | 2% | Y |
| XSS Prevention (Dealing with code) | 2% | Y |
| User Profile (Pic/Name/Email/Phone/Address) | 10% | Y |
| Message Operations (Edit/Search/Unsend/Image) | 10% | Y |

### Bonus Components (Max 10%)
| **Bonus Components** | **Score** | **Check** |
| :------------------- | :-------: | :-------: |
| Chatbot (ChatGPT/Gemini API) | 2% | N |
| Block User | 2% | Y |
| Send GIF from Tenor API | 3% | N |
| Message Emoji | 3% | Y |
| Reply for specify message | 6% | Y |
| Custom sticker into chatroom (Drawing) | 10% | N |

---

## 如何操作 (How to use)

### 1. 登入與註冊
*   **Email 註冊**：在登入頁面點選「註冊」，輸入 Email 與密碼。
*   **Google 登入**：點選「使用 Google 帳號登入」按鈕進行快速登入。
*   **初始化資料**：首次登入需設定個人暱稱與唯一自定義 ID。

### 2. 個人資料管理
*   點選側邊欄左下角的個人卡片，即可開啟「編輯個人資料」彈窗。
*   可在此上傳頭像圖片、修改暱稱、更新電話與地址。

### 3. 聊天功能
*   **添加好友**：點選側邊欄「👤+」符號，輸入對方的 ID 即可開啟私聊。
*   **建立群組**：點選「💬+」符號，輸入群組名稱與成員 ID（逗號隔開）。
*   **訊息操作**：
    *   **搜尋**：在頂部搜尋框輸入文字，可即時過濾並跳轉到對應訊息。
    *   **編輯/收回/刪除**：鼠標懸停於訊息上，點選對應按鈕進行操作。
    *   **回覆與表情**：可針對特定訊息進行回覆或添加 Emoji 反應。

### 4. 封鎖與安全
*   點選對方的頭像可查看其詳細資料。
*   在此彈窗中點選「封鎖」，對方的訊息將即時消失，且對方無法再傳送私訊。

---

## 本地開發設定 (How to setup locally STEP BY STEP)

1.  **複製專案**：
    ```bash
    git clone <your-repo-url>
    cd <project-folder>
    ```
2.  **安裝 Firebase Tools** (若尚未安裝)：
    ```bash
    npm install -g firebase-tools
    ```
3.  **Firebase 登入**：
    ```bash
    firebase login
    ```
4.  **初始化與關聯專案**：
    ```bash
    firebase use midterm-113062110
    ```
5.  **啟動本地伺服器**：
    ```bash
    firebase serve
    ```
6.  **瀏覽網頁**：打開瀏覽器訪問 `http://localhost:5000`。

---

## 創意加分功能 (Bonus Function Description)
*   **回覆訊息系統 (6%)**：實作了類似 LINE/Messenger 的回覆機制，點擊被回覆的區塊會自動平滑跳轉至原訊息並閃爍提醒。
*   **即時封鎖機制 (2%)**：使用了 Firebase `onSnapshot` 同步監聽，封鎖動作在兩端皆為即時生效，無需重新整理頁面。
*   **精準 Chrome 通知 (5%)**：只有在視窗縮小或切換分頁時，且接收到非當前對話框的新訊息時才會跳出通知，避免干擾。

---

## 給助教的話 (Others)
*   測試 Chrome 通知時，請確保已在網址左側「鎖頭」處開啟通知權限，並將網頁切換至背景分頁再發送測試訊息。
*   RWD 專門針對手機版進行了優化，點擊房間後會切換至全螢幕對話視窗。

<style>
table th{
    width: 100%;
}
</style>