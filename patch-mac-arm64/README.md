# 摸魚 補丁更新倉庫（mac-arm64）

客戶端（`backend/app/update_downloader.py`）讀 `manifest.json`，與本機的比對後只抓變動的檔案：`files/<sha256>`。

- `files/` 是內容定址的，**只增不刪**——舊版客戶端可能還需要舊檔案。
- 這裡的檔案由 `scripts/publish_patch.py` 產生，不要手改。
- 目前 manifest 版本：`1.0.30`
