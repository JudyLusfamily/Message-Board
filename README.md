# 咱兜的留言簿

全家共享的語音留言板，使用 Supabase 同步資料。

## GitHub Pages 發佈

1. 在 GitHub 建立一個 repository。
2. 將此資料夾內所有檔案推送到 `main` 分支。
3. 到 repository 的 **Settings → Pages**。
4. 在 **Build and deployment → Source** 選擇 **GitHub Actions**。
5. 到 **Actions** 查看 `Deploy family message board`，完成後即可取得網址。

工作流程只發佈網站所需檔案，不會將 `supabase-setup.sql` 或 README 放進網站成品。

## 資料庫

資料庫已透過 `supabase-setup.sql` 建立。前端使用 Supabase publishable key；資料表不允許瀏覽器直接存取，讀寫都必須通過家庭密碼驗證函式。

## 更新網站

修改檔案後提交並推送到 `main`，GitHub Actions 會自動重新發佈。手機若仍顯示舊版，可完全關閉網站後再重新開啟。
