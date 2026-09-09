# 咱兜的留言簿

這是可直接發佈到網際網路的純靜態網站，不需要資料庫或建置指令。網站支援手機安裝與離線開啟；留言仍只儲存在該裝置的瀏覽器中，不會傳送至伺服器。

## 最簡單的發佈方式：Netlify Drop

1. 前往 <https://app.netlify.com/drop>。
2. 將整個 `family-message-board` 資料夾拖進頁面。
3. 等待完成後，Netlify 會提供一個可分享的 HTTPS 網址。
4. 用手機開啟該網址，允許麥克風權限即可使用語音輸入。

## 其他支援平台

- **GitHub Pages**：把這個資料夾放進 GitHub repository，於 Settings → Pages 選擇從分支發佈。
- **Vercel**：匯入 repository，或使用 Vercel CLI 在此資料夾執行 `vercel`。
- **Cloudflare Pages**：匯入 repository，建置指令留白，輸出目錄填入 `.`。

所有平台都必須使用 HTTPS，瀏覽器才會允許網站使用麥克風。iPhone/iPad 上若瀏覽器不提供網站語音辨識，可以點選輸入框，再使用 iOS 鍵盤上的麥克風。

## 本機預覽

在資料夾內執行：

```powershell
python -m http.server 8000
```

再開啟 <http://localhost:8000>。
