# SenOS

Giao diện / hệ điều hành chạy từ thẻ nhớ cho máy chơi game **TrimUI Brick Pro (TG4040)**, dựa trên firmware gốc.

## Cài đặt / cập nhật

- **Trên máy (từ 0.5.9):** Cài đặt › Thông tin › **Kiểm tra cập nhật** — máy tự tải và cài bản mới nhất từ repo này.
- **Bằng tay:** tải [`releases/senos-update.zip`](releases/senos-update.zip), chép vào gốc thẻ nhớ rồi khởi động lại máy.

## Cách phát hành bản mới

Máy đọc file [`update.json`](update.json) ở nhánh `main`:

```json
{ "version": "0.5.9", "notes": "…", "url": "…/releases/senos-update.zip", "size": 0, "sha256": "…" }
```

Thay `releases/senos-update.zip`, cập nhật `version`, `size`, `sha256` (và `notes`) trong `update.json`, rồi commit lên `main`.
Máy chỉ cập nhật khi `version` cao hơn bản đang chạy và luôn kiểm tra mã SHA-256 trước khi cài.
