# Tài liệu (Documents)

## 🎯 Tổng quan

Bên cạnh cấu trúc, có nhiều yếu tố HTML cần cân nhắc để đảm bảo khả năng tiếp cận (a11y). Mô-đun này tập trung vào các yếu tố phổ biến, dễ sai nhưng quan trọng: tiêu đề trang, ngôn ngữ, và iFrame.

> Lưu ý: Nên nắm vững HTML ngữ nghĩa trước. Bạn cũng nên xem lại mô-đun ARIA và HTML trong khóa học này.

---

## 🏷️ Tiêu đề trang (`<title>`)

- Xác định nội dung của trang/màn hình, nằm trong thẻ `<head>`
- Tương đương ngữ nghĩa với `<h1>` (chủ đề chính), nhưng không hiển thị trên trang
- Quan trọng cho người dùng và SEO; cần chính xác, độc nhất, súc tích
- Với SPA: cập nhật `document.title` (có thể cần thông báo tới screen reader)

### ✅ Viết tiêu đề hiệu quả
- Ưu tiên nội dung quan trọng lên trước
- Tránh nhồi nhét từ khóa; giữ ~55–60 ký tự đầu

#### ❌ Không nên
```html
<title>The Food Channel | Outrageous Pumpkins | Season 3</title>
```

#### ✅ Nên làm
```html
<title>Season 3 | Outrageous Pumpkins | The Food Channel</title>
```

> Điểm chính: Công cụ tìm kiếm thường chỉ hiển thị ~55–60 ký tự đầu của tiêu đề.

---

## 🌐 Ngôn ngữ (Language)

### 1) Ngôn ngữ toàn trang (`<html lang>`)
- Đặt ngôn ngữ mặc định cho toàn bộ trang
- Dùng mã ISO 2 ký tự (ví dụ: `vi`, `en`) để tương thích AT
- Khi thiếu, AT dùng ngôn ngữ hệ thống của người dùng → phát âm sai, khó hiểu

#### ❌ Không nên
```html
<html>...</html>
```

#### ✅ Nên làm
```html
<html lang="en">...</html>
```

- `lang` chỉ nhận 1 ngôn ngữ tại một thời điểm → đặt theo ngôn ngữ chính của trang

#### ❌ Không nên
```html
<html lang="ar,en,fr,pt">...</html>
```

#### ✅ Nên làm
```html
<html lang="ar">...</html>
```

### 2) Ngôn ngữ theo phần (Inline `lang`)
- Ghi đè ngôn ngữ cho một đoạn cụ thể trong nội dung
- Đặt `lang` vào phần tử bao bọc đoạn khác ngôn ngữ

#### ❌ Không nên
```html
<html lang="en">
  <body>
    <div>
      <p>While traveling in Estonia this summer, I often asked,
        "Kas sa räägid inglise keelt?" when I met someone new.</p>
    </div>
  </body>
</html>
```

#### ✅ Nên làm
```html
<html lang="en">
  <body>
    <div>
      <p>While traveling in Estonia this summer, I often asked,
        <span lang="et">"Kas sa räägid inglise keelt?"</span>
        when I met someone new.</p>
    </div>
  </body>
</html>
```

---

## 🧩 iFrame (`<iframe>`)

- Nhúng trang HTML khác hoặc nội dung bên thứ ba (quảng cáo, video, analytics, nội dung tương tác)
- Mỗi `<iframe>` nên có `title` mô tả nội dung bên trong
- Cho phép cuộn (`scrolling="auto"` hoặc `"yes"`) để người dùng tiếp cận nội dung ẩn
- Hộp chứa nên linh hoạt chiều rộng/chiều cao

#### ❌ Không nên
```html
<iframe src="https://www.youtube.com/embed/3obixhGZ5ds"></iframe>
```

#### ✅ Nên làm
```html
<iframe
  title="Google Pixel - Lizzo in Real Tone"
  src="https://www.youtube.com/embed/3obixhGZ5ds"
  scrolling="auto">
</iframe>
```

---

## ✅ Kiểm tra nhanh

- [ ] Tiêu đề trang súc tích, độc nhất, có từ khóa chính?
- [ ] `document.title` cập nhật đúng (SPA)?
- [ ] Có đặt `<html lang="...">` với mã ISO 2 ký tự?
- [ ] Các đoạn khác ngôn ngữ có gán `lang` cục bộ?
- [ ] Mọi `<iframe>` có `title` mô tả, có thể cuộn?

---

## 📚 Tham khảo
- HTML `<title>`: MDN, W3C
- Ngôn ngữ (`lang`): MDN, W3C i18n
- iFrame accessibility: W3C, WebAIM
- WCAG 2.2 SC 3.1.1 (Language of Page): `<html lang>` là yêu cầu A
- WCAG 2.2 SC 2.4.11 (Focus Not Obscured): Modal/iframe không được che focus indicator

