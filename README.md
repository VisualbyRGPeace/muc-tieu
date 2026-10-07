# 🎯 Mục tiêu – Tuần · Tháng · Năm

Web app (PWA) quản lý mục tiêu và tiến độ, đồng bộ realtime iPhone ↔ PC bằng Firebase. Tông thuần trắng – đen.

## Cấu trúc
| File | Vai trò |
|---|---|
| `index.html` | Toàn bộ giao diện và logic |
| `manifest.json` | Cài app lên màn hình chính |
| `sw.js` | Service worker: mở nhanh, chạy được khi mất mạng |
| `icons/` | Icon app (192, 512, maskable, apple-touch) |
| `firestore.rules` | Rule bảo mật: mỗi người chỉ đọc/ghi dữ liệu của mình |

## Cài đặt
1. Tạo project tại [Firebase Console](https://console.firebase.google.com), thêm Web app, copy `firebaseConfig` vào `index.html`.
2. Bật **Authentication → Email/Password**.
3. Bật **Firestore Database**, dán nội dung `firestore.rules` vào tab Rules.
4. Upload toàn bộ thư mục lên repo GitHub, vào **Settings → Pages → Deploy from branch → main / root**.
5. Firebase → **Authentication → Settings → Authorized domains**: thêm `<tên-github>.github.io`.

## Dùng trên iPhone
Mở link bằng Safari → Chia sẻ → **Thêm vào MH chính**.

## Cập nhật phiên bản
Đổi `const C = "goals-v1"` trong `sw.js` thành `goals-v2` mỗi lần sửa code để máy người dùng tải bản mới.
