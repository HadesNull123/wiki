# Đóng góp nội dung

Bạn có thể đóng góp cho Blockchain Wiki bằng cách sửa 1 bài viết đã có, đóng góp bài viết mới, hoặc viết cả một series mới.

## Trước khi bắt đầu

Blockchain Wiki đề cao tính khách quan và dễ hiểu.

- Giọng văn trung lập, khách quan, không thiên vị
- Dựa trên facts thay vì opinions
- Trong sáng, dễ hiểu, dùng cấu trúc câu và từ đơn giản
- Nếu có thể, hãy thêm hình minh hoạ
- Không quảng cáo

## Cách làm

1. Fork [Blockchain Wiki Repo](https://github.com/TradaTech/wiki)
2. Thực hiện sửa
3. Tạo Pull Request vào `master` branch của Blockchain Wiki repo
4. Đợi [Netlify](https://www.netlify.com) deploy preview thành công, xem thử và sửa nếu có vấn đề

Chúng tôi sẽ kiểm tra, merge, và deploy sớm nhất có thể.

!> Bạn nên xem thử ở máy nhà trước khi tạo Pull Request<br>1. Cài [Docsify](https://docsify.js.org/) `npm i docsify-cli -g`<br>2. `docsify serve ./docs`

?> Để thêm 1 mục vào thanh mục lục bên trái, hãy sửa ở file `_sidebar.md` nằm _cùng thư mục_.

## Cách format bài viết

Các bài được viết bằng [markdown](https://www.markdownguide.org/cheat-sheet/). Ngoài ra, Blockchain Wiki hỗ trợ thêm `#>` (subheader), `?>` (info/tip box), `!>` (warn box).

**Ví dụ:**

---

#> Đây là 1 sub-header, hãy để ngay sau title chính để nhấn mạnh.

> Đây là 1 blockquote.

?> _NOTE_ Đây là 1 ô ghi chú.

!> **WARN** Đây là 1 ghi chú quan trọng.

---

Để có kết quả như trên, hãy sử dụng markdown như sau:

```markdown
#> Đây là 1 sub-header, hãy để ngay sau title chính để nhấn mạnh.

> Đây là 1 blockquote.

?> _NOTE_ Đây là 1 ô ghi chú.

!> **WARN** Đây là 1 ghi chú quan trọng.
```

## Liên hệ

Nếu có khó khăn ghì trong quá trình viết, có thể liên hệ qua [Telegram](https://t.me/tradatech) hoặc [Facebook](https://facebook.com/tradatech).
