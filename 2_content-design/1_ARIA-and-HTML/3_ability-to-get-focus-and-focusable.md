# Khả năng lấy nét và kích hoạt bằng bàn phím (Nguyên tắc 3 và 4)

> ⚠️ **Cập nhật 10/2026:** Kiến thức nền trong file này đúng. Cần lưu ý WCAG 2.2 SC 2.4.11 (Focus Not Obscured - AA) và SC 2.4.13 (Focus Appearance - AAA) về yêu cầu focus indicator rõ ràng, đủ lớn.

---

## 🎯 Tổng quan

Một phần tử accessible cần có **CẢ HAI** đặc tính:
1. **Focusable** - Có thể chọn bằng Tab
2. **Kích hoạt được** - Có thể dùng bằng Enter/Space

---

## 1. 🔍 Focusable (Có thể lấy nét)

### Định nghĩa
**Focusable** = "Có thể CHỌN được bằng bàn phím"

Khi bạn nhấn **Tab**, phần tử được chọn làm điểm hiện hành để tương tác.

### Ví dụ thực tế
**Remote TV:** Các nút Power, Volume+, Volume-, Channel+ - bạn có thể di chuyển giữa chúng.

### Phần tử mặc định focusable
- **Liên kết:** `<a href="...">`
- **Nút:** `<button>`
- **Ô nhập liệu:** `<input>`, `<textarea>`, `<select>`

### Cách nhận biết
Khi nhấn **Tab**, đường viền xanh lam xuất hiện xung quanh phần tử đang focus.

> **💡 Câu hỏi:** "Tôi có thể CHỌN cái này bằng phím Tab không?"

---

## 2. ⚡ Khả năng kích hoạt (Enter/Space)

### Định nghĩa
**Kích hoạt được** = "Có thể DÙNG được bằng bàn phím"

Bước tiếp theo sau khi đã focus - phần tử có thể được kích hoạt bằng Enter hoặc Space.

### Ví dụ thực tế
**Remote TV:** Sau khi focus tới nút Volume+, bạn phải NHẤN (kích hoạt) để tăng âm lượng.

### Phím kích hoạt trên web

#### ⌨️ Phím Enter
**Mục đích:** Kích hoạt hành động chính

| Phần tử | Hành động |
|---------|-----------|
| `<a>` | Đi đến URL |
| Nút submit | Gửi form |

#### 🔘 Phím Space
**Mục đích:** Thay đổi trạng thái

| Phần tử | Hành động |
|---------|-----------|
| `<button>` | Thực hiện hành động |
| `<input type="checkbox">` | Tick/bỏ tick |
| Switch | Bật/tắt |

> **💡 Câu hỏi:** "Sau khi CHỌN (focus), tôi có thể DÙNG (activate) nó bằng phím nào?"

---

## 🔗 Sự kết hợp quan trọng

### Ví dụ tốt: `<button>`

```html
<button>Click me</button>
```

✅ **Focusable:** Tab → đường viền focus hiển thị  
✅ **Kích hoạt được:** Space hoặc Enter → kích hoạt nút

### Ví dụ xấu: `<div>` với onclick

```html
<div onclick="doSomething()" class="pretty-button">Click me</div>
```

```css
.pretty-button {
  /* Rất nhiều CSS đẹp đẽ */
}
```

#### ❌ Vấn đề 1: Không focusable
- `<div>` không mặc định focusable
- Người dùng bàn phím không thể tab tới
- **Vi phạm:** Nguyên tắc Operable

#### ❌ Vấn đề 2: Không kích hoạt được
- Ngay cả với `tabindex="0"`
- Không thể kích hoạt bằng Space/Enter
- Chỉ phản hồi `onclick` (chuột)
- **Vi phạm nghiêm trọng:** Nguyên tắc Operable

---

## 🛠️ Cách sửa chữa

### Nguyên tắc: Sử dụng HTML đúng ngữ nghĩa

**Thay vì `<div>`, hãy dùng `<button>`**

```html
<button>Click me</button>
```

### Lợi ích của `<button>`

| Đặc tính | Tự động có |
|----------|------------|
| **Focusable** | ✅ |
| **Kích hoạt Enter** | ✅ |
| **Kích hoạt Space** | ✅ |
| **Role button** | ✅ (screen reader biết) |

---

## 📊 Tóm tắt so sánh

| Đặc tính | Focusable | Kích hoạt Enter/Space |
|----------|-----------|----------------------|
| **Câu hỏi** | "Có thể CHỌN bằng Tab?" | "Có thể DÙNG bằng Enter/Space?" |
| **Ví dụ** | Đường viền xanh khi tab | Nhấn Space bật/tắt, Enter submit |
| **Cách đạt được** | Phần tử interactive mặc định hoặc `tabindex="0"` | Chỉ có tự động với HTML đúng |

---

## 💡 Bài học quan trọng

> **🎯 Luôn sử dụng đúng thẻ HTML cho đúng mục đích**

**Lợi ích:**
- Tự động xử lý hầu hết vấn đề accessibility
- Không cần can thiệp thủ công
- Code sạch và maintainable

**Chỉ dùng `tabindex` và ARIA khi thực sự cần thiết**

---

## 🔍 Kiểm tra nhanh

### Checklist
- [ ] Phần tử có thể focus bằng Tab?
- [ ] Có thể kích hoạt bằng Enter/Space?
- [ ] Sử dụng đúng thẻ HTML?
- [ ] Không dùng `<div>` + `onclick`?

### Test thực tế
1. **Tab qua trang** - Kiểm tra focus indicator
2. **Enter/Space** - Kiểm tra kích hoạt
3. **Screen reader** - Kiểm tra thông báo đúng role