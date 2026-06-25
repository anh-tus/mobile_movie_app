# 🎬 Mobile Movie App

Ứng dụng xem phim trên thiết bị di động được xây dựng bằng React Native và Expo.

## 🛠 Công nghệ sử dụng

- **Framework:** [Expo](https://expo.dev) (~54.0.34) & [React Native](https://reactnative.dev) (0.81.5)
- **Định tuyến (Routing):** [Expo Router](https://docs.expo.dev/router/introduction) – Hệ thống định tuyến dựa trên file
- **Giao diện (Styling):** [NativeWind](https://www.nativewind.dev) v4 kết hợp với [Tailwind CSS](https://tailwindcss.com) v3
- **Ngôn ngữ:** TypeScript

## 📁 Cấu trúc thư mục

```text
mobile_movie_app/
├── app/              # Màn hình & routing (Expo Router)
│   ├── (tabs)/       # Màn hình thanh điều hướng (Home, Search, Saved, Profile)
│   ├── movies/       # Màn hình chi tiết phim
│   ├── _layout.tsx   # Layout chung toàn ứng dụng
│   └── globals.css   # Cấu hình CSS toàn cục cho Tailwind
├── assets/           # Tài nguyên tĩnh (Hình ảnh, icon, fonts)
├── components/       # Các UI component tái sử dụng (VD: SearchBar)
├── constants/        # Các hằng số (constants) của dự án
├── interfaces/       # Các định nghĩa TypeScript interface cho dữ liệu (Movie, User...)
├── types/            # Các định nghĩa kiểu bổ sung
├── app.json          # Cấu hình ứng dụng Expo
├── tailwind.config.js # Cấu hình Tailwind CSS
└── tsconfig.json     # Cấu hình TypeScript
```

## 🚀 Hướng dẫn cài đặt và chạy

### 1. Cài đặt các gói thư viện (Dependencies)

```bash
npm install
```

### 2. Khởi động ứng dụng

```bash
npx expo start
```

Sau khi máy chủ khởi động, bạn có thể chọn môi trường chạy:

- **Android**: Nhấn phím `a` để mở trên Android Emulator
- **iOS**: Nhấn phím `i` để mở trên iOS Simulator
- **Thiết bị thật**: Tải ứng dụng **Expo Go** trên điện thoại và quét mã QR hiển thị trên màn hình terminal.

## 📦 Các lệnh (Scripts) hữu ích

Bạn có thể sử dụng các lệnh sau trong quá trình phát triển:

```bash
npm start          # Khởi động Expo dev server
npm run android    # Chạy trực tiếp trên Android
npm run ios        # Chạy trực tiếp trên iOS
npm run web        # Chạy trên nền tảng Web
npm run lint       # Kiểm tra lỗi code bằng ESLint
```

## 🌿 Quy trình quản lý mã nguồn (Git Workflow)

| Tên nhánh | Mục đích sử dụng |
| ------ | -------------------------------- |
| `main` | Production – Chứa mã nguồn ổn định, dùng để phát hành |
| `dev`  | Development – Nhánh phát triển chính, chứa các tính năng mới |

**Cách phát triển tính năng mới:**

```bash
# Chuyển sang nhánh phát triển
git checkout dev

# (Code và commit các thay đổi của bạn tại đây)

# Khi tính năng hoàn thiện, gộp (merge) vào nhánh main
git checkout main
git merge dev
git push origin main
```