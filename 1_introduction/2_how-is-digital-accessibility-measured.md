# Khả năng tiếp cận kỹ thuật số được đo lường như thế nào?

## Tổng quan

Khả năng tiếp cận kỹ thuật số là thiết kế và xây dựng các dịch vụ kỹ thuật số sao cho mọi người, bất kể khả năng tinh thần hay thể chất, đều có thể tương tác với sản phẩm một cách có ý nghĩa và bình đẳng.

## Cách đo lường khả năng tiếp cận

### 1. Tiêu chuẩn đánh giá

Khả năng tiếp cận được đo lường dựa trên các tiêu chuẩn quốc tế. Việc lựa chọn tiêu chuẩn phụ thuộc vào:
- Ngành nghề và loại sản phẩm
- Luật pháp và chính sách địa phương
- Mục tiêu tiếp cận tổng thể

**Khuyến nghị**: Tuân thủ phiên bản mới nhất của **WCAG** (Web Content Accessibility Guidelines).

### 2. Kiểm toán khả năng tiếp cận

Kiểm toán sử dụng nhiều phương pháp:
- Kiểm tra thiết kế
- Kiểm tra tự động
- Kiểm tra thủ công
- Kiểm tra với công nghệ hỗ trợ (AT)

**Lưu ý**: Cần thực hiện kiểm tra liên tục trong suốt vòng đời sản phẩm, không chỉ một lần.

## WCAG - Tiêu chuẩn vàng

### Giới thiệu
- **WCAG** (Web Content Accessibility Guidelines) là tiêu chuẩn quốc tế
- Được phát triển bởi W3C
- Áp dụng cho web và ứng dụng di động
- Phiên bản hiện tại: **WCAG 2.2**

### Ba mức độ tuân thủ

| Mức độ | Số tiêu chí | Mô tả |
|--------|-------------|-------|
| **A** | 30 | Cơ bản - Tất cả sản phẩm phải đạt |
| **AA** | 50 | Tiêu chuẩn - Mục tiêu phổ biến |
| **AAA** | 78 | Cao cấp - Mức độ cao nhất |

**Lưu ý**: Các mức độ có tính lũy tiến. Để đạt AA, phải vượt qua cả A và AA.

## Nguyên tắc POUR

![alt text](image.png)

WCAG dựa trên 4 nguyên tắc cơ bản (POUR):

### 1. **P**erceivable (Có thể nhận thức)
Người dùng phải có thể nhận thức được tất cả thông tin cần thiết.

**Ví dụ thực tế:**
- Thêm alt text cho hình ảnh
- Phụ đề cho video
- Đảm bảo màu sắc không phải là phương pháp duy nhất để truyền tải ý nghĩa.

### 2. **O**perable (Có thể vận hành)
Người dùng phải có thể điều khiển giao diện.

**Ví dụ thực tế:**
- Hỗ trợ bàn phím và cảm ứng
- Điều khiển video đầy đủ
- Cho phép gia hạn thời gian khi cần

### 3. **U**nderstandable (Có thể hiểu)
Người dùng phải hiểu được thông tin và cách sử dụng.

**Ví dụ thực tế:**
- Viết nội dung rõ ràng, đơn giản
- Điều hướng dễ dự đoán
- Thông báo lỗi rõ ràng

### 4. **R**obust (Mạnh mẽ)
Sản phẩm phải tương thích với công nghệ hỗ trợ và thiết bị khác nhau.

**Ví dụ thực tế:**
- Hoạt động trên nhiều trình duyệt
- Tương thích với trình đọc màn hình
- Responsive trên mọi kích thước màn hình

## Kết luận

POUR không phải là quy tắc cứng nhắc mà là cách tiếp cận để hiểu và đáp ứng nhu cầu đa dạng của người dùng. Mục tiêu cuối cùng là tạo ra trải nghiệm kỹ thuật số bao gồm tất cả mọi người.

---

*Lưu ý: WCAG 3.0 đang trong giai đoạn thử nghiệm và dự kiến sẽ trở thành tiêu chuẩn chính thức trong vài năm tới.*

---

## WCAG 2.2 — Hiệu lực từ 10/2023

9 Success Criteria mới so với 2.1:

| SC | Tên | Mức | Mô tả |
|----|-----|-----|-------|
| 2.4.11 | Focus Not Obscured | AA | Element focus không bị che toàn bộ |
| 2.4.12 | Focus Not Obscured (Enhanced) | AAA | Element focus không bị che gì cả |
| 2.4.13 | Focus Appearance | AAA | Vùng focus đủ lớn, tương phản rõ |
| 2.5.7 | Dragging Movements | AA | Thao tác kéo phải có alternative |
| 2.5.8 | Target Size (Minimum) | AA | Target ≥ 24×24 CSS px |
| 3.2.6 | Consistent Help | A | Help mechanism cùng vị trí trên mọi trang |
| 3.3.7 | Redundant Entry | A | Không hỏi lại thông tin đã nhập |
| 3.3.8 | Accessible Authentication | AA | Không dùng cognitive test để login |
| 3.3.9 | Accessible Authentication (Enhanced) | AAA | Không yêu cầu nhận diện đối tượng |

> ⚠️ **Lưu ý:** WCAG 2.2 đặc biệt nhấn mạnh vào khả năng tiếp cận cho người khuyết tật nhận thức (ADHD, tự kỷ, dementia, khó đọc).

Ref: https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/

## EAA — EU Accessibility Act (Hiệu lực 28/6/2025)

EAA (EU Directive 2019/882) chính thức có hiệu lực từ **28/6/2025** tại tất cả 27 quốc gia EU.

**Yêu cầu tuân thủ cho:** thương mại điện tử (e-commerce), ngân hàng, e-book, ứng dụng di động, ATM, điện thoại thông minh, tivi thông minh, dịch vụ thông tin liên lạc điện tử (ECS).

**Không tuân thủ = vi phạm pháp luật EU**, có thể bị phạt tiền hoặc buộc rút sản phẩm khỏi thị trường. Mỗi quốc gia tự quy định mức phạt cụ thể.

**Quy định riêng của một số quốc gia:**
- Hà Lan: ACM giám sát tuân thủ từ 28/6/2025 cho e-commerce và ECS
- Ireland: ComReg giám sát ECS, CCPC giám sát sản phẩm và e-commerce
- Phần Lan: Traficom giám sát sản phẩm và dịch vụ

Ref: https://ec.europa.eu/social/main.jsp?catId=1202 | https://eur-lex.europa.eu/EN/legal-content/summary/accessibility-of-products-and-services.html

---

## WCAG 3.0 Working Draft — Theo dõi (chưa enforce, 10/2026)

> ⚠️ **WCAG 3.0 vẫn là Working Draft** — chưa có hiệu lực. **WCAG 2.2 vẫn là chuẩn tuân thủ chính thức.** Khuyến nghị: tiếp tục tuân thủ WCAG 2.2 AA đầy đủ, đồng thời theo dõi WCAG 3.0 development để chuẩn bị tương lai.

WCAG 3.0 Working Draft được cập nhật **September 2026** (W3C, 10/9/2026), đánh dấu bước tiến lớn về conformance model.

### Thay đổi lớn so với WCAG 2.x

| Khía cạnh | WCAG 2.x | WCAG 3.0 |
|-----------|----------|----------|
| **Conformance** | Pass/Fail (A / AA / AAA) | 6 reporting tiers + impact-based tags |
| **Cấu trúc** | 13-17 Guidelines | Functional categories (Perceivable, Operable...) |
| **Mức độ** | Fixed levels (A→AA→AAA) | Gradient: bronze/silver/gold/platinum/steel/titanium |
| **Đo lường** | Manual sampling | Machine-actionable assertions |

### 6 Reporting Tiers mới
- **Titanium**: gần như hoàn hảo, ≤0.01 failures per page
- **Platinum**: enterprise-grade, ≤0.05 failures/page
- **Gold**: cao nhất practical, ≤0.25 failures/page
- **Silver**: equivalent WCAG 2.1 AA, ≤0.5 failures/page
- **Bronze**: equivalent WCAG 2.1 A, ≤1 failure/page
- **Steel**: baseline, ≥50% pages meet critical requirements

### Các features mới đáng chú ý
- **Impact-based requirement tags** thay vì level cứng nhắc — cùng 1 requirement có thể "crash" (fatal) hoặc "inconvenience" (minor) tùy ngữ cảnh
- **Automated testing** được khuyến khích nhiều hơn
- Áp dụng cho: websites, native apps, e-books, authoring tools, authoring tool outputs

### Timeline dự kiến
- Working Draft tiếp tục được cập nhật (latest: September 2026)
- Không có enforcement date cố định
- W3C đã xác nhận **không deprecated WCAG 2.x** khi 3.0 ra mắt
- ADA Title II (US): enforcement vẫn dựa trên WCAG 2.1 AA

Ref: https://www.w3.org/WAI/news/2026-09-10/wcag3/ | https://www.w3.org/TR/wcag-3.0/

