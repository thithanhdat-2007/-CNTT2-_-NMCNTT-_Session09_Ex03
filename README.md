# Hướng dẫn cài đặt VS Code và thực hành Markdown

## 1. Báo cáo phân tích Input/Output

- **Input:** Văn bản thô trong file `.md`, gồm nội dung hướng dẫn và các ký hiệu Markdown như `#`, dấu backtick, dấu `|`, `- [ ]`. Các ký hiệu này được gõ trực tiếp trong khung soạn thảo của StackEdit.
- **Xử lý:** Parser phân tích cú pháp Markdown và chuyển nội dung sang dạng hiển thị.
- **Output:** Bản xem trước trên StackEdit có tiêu đề rõ ràng, tên biến được định dạng Inline Code, khối Python được tô màu cú pháp, bảng so sánh có hàng/cột và danh sách công việc có ô đánh dấu.

**Lưu ý:** Render Markdown chỉ định dạng nội dung để đọc, không thực thi code Python hoặc câu lệnh Terminal.

## 2. Cài đặt VS Code trên Windows

1. Truy cập [trang tải VS Code](https://code.visualstudio.com/download), chọn bản phù hợp với máy Windows.
2. Mở bộ cài, làm theo hướng dẫn và hoàn tất cài đặt.
3. Mở VS Code. Để thực hành Python, cài thêm Python từ [python.org](https://www.python.org/downloads/) và extension **Python** của Microsoft trong mục Extensions.
4. Mở thư mục bài tập trong VS Code, tạo file `hello.py`.
5. Nhấn `Ctrl+Shift+P`, tìm `Python: Select Interpreter` và chọn bản Python đã cài.

> Extension Python hỗ trợ soạn và chạy code trong VS Code; bạn vẫn cần cài trình thông dịch Python riêng.

## 3. Inline Code và code Python

Tên biến ngắn như `ten`, `diem` và `trung_binh` được đặt trong một cặp dấu backtick để phân biệt với văn bản giải thích.

**Dán đoạn dưới vào file `hello.py`, không dán trực tiếp vào Terminal:**

```python
ten = "Sinh viên PTIT"
diem = [7, 8, 9]
trung_binh = sum(diem) / len(diem)

print(f"Xin chào {ten}!")

for thu_tu, gia_tri in enumerate(diem, start=1):
    print(f"Điểm bài {thu_tu}: {gia_tri}")

print(f"Điểm trung bình: {trung_binh:.2f}")

if trung_binh >= 5:
    print("Kết quả: Đạt")
else:
    print("Kết quả: Chưa đạt")
```

Khối code khai báo ngôn ngữ `python` ngay sau ba dấu backtick mở đầu để trình xem tô màu cú pháp.

**Lệnh gõ vào Terminal PowerShell**, tại thư mục chứa `hello.py` sau khi lưu file:

```powershell
python --version
python hello.py
```

Lệnh đầu kiểm tra phiên bản Python; lệnh sau chạy chương trình. Nếu máy chỉ nhận lệnh `py`, dùng `py --version` và `py hello.py` tương ứng.

## 4. So sánh StackEdit và VS Code

| Tiêu chí | StackEdit | VS Code |
| --- | --- | --- |
| Sử dụng | Soạn Markdown trực tiếp trên trình duyệt | Soạn tài liệu và lập trình trong ứng dụng trên máy |
| Ưu điểm khi học Markdown | Có khung soạn thảo và xem trước, dễ đối chiếu cú pháp | Có xem trước Markdown và quản lý tài liệu cùng mã nguồn |
| Hỗ trợ lập trình | Phù hợp trình bày đoạn code trong tài liệu | Có Terminal tích hợp và có thể mở rộng bằng extension |
| Phù hợp | Viết ghi chú, báo cáo Markdown nhanh | Làm dự án gồm nhiều file và chạy chương trình |

## 5. Task List kiểm tra tiến độ

Chỉ đổi `[ ]` thành `[x]` khi đã thực hiện xong công việc.

- [ ] Tải bộ cài VS Code phù hợp với máy.
- [ ] Cài đặt và mở được VS Code.
- [ ] Cài Python.
- [ ] Cài extension Python của Microsoft.
- [ ] Chọn trình thông dịch Python trong VS Code.
- [ ] Tạo và lưu file `hello.py`.
- [ ] Chạy chương trình và kiểm tra kết quả.
- [ ] Xem trước tài liệu trên StackEdit và lưu file `.md`.

## 6. Escape ký tự đặc biệt

Đặt dấu gạch chéo ngược trước ký tự đặc biệt để tránh bị hiểu là cú pháp Markdown.

Ví dụ mã nguồn:

```markdown
\*Đây là dấu sao được hiển thị nguyên văn\*.
\# Đây không phải tiêu đề.
```

Kết quả render:

\*Đây là dấu sao được hiển thị nguyên văn\*.

\# Đây không phải tiêu đề.

## 7. Lưu và nộp bài

1. Mở hoặc dán nội dung file này vào StackEdit.
2. Kiểm tra khối Python, bảng so sánh, Task List và các ký tự escape ở khung xem trước.
3. Xuất tài liệu dưới định dạng Markdown, đặt tên `README.md`.
4. Đưa file lên repository theo mẫu `[Tên Lớp]_[Môn Học]_Session08_Ex03`, thay tên lớp và môn học bằng thông tin thực tế.

## Tài liệu tham khảo

- [Hướng dẫn cài VS Code trên Windows](https://code.visualstudio.com/docs/setup/windows)
- [Hướng dẫn Python trong VS Code](https://code.visualstudio.com/docs/python/python-tutorial)
- [StackEdit](https://stackedit.io/)
