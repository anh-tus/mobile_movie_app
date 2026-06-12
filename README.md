# 🎬 Mobile Movie App

Ứng dụng xem phim trên mobile được xây dựng bằng React Native & Expo.

## 🛠 Tech Stack

- [Expo](https://expo.dev) ~54.0.34
- [React Native](https://reactnative.dev) 0.81.5
- [Expo Router](https://docs.expo.dev/router/introduction) – File-based routing
- [NativeWind](https://www.nativewind.dev) + [Tailwind CSS](https://tailwindcss.com) – Styling
- TypeScript

## 📁 Cấu trúc thư mục

```
mobile_movie_app/
├── app/              # Màn hình & routing (file-based)
│   ├── _layout.tsx
│   ├── globals.css
│   └── index.tsx
├── assets/           # Hình ảnh, icon
├── app.json          # Cấu hình Expo
├── tailwind.config.js
└── tsconfig.json
```

## 🚀 Bắt đầu

### Cài đặt dependencies

```bash
npm install
```

### Chạy ứng dụng

```bash
npx expo start
```

Sau đó chọn môi trường:

- **Android**: Nhấn `a` hoặc dùng Android Emulator
- **iOS**: Nhấn `i` hoặc dùng iOS Simulator
- **Expo Go**: Quét QR code bằng app Expo Go

## 🌿 Git Workflow

| Nhánh  | Mục đích                         |
| ------ | -------------------------------- |
| `main` | Production – sản phẩm ổn định    |
| `dev`  | Development – code tính năng mới |

```bash
# Phát triển tính năng mới
git checkout dev

# Merge vào main khi hoàn thiện
git checkout main
git merge dev
git push origin main
```

## 📦 Scripts

```bash
npm start          # Khởi động Expo dev server
npm run android    # Chạy trên Android
npm run ios        # Chạy trên iOS
npm run web        # Chạy trên Web
npm run lint       # Kiểm tra lỗi code
```
