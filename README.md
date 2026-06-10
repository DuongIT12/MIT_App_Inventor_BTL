# MIT_App_Inventor_BTL
# 1. QUY TRÌNH TẠO RA PHẦN MỀM & THÀNH PHẦN GIAO DIỆN

## Thanh công cụ (Palette) gồm những gì?

Khi thiết kế giao diện (**Designer Mode**) trong **MIT App Inventor**, thanh công cụ bên trái (**Palette**) là nơi chứa toàn bộ các thành phần (**Components**) được chia theo nhóm chức năng:

- **User Interface**  
  Chứa các đối tượng tương tác trực tiếp với người dùng như:  
  - *Button* (Nút bấm)  
  - *Label* (Nhãn hiển thị chữ)  
  - *TextBox* (Ô nhập dữ liệu)

- **Layout**  
  Dùng để sắp xếp bố cục các đối tượng:  
  - *HorizontalArrangement* (theo chiều ngang)  
  - *VerticalArrangement* (theo chiều dọc)  
  - *TableArrangement* (dạng bảng)

- **Media**  
  Các thành phần xử lý âm thanh, hình ảnh, máy ảnh:  
  - *Player*  
  - *Sound*  
  - *Camera*

- **Maps & Drawing/Animation**  
  Hỗ trợ vẽ bản đồ hoặc làm chuyển động game đơn giản:  
  - *Canvas*  
  - *ImageSprite*

- **Sensors**  
  Truy cập vào cảm biến của điện thoại:  
  - Gia tốc kế  
  - La bàn  
  - GPS

- **User Interface (WebViewer)**

  Thành phần đặc biệt để nhúng trang web trực tiếp vào ứng dụng.




# 2. THIẾT KẾ 3 SCREEN (GIAO DIỆN & LOGIC)

Bạn bấm vào nút **Add Screen...** ở phía trên màn hình để tạo đủ 3 màn hình với các chức năng sau:

---

## Màn hình 1: About (Giới thiệu bản thân)

### Giao diện (Designer)
- Dùng **VerticalArrangement** để căn giữa các đối tượng.  
- Thêm các **Label** để hiển thị thông tin cá nhân: Họ tên, Mã số sinh viên, Lớp, Trường.  
- Thêm 2 **Button**:  
  - `btnGoToMath` (Giải toán)  
  - `btnGoToWeb` (Xem trang web)
<img width="1899" height="918" alt="Screenshot 2026-06-09 205025" src="https://github.com/user-attachments/assets/a9d11d19-9315-48f4-9984-8b9fc7aee0a2" />

### Khối lệnh (Blocks)
- Sử dụng sự kiện:
  ```text
  when btnGoToMath.Click
  → open another screen screenName "Screen2"
<img width="1911" height="918" alt="18" src="https://github.com/user-attachments/assets/68c71c8a-a000-4f19-b0dd-a180cc654c73" />


## Thiết kế giao diện & logic

## Màn hình 2: Giải toán

### Giao diện (Designer)
- Dùng các **TextBox** để người dùng nhập dữ liệu đầu vào (ví dụ: số a và số b).  
- Dùng một **Button** đặt tên là `btnSolve` để kích hoạt tính năng giải toán.  
- Dùng một **Label** đặt tên là `lblResult` để hiển thị kết quả.
<img width="1909" height="887" alt="Screenshot 2026-06-09 205546" src="https://github.com/user-attachments/assets/8fbe3898-7ff0-432d-a024-8413df88c2fb" />

### Khối lệnh (Blocks)

<img width="1904" height="918" alt="19" src="https://github.com/user-attachments/assets/e35afbcf-f081-4220-8ebd-a05afe000ac2" />

- Sử dụng sự kiện:
  ```text
  when btnSolve.Click

<img width="1909" height="918" alt="16" src="https://github.com/user-attachments/assets/3d83f4ee-1e69-44ea-b5fd-02e0f7eda390" />


## Màn hình 3: Sử dụng Webview

## Giao diện (Designer)
- Kéo thành phần **WebViewer** từ nhóm **User Interface** thả vào màn hình.
- Thiết lập thuộc tính **Width** và **Height** của WebViewer thành **Fill Parent** để nó tràn toàn bộ màn hình điện thoại.  
- Tại ô thuộc tính **HomeUrl**, dán một đường link trang web có hỗ trợ giao diện điện thoại (Responsive), ví dụ:  
  - `https://m.wikipedia.org`  
  - hoặc một trang tin tức bản di động.
<img width="1914" height="924" alt="Screenshot 2026-06-09 210012" src="https://github.com/user-attachments/assets/96de2e19-9f04-437f-b64b-bd620d8312f2" />

---

## Khối lệnh (Blocks)
- Phần này thực chất **không cần kéo block nào** vì thuộc tính **HomeUrl** đã được cài đặt sẵn ở phần giao diện.
<img width="1908" height="918" alt="20" src="https://github.com/user-attachments/assets/f657aeb1-370c-48b8-ae69-08378ecf579d" />

- Trang web sẽ tự động tải lên ngay khi mở màn hình này.

  <img width="1914" height="924" alt="17" src="https://github.com/user-attachments/assets/5d408a32-963d-45e6-9f69-1116f16fc6c7" />


## 3. Đánh Giá Bản Chất Công Cụ Lập Trình Trực Quan

#### a. Bản chất của việc kéo thả block
Kéo thả block trong MIT App Inventor thực chất là hình thức **Lập trình trực quan (Visual Programming)**. Đằng sau giao diện các khối hình học màu sắc là những đoạn mã nguồn (thường là Java hoặc JavaScript) đã được định nghĩa và đóng gói sẵn theo tiêu chuẩn. Việc ghép nối các block tương đương với việc thiết lập logic luồng chạy cho chương trình, hệ thống sẽ tự động biên dịch các mối nối này thành mã máy hoàn chỉnh.

#### b. Ưu điểm và Nhược điểm so với viết code truyền thống
* **Ưu điểm:**
  * **Tốc độ và sự tiếp cận:** Rút ngắn thời gian phát triển ứng dụng, cực kỳ trực quan, dễ học, phù hợp để làm nhanh các bản mẫu thử nghiệm (Prototype).
  * **Loại bỏ lỗi cú pháp:** Hoàn toàn không xảy ra lỗi cú pháp (Syntax errors) kinh điển như thiếu dấu chấm phẩy `;`, đặt sai tên từ khóa, hay quên đóng ngoặc nhọn `{}`.
* **Nhược điểm:**
  * **Hạn chế hiệu năng & tính linh hoạt:** Khó can thiệp sâu vào hệ thống, không tối ưu được tài nguyên thiết bị khi xử lý các thuật toán hoặc cấu trúc dữ liệu quy mô lớn và phức tạp.
  * **Khó quản lý mã nguồn:** Khi project mở rộng, màn hình chứa các khối lệnh (Blocks) sẽ trở nên cực kỳ dày đặc, rối mắt, gây khó khăn cho việc bảo trì, đọc lại logic và làm việc nhóm.

#### c. Tính năng sao chép khối lệnh bằng Backpack (Chiếc ba lô)
* **Bản chất:** **Backpack** là một vùng lưu trữ tạm thời (Clipboard) chuyên dụng của MIT App Inventor, hiển thị bằng biểu tượng chiếc ba lô ở góc trên bên phải màn hình Blocks.
* **Cách sử dụng & Ý nghĩa:** Người dùng có thể kéo một khối hoặc một cụm khối lệnh logic thả vào Backpack để lưu trữ (Copy). Khi di chuyển sang một Screen khác trong cùng dự án, chỉ cần mở Backpack và kéo cụm khối đó ra màn hình làm việc (Paste). Tính năng này giúp tái sử dụng mã nguồn nhanh chóng, giảm thiểu tối đa thời gian xây dựng lại các khối lệnh có chung logic (như các nút bấm quay lại màn hình cũ).



