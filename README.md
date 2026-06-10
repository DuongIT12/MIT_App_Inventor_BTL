<img width="784" height="457" alt="image" src="https://github.com/user-attachments/assets/2ecbb1fc-ec0c-474c-99e5-469ed3968e7d" /># MIT_App_Inventor_BTL
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


# 2. VIẾT APP SỬ DỤNG ANDROID STUDIO

## File AndroidManifest.xml và cơ chế xin quyền
### a. File AndroidManifest.xml mô tả gì?

**AndroidManifest.xml** là file cấu hình cốt lõi và bắt buộc phải có của mọi ứng dụng Android.  
Nó đóng vai trò là cầu nối thông tin giữa ứng dụng của bạn và Hệ điều hành Android (OS) cùng Google Play.  

File này mô tả:

- **Cấu trúc ứng dụng:**  
  Khai báo toàn bộ các thành phần cấu thành nên app (bao gồm các màn hình *Activity*, các dịch vụ chạy ngầm *Service*, bộ nhận sự kiện hệ thống *Broadcast Receiver*, và bộ quản lý dữ liệu *Content Provider*).  
  Nếu một *Activity* không được khai báo tại đây, hệ thống sẽ không cho phép khởi chạy nó.

- **Thông tin định danh:**  
  Tên gói ứng dụng (*package*), biểu tượng (*icon*), tên hiển thị (*label*), và giao diện chủ đạo (*theme*).

- **Yêu cầu hệ thống:**  
  Các cấu hình phần cứng tối thiểu để app chạy được (như phiên bản Android SDK thấp nhất, cấu hình camera, cảm biến).

- **Cơ chế an toàn:**  
  Khai báo các quyền truy cập tài nguyên phần cứng hoặc phần mềm hệ thống.

### b. Khi ứng dụng cần quyền (Permission), khai báo như thế nào? Để làm gì?

- **Cách khai báo:**  
  Bạn sử dụng thẻ `<uses-permission>` đặt nằm phía ngoài thẻ `<application>` và nằm trong thẻ cấu hình gốc `<manifest>`.

- **Ví dụ cụ thể khi cần quyền truy cập Internet và quyền đọc bộ nhớ máy:**

```xml
<manifest xmlns:android="http://schemas.android.com/apk/config/android" package=...>
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
    <application ...>
        ...
    </application>
</manifest>
```

## 2. VÒNG ĐỜI CỦA ỨNG DỤNG ANDROID VÀ HÀM onCreate

### Vòng đời ứng dụng Android (Activity Lifecycle) là gì?

Một màn hình (Activity) trong Android không chỉ đơn thuần là mở lên và đóng lại, mà nó chịu sự quản lý nghiêm ngặt của Hệ điều hành thông qua một vòng tuần hoàn các trạng thái.  
Hệ điều hành cung cấp các hàm phản hồi (Callback) để ứng dụng tự xử lý dữ liệu khi trạng thái thay đổi:

- **onCreate()**: Kích hoạt khi Activity bắt đầu được khởi tạo trong bộ nhớ.  
- **onStart()**: Màn hình bắt đầu xuất hiện trước mắt người dùng nhưng chưa tương tác được.  
- **onResume()**: Ứng dụng chạy ở tiền cảnh (foreground), người dùng bắt đầu tương tác trực tiếp (gõ phím, bấm nút).  
- **onPause()**: Ứng dụng bị mất tập trung một phần (ví dụ có một hộp thoại thông báo/báo thức đè lên một phần màn hình).  
- **onStop()**: Màn hình bị che khuất hoàn toàn (người dùng bấm nút Home ra ngoài hoặc chuyển hẳn sang app khác).  
- **onDestroy()**: Ứng dụng bị giải phóng hoàn toàn khỏi bộ nhớ (người dùng vuốt tắt app hoặc bấm nút Back thoát hẳn).



### Tại sao code tự sinh sau khi tạo dự án luôn có sẵn hàm onCreate?
- Hàm onCreate() là điểm bắt đầu bắt buộc (Entry Point) của một màn hình. Hệ điều hành Android quy định rằng khi khởi chạy một Activity, việc xây dựng cấu trúc nền tảng phải được làm tại đây.
Vì vậy, Android Studio tự động sinh ra hàm này để lập trình viên thực hiện 3 nhiệm vụ sống còn:


## Hàm onCreate() trong Android

Khi tạo dự án mới trong Android Studio, mã nguồn tự sinh luôn có sẵn hàm **onCreate()**, vì đây là điểm bắt đầu bắt buộc của một màn hình (*Activity*).

Ba nhiệm vụ chính của hàm này:

1. Gọi **super.onCreate(savedInstanceState)** để hệ thống thiết lập lại trạng thái cũ của màn hình (nếu có).  
2. Liên kết mã nguồn Java với file giao diện XML bằng hàm **setContentView(R.layout.activity_main)**.  
3. Khởi tạo các biến toàn cục, cấu hình các bộ lắng nghe sự kiện, hoặc ánh xạ các View (bằng **findViewById**) để ứng dụng sẵn sàng hoạt động.  

Nếu thiếu hàm **onCreate()**, màn hình sẽ trống rỗng và không thể kích hoạt các trạng thái tiếp theo trong vòng đời ứng dụng.


## 3. KIỂM TRA QUYỀN ĐỘNG TRONG CODE JAVA

### Kiểm tra quyền và ý nghĩa

Từ phiên bản Android 6.0 (API 23) trở đi, ngoài việc khai báo trong file Manifest, ứng dụng bắt buộc phải xin quyền trực tiếp từ người dùng tại thời điểm app đang chạy (Runtime Permission) đối với các quyền nguy hiểm (đọc bộ nhớ, camera, vị trí).

### Ví dụ kiểm tra quyền đọc bộ nhớ:

```java
// Kiểm tra xem ứng dụng đã được cấp quyền đọc bộ nhớ chưa
if (ContextCompat.checkSelfPermission(this, Manifest.permission.READ_EXTERNAL_STORAGE)
        != PackageManager.PERMISSION_GRANTED) {

    // Ý nghĩa: Nếu CHƯA ĐƯỢC CẤP QUYỀN -> tiến hành hiển thị hộp thoại hệ thống yêu cầu quyền
    ActivityCompat.requestPermissions(this,
            new String[]{Manifest.permission.READ_EXTERNAL_STORAGE}, 101);
} else {
    // Ý nghĩa: Nếu ĐÃ ĐƯỢC CẤP QUYỀN -> thực thi công việc tương ứng ngay lập tức
    docDuLieuTuAssets();
}
```
### Ý nghĩa của việc kiểm tra:
- Tránh việc ứng dụng bị hệ điều hành tắt đột ngột (Crash app) do vi phạm chính sách bảo mật khi cố tình truy cập tài nguyên hệ thống mà không có sự đồng ý của người dùng.
   - Đảm bảo tính linh hoạt: Người dùng có thể thu hồi quyền trong phần cài đặt thiết bị bất cứ lúc nào, việc check quyền liên tục giúp ứng dụng luôn biết trạng thái chính xác để xử lý kịch bản lỗi mượt mà.
 
## TỐI ƯU GIAO DIỆN XML VÀ CƠ CHẾ THAM CHIẾU (TRÁNH HARDCODE)
Cú pháp của việc tham chiếu là gì?  
- Khi thiết kế giao diện, thay vì viết chữ trực tiếp vào file XML (android:text="Nguyễn Thế Dương" - gọi là Hardcode) , bạn cần đưa chuỗi văn bản đó vào file tài nguyên tập trung tại thư mục res/values/strings.xml.

#### Khai báo và tham chiếu String Resource trong Android

- **Cú pháp khai báo trong `strings.xml`:**
```xml
<string name="txt_username">Nguyễn Thế Dương</string>
```
- Cú pháp tham chiếu trong file giao diện XML:    
Ngôn ngữ XML sử dụng ký tự @ để đại diện cho việc gọi tài nguyên hệ thống.  
```android:text="@string/txt_username"```  
  
- Cú pháp tham chiếu trong file xử lý Java:  
Ngôn ngữ Java sử dụng lớp đối tượng cấu trúc R (Resource) được biên dịch tự động làm đầu mối truy cập.
```textView.setText(R.string.txt_username)```  

### Ưu điểm của việc tham chiếu này?

- **Quản lý tập trung:**  
  Khi muốn thay đổi một câu chữ được dùng ở 10 màn hình khác nhau, bạn chỉ cần chỉnh sửa đúng 1 dòng duy nhất trong file `strings.xml` thay vì phải đi tìm mọi từng file giao diện.  

- **Tách biệt logic và giao diện:**  
  Giúp lập trình viên tập trung thiết kế cấu trúc bố cục, còn đội ngũ biên dịch nội dung hoặc thiết kế nội dung làm việc độc lập trên file cấu hình text.  

---

### OS hỗ trợ tự động lấy giá trị theo LOCATION, LANGUAGE, THEME giúp app làm được điều gì?

Việc hỗ trợ tự động (**Auto-resource resolution**) này giúp ứng dụng đạt được khả năng **Bản địa hóa (Localization)** và **Tương thích giao diện linh hoạt** mà không cần lập trình viên phải viết thêm bất kỳ dòng code logic `if/else` phức tạp nào để kiểm tra cấu hình máy của người dùng.  

Cụ thể, hệ điều hành Android hoạt động dựa trên cơ chế đặt tên thư mục tài nguyên theo hậu tố quy chuẩn:

- **LANGUAGE & LOCATION:**  
  Nếu người dùng cài đặt máy điện thoại là tiếng Anh, OS tự động quét và lấy chữ trong thư mục `res/values-en/strings.xml`.  
  Nếu người dùng đổi máy sang tiếng Việt, OS tự chọn thư mục `res/values-vi/strings.xml`.  

- **THEME:**  
  Khi người dùng bật chế độ nền tối (Dark Mode), hệ thống tự động ánh xạ cấu hình màu sắc trong thư mục `res/values-night/themes.xml` thay vì thư mục `values` thông thường.

## Tránh hardcode chuỗi trong code Java

Lập trình viên không nên gán trực tiếp chuỗi như:
```java
textView.setText("Chào bạn");
```
- Trong code Java tuyệt đối không gán chuỗi trực tiếp kiểu textView.setText("Chào bạn"). Thay vào đó, bạn phải gán thông qua ID tham chiếu tài nguyên R.string để hệ thống tự động bóc tách ngôn ngữ và vị trí của máy người dùng
```
TextView tvWelcome = findViewById(R.id.tv_welcome);

// Cách làm đúng: Gọi trực tiếp ID tài nguyên, Android OS sẽ tự chọn ngôn ngữ phù hợp để hiển thị
tvWelcome.setText(R.string.welcome_message);
```

## 5. ĐỐI TƯỢNG CHỨA (VIEWGROUP) SẮP XẾP LINH HOẠT

### LinearLayout và các quy luật sắp xếp

Để gộp các đối tượng con (Button, TextView, EditText) nằm kề nhau theo một quy luật sắp xếp nhất định, Android sử dụng đối tượng chứa là `LinearLayout`.

- **Sắp xếp theo chiều dọc (Vertical):**  
  Các đối tượng con xếp chồng lên nhau từ trên xuống dưới, giống cấu trúc một cột dữ liệu.

**XML**
```xml
android:orientation="vertical"
```
- Sắp xếp theo chiều ngang (Horizontal):  
Các đối tượng con nằm dàn hàng ngang liên tiếp nhau từ trái qua phải.
```
android:orientation="horizontal"
```

- Thuộc tính gravity:  
Định nghĩa quy luật dồn và căn chỉnh vị trí của các đối tượng con hoặc nội dung bên trong vùng chứa.
Ví dụ: android:gravity="center" sẽ kéo toàn bộ các nút bấm và chữ đặt vào vị trí chính giữa trung tâm của layout.


## 6. XỬ LÝ SỰ KIỆN NGƯỜI DÙNG (EVENT CLICK)

Khi người dùng bấm vào một đối tượng, một đoạn code sẽ được chạy.  
Việc này cần sự phối hợp giữa cấu hình giao diện (layout XML) và code xử lý.

Trong file layout XML, các đối tượng có khả năng tương tác (ví dụ: Button) phải khai báo thuộc tính để hệ thống nhận diện.

Có 2 cách viết code, cách thứ nhất là khai báo trực tiếp bằng thuộc tính `android:onClick` trong XML.

### Ví dụ:

```xml
<Button
    android:id="@+id/btn_submit"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:onClick="xuLyKhiNguoiDungClick"
    android:text="Gửi dữ liệu" /> ```

- Trong code Java, bạn cần tạo một hàm có tên trùng khớp với tên đã khai báo trong XML.  
Hàm này phải có dạng **public**, trả về **void**, và nhận một tham số duy nhất kiểu **View**.

### Ví dụ:

```java
public void xuLyKhiNguoiDungClick(View view) {
    // Đoạn code xử lý tính toán hoặc chuyển màn hình nằm ở đây
    Toast.makeText(this, "Bạn đã bấm nút bằng Cách 1!", Toast.LENGTH_SHORT).show();
}
```

## Cách 2: Sử dụng bộ lắng nghe sự kiện bằng mã lệnh Java (Chuẩn hóa cấu trúc công nghiệp)

Đây là cách thường dùng trong các dự án thực tế vì giúp file giao diện XML thuần khiết, không bị pha trộn logic code.

Trong file layout XML, không cần khai báo thuộc tính `onClick`, chỉ cần đặt **ID** rõ ràng cho Button.

### Ví dụ XML:

```xml
<Button
    android:id="@+id/btn_submit"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Gửi dữ liệu" />
```
- Tại Code Java: Thực hiện ánh xạ view bằng ID, sau đó gán bộ lắng nghe sự kiện setOnClickListener ẩn danh.
  
  ## Java

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    // 1. Ánh xạ nút bấm từ XML sang Java
    Button btnSubmit = findViewById(R.id.btn_submit);

    // 2. Thiết lập bộ lắng nghe sự kiện click
    btnSubmit.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            // Đoạn code xử lý logic nằm ở đây
            Toast.makeText(MainActivity.this, "Bạn đã bấm nút bằng Cách 2!", Toast.LENGTH_SHORT).show();
        }
    });
}
```

## 7. LÀM VIỆC VỚI THƯ MỤC ĐẶC BIỆT Assets

Thư mục `assets` là kho lưu trữ các file tài nguyên thô (Raw files) đi kèm ứng dụng.  
Khi bạn dùng Windows Explorer copy tài nguyên vào đây, lúc biên dịch (compile), hệ thống sẽ đóng gói toàn bộ cấu trúc file này vào tệp cài đặt gốc của ứng dụng.

---

### a. Cú pháp truy cập vào thư mục `Assets` bằng Java

Android cung cấp đối tượng chuyên dụng là **AssetManager** để quản lý mở luồng đọc file.  

- **Cú pháp mở một file text tên là `huongdan.txt` nằm trong Assets:**

```java
AssetManager assetManager = getAssets();
InputStream is = assetManager.open("huongdan.txt");
```
### b. Lợi ích của việc ứng dụng có sẵn các file offline này là gì?
- **Hoạt động không phụ thuộc mạng:**  
  Người dùng có thể sử dụng toàn bộ chức năng cốt lõi của app (đọc cẩm nang, xem hướng dẫn, tra cứu dữ liệu) ở bất cứ đâu, kể cả vùng sâu vùng xa, máy bay hay khi mất kết nối mạng internet.  

- **Tốc độ phản hồi cực nhanh:**  
  Dữ liệu nằm ngay trên bộ nhớ cục bộ của điện thoại, không mất thời gian chờ đợi tải (loading) dữ liệu từ máy chủ (Server) qua internet, giảm thiểu tối đa độ trễ UI.  

- **Tiết kiệm băng thông và chi phí vận hành:**  
  Tiết kiệm dung lượng mạng di động (3G/4G/5G) cho người dùng, đồng thời giảm tải băng thông và chi phí duy trì máy chủ cho nhà phát triển.

## c. Ứng dụng thực tế: App hướng dẫn việc 

Dựa theo gợi ý sáng tạo, bạn có thể xây dựng **“Ứng dụng Hướng dẫn quy trình cài đặt và cấu hình Hệ điều hành Linux Ubuntu”** hoặc **“Cẩm nang hướng dẫn chăm sóc mèo cưng”**.

- **Đặc thù dữ liệu:**  
  Dữ liệu văn bản được chuẩn bị sẵn dưới dạng file định dạng cấu trúc mở rộng `.json` đặt tên là `data_huongdan.json` nằm trong mục Assets.  
  Cấu trúc bao gồm các thẻ: `id`, bước thực hiện, tiêu đề, nội dung chi tiết, và tên ảnh minh họa đi kèm.

- **Thuật toán xử lý:**  
  Khi app khởi chạy, hàm `onCreate()` kích hoạt luồng đọc file thô từ thư mục Assets, sau đó sử dụng thư viện xử lý chuỗi Json (như `JSONObject`) để bóc tách cấu hình mảng dữ liệu (*Parse data*).

- **Đối tượng hiển thị giao diện:**  
  Dữ liệu sau khi xử lý phân tách sẽ được nạp vào một danh sách và hiển thị giao diện danh mục qua đối tượng `RecyclerView` hoặc `ListView`, kết hợp với thành phần hiển thị chữ `TextView` và hiển thị ảnh đồ họa `ImageView`.

---


















