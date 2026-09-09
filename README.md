# 咱兜的留言簿

這是全家共享的語音留言板，前端使用 Supabase publishable key，資料表不允許瀏覽器直接存取；所有讀寫均經過家庭密碼驗證函式。

## 第一次設定資料庫（必要）

1. 登入 Supabase，開啟目前專案。
2. 左側選擇 **SQL Editor**，再按 **New query**。
3. 在本機開啟 `supabase-setup.sql`，複製全部內容貼進 SQL Editor。
4. 將最後一行的 `請換成至少8碼家庭密碼` 換成自訂密碼。建議至少 10 碼並混合數字與文字。
5. 按 **Run**；畫面顯示成功後資料庫即完成。

家庭密碼只會以雜湊形式儲存在資料庫。請把密碼告訴家人，但不要把修改後、含有密碼的 SQL 檔一起公開上傳。

## 發佈網站

最簡單的方法是前往 <https://app.netlify.com/drop>，將整個 `family-message-board` 資料夾拖進頁面。發佈完成後會取得 HTTPS 網址。若修改過本機的 `supabase-setup.sql` 加入真實密碼，請先把該檔案移出資料夾再上傳。

也可使用 GitHub Pages、Vercel 或 Cloudflare Pages。網站不需建置指令。

## 使用方式

每位家人用相同家庭密碼進入，姓名可各自填「爸爸」、「媽媽」等。網站每 10 秒自動同步，也會在新增或刪除後立即更新。
