# math

個人簡介範例站點（由自動化工具建立）。

此專案示範一個簡單的靜態個人介紹頁面，包含：

- `index.html`：主頁（已將內嵌樣式抽出）。
- `styles.css`：外部 CSS（調整排版、響應式大頭貼）。
- `assets/profile.svg`：簡單的響應式 SVG 大頭貼範例。
- `.github/workflows/deploy.yml`：GitHub Actions 範例工作流程，示範如何在 push 到 `main` 時部署到 GitHub Pages（使用官方 `upload-pages-artifact` / `deploy-pages`）。

如何本機預覽：

```bash
# 在專案根目錄啟動簡單 HTTP server
python3 -m http.server 8000
# 然後在瀏覽器打開：
http://localhost:8000/index.html
```

若要部署到 GitHub Pages：

1. 將此 repo 推送到 GitHub（分支為 `main`）。
2. 確認 repo 設定中 Pages 的方式允許使用 GitHub Actions（或依照你的需求修改 workflow 的 `path:` 指向 `docs/` 等）。
3. push 到 `main`，GitHub Actions 工作流程會上傳整個 repo 根目錄並嘗試部署。

註：第一次啟用 Pages 時，可能需要在 GitHub 網頁端到 Settings → Pages 進行一次確認。

後續建議：
- 把 `index.html` 中的示範文字（姓名、Email、外部連結）替換為你的實際資訊。
- 若要更佳的圖片支援，可加入 JPG / WebP 多解析度檔案並用 `<picture>` 或 `srcset` 提供不同解析度。
- 若使用自訂網域，請在 repo 根目錄加入 `CNAME` 檔案並更新 Pages 設定。