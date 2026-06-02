# Hello World - Next.js Website

Một website đơn giản "Hello World" được xây dựng bằng **Next.js 14** với **App Router** và **CSS thuần** (vanilla CSS).

## 📋 Yêu cầu Hệ thống

- **Node.js**: 16.8+ hoặc cao hơn
- **npm** hoặc **yarn** hoặc **pnpm**

## 🚀 Hướng dẫn Cài đặt và Chạy

### 1. Cài đặt Dependencies

```bash
# Sử dụng npm
npm install

# Hoặc sử dụng yarn
yarn install

# Hoặc sử dụng pnpm
pnpm install
```

### 2. Chạy Development Server

```bash
# Sử dụng npm
npm run dev

# Hoặc sử dụng yarn
yarn dev

# Hoặc sử dụng pnpm
pnpm dev
```

Mở trình duyệt và truy cập: **http://localhost:3000**

### 3. Build cho Production

```bash
# Sử dụng npm
npm run build

# Hoặc sử dụng yarn
yarn build

# Hoặc sử dụng pnpm
pnpm build
```

### 4. Chạy Production Server

```bash
# Sử dụng npm
npm start

# Hoặc sử dụng yarn
yarn start

# Hoặc sử dụng pnpm
pnpm start
```

## 📁 Cấu trúc Dự án

```
hello-world-nextjs/
├── app/
│   ├── layout.tsx          # Root layout - HTML wrapper chính
│   ├── page.tsx            # Trang chủ (Home page)
│   └── globals.css         # CSS toàn cục - biến, responsive, animations
├── package.json            # Dependencies và scripts
├── tsconfig.json           # Cấu hình TypeScript
├── next.config.js          # Cấu hình Next.js
├── .gitignore              # Git ignore rules
└── README.md               # Tệp này
```

## 📄 Giải Thích Từng File

### `package.json`
Quản lý dependencies và scripts của dự án.
- **Dependencies**: `react`, `react-dom`, `next`
- **DevDependencies**: `typescript`, type definitions, eslint
- **Scripts**:
  - `dev`: Chạy development server
  - `build`: Build ứng dụng cho production
  - `start`: Chạy server ở chế độ production
  - `lint`: Kiểm tra code quality

### `tsconfig.json`
Cấu hình TypeScript cho dự án. Đảm bảo strict mode được bật để phát hiện lỗi sớm.

### `next.config.js`
Cấu hình Next.js. Hiện tại sử dụng strict mode của React.

### `app/layout.tsx`
**Root Layout Component** - Tệp bắt buộc trong App Router.
- Định nghĩa metadata (title, description, keywords)
- Bao bọc tất cả các trang
- Import file `globals.css`
- Thiết lập ngôn ngữ (`lang="vi"`)

### `app/page.tsx`
**Home Page Component** - Trang chủ của ứng dụng.
- Hiển thị tiêu đề "Hello, World!"
- Hiển thị đoạn mô tả
- Tất cả styling được xử lý bởi CSS variables trong `globals.css`

### `app/globals.css`
**Tệp CSS Toàn Cục** - Nơi tất cả styling được định nghĩa.

#### Cấu trúc của `globals.css`:

1. **CSS Variables** (`:root`)
   - Màu sắc: primary, background, text, border, shadow
   - Typography: font-family, font-sizes, line-heights
   - Spacing: base, small, large
   - Animation: transition duration, timing

2. **Reset và Base Styles**
   - Reset margin/padding mặc định
   - Thiết lập font, màu, background cho body

3. **Layout Container**
   - Sử dụng Flexbox để căn giữa nội dung
   - min-height 100vh (full viewport height)

4. **Typography**
   - `h1`: Heading lớn với hiệu ứng hover (scale, color change)
   - `p`: Paragraph với hiệu ứng hover (color change)

5. **Animations**
   - `fadeIn`: Animation hiệu ứng mở từ từ khi tải trang

6. **Responsive Design**
   - Mobile (≤640px): Font size nhỏ hơn, spacing giảm
   - Tablet (641px - 1024px): Font size trung bình
   - Desktop (≥1025px): Font size lớn, spacing đầy đủ

7. **Accessibility**
   - Focus styles cho keyboard navigation
   - Support cho `prefers-reduced-motion`
   - Dark mode support qua `prefers-color-scheme`

## ✨ Tính Năng

✅ **Next.js 14 + App Router** - Cấu trúc hiện đại  
✅ **TypeScript** - Type safety  
✅ **CSS Variables** - Dễ maintain và customize  
✅ **Responsive Design** - Tối ưu cho mobile, tablet, desktop  
✅ **Animations** - Hiệu ứng fade-in, hover effects  
✅ **Accessibility** - Focus styles, dark mode, reduce motion support  
✅ **No External UI Library** - Chỉ sử dụng CSS thuần  
✅ **Code Comments** - Dễ hiểu và bảo trì  

## 🎨 Customize

### Thay đổi Màu Sắc
Chỉnh sửa CSS variables trong `app/globals.css`:

```css
:root {
  --color-primary: #6366f1; /* Thay đổi màu chính */
  --color-background: #ffffff; /* Thay đổi màu nền */
  --color-text: #1f2937; /* Thay đổi màu chữ */
}
```

### Thay đổi Font
Sửa `--font-family-base` trong `app/globals.css`:

```css
:root {
  --font-family-base: 'Your Font Family', sans-serif;
}
```

### Thay đổi Responsive Breakpoints
Chỉnh sửa media queries trong `app/globals.css`:

```css
@media (max-width: 640px) {
  /* Mobile styles */
}

@media (min-width: 641px) and (max-width: 1024px) {
  /* Tablet styles */
}

@media (min-width: 1025px) {
  /* Desktop styles */
}
```

## 🔧 Troubleshooting

### Port 3000 đã bị sử dụng
```bash
# Sử dụng port khác
npm run dev -- -p 3001
```

### Module not found error
```bash
# Xóa node_modules và cài đặt lại
rm -rf node_modules
npm install
```

### Build error
```bash
# Xóa .next folder
rm -rf .next
npm run build
```

## 📚 Tài Liệu Tham Khảo

- [Next.js Documentation](https://nextjs.org/docs)
- [App Router Guide](https://nextjs.org/docs/app)
- [CSS Variables MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/--*)
- [Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)

## 📝 License

MIT License - Tự do sử dụng và chỉnh sửa.

---

**Tạo bởi**: janjanheo  
**Tháng 6, 2026**
