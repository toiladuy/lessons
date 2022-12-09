# HTML

## Nội dung
1. [Cấu trúc 1 trang HTML chuẩn](#cấu-trúc-1-trang-html-chuẩn)
2. [Cấu tạo của 1 thẻ (element)](#cấu-tạo-của-1-thẻ-element)
3. [Các thẻ HTML thường gặp](#các-thẻ-thường-gặp)
4. [Các thuộc tính thường gặp](#các-thuộc-tính-thường-gặp)
5. [Đường dẫn (Path)](#đường-dẫn-đến-nội-dung-path)
6. [HTML Forms](#html-forms)
7. [Các nội dung nâng cao có thể tìm hiểu thêm](#các-nội-dung-nâng-cao-có-thể-tìm-hiểu-thêm)

### Cấu trúc 1 trang HTML chuẩn
- Khai báo `<!DOCTYPE html>`
- Thẻ `<html></html>`
- Thẻ `<head></head>`
- Thẻ `<body></body>`

```html
<!DOCTYPE html>
<html>

<head>
  <title>Page Title</title>
</head>

<body>
  <p>Nội dung trang web đặt trong thẻ body</p>
</body>

</html>
```

### Cấu tạo của 1 thẻ (element)
Thẻ HTML bất kỳ bao gồm 3 phần:

1. Tên thẻ (element). Ví dụ: `<p>`, `<h1>`
2. Các thuộc tính của thẻ (attribute). Có 2 loại:
    - Thuộc tính hệ thống (Built-in attributes)
    - Thuộc tính data (`data-*` attributes) cho phép người dùng đặt bất kỳ.
3. Nội dung thẻ (body)
    - Có thể chứa các thẻ con.
    - Nội dung sẽ **tự động xóa các dấu khoảng trắng liên tục hơn 1 và xuống hàng khi nhập**.

Ví dụ:
```html
<div id="ma_dinh_danh" class="ten_the" data-page="1">
    <h3>Title</h3>
    <p>Body</p>
</div>
```


### Các thẻ thường gặp

```html
<!-- Thẻ Heading: từ <h1> đến <h6> -->
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
...
<h6>This is heading 6</h6>

<!-- Thẻ Paragraph: <p> -->
<p>This is a paragraph.</p>

<!-- Thẻ Link: <a>, dùng target="_blank" khi nhấn vào link mở tab mới -->
<a href="https://www.w3schools.com" target="_blank">This is a link</a>

<!-- Thẻ Image: <img>, alt là nội dung hiển thị khi ảnh ko load được -->
<img src="https://picsum.photos/seed/picsum/200/300" alt="hinh_bi_loi_rui">

<!-- Thẻ Xuống hàng: <br> -->
<br>

<!-- Thẻ div: <div> hoặc <span>, thẻ ko mang ý nghĩa gì, được dùng khi ko biết dùng thẻ gì khác -->
<div>Thẻ div cho cả đoạn text</div>
<span>Thẻ span cho 1 đoạn inline text</span>

<!-- Bôi đậm: <b> hoặc <strong>, thường dùng <b> hơn -->
<b>Dòng này sẽ được đôi đậm</b>
<strong>Dòng này sẽ được đôi đậm</strong>

<!-- In nghiêng: <i> hoặc <em>, thường dùng <i> hơn -->
<i>Dòng này sẽ được in nghiêng</i>
<strong>Dòng này sẽ được in nghiêng</strong>

<!-- Đường gạch ngang: <hr> -->
<hr>

<!-- 
    Thẻ Định dạng sẵn: <pre>, nội dung trong thẻ sẽ 
    giữ nguyên khoảng cách và xuống dòng trong nội dung.
-->
<pre>
    Hello,

Câu này lúc hiển thị sẽ vẫn giữ khoảng trắng và xuống hàng.


  Dòng này được xuống hàng 2 lần và chỉ thụt đầu dòng 1 ít.
</pre>

<!-- Table -->
<table>
    <thead>
        <tr>
            <th>Tên cột 1</th>
            <th>Tên cột 2</th>
            <th>Tên cột 3</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Giá trị cột 1</td>
            <td>Giá trị cột 2</td>
            <td>Giá trị cột 3</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>Footer 1</td>
            <td>Footer 2</td>
            <td>Footer 3</td>
        </tr>
    </tfoot>
</table>

<!-- Thẻ Unordered List: dùng hiển thị danh sách với gạch đầu dòng -->
<ul>
    <li>
        <p>Hello</p>
        Có thể để bất cứ gì trong này
    </li>

    <li></li>
</ul>

<!-- Thẻ Ordered List: dùng hiển thị danh sách có số thứ tự 1., 2., ... -->
<ol>
    <li>
        <p>Hello</p>
        Có thể để bất cứ gì trong này
    </li>

    <li></li>
</ol>
```


### Các thuộc tính thường gặp

```html

<!-- id: mã định danh thẻ, nên đặt duy nhất trong cả trang -->
<div id="ma_dinh_danh"></div>

<!-- class: phân loại cho thẻ, có thể dùng nhiều class cách nhau khoảng trắng -->
<div class="card group"></div>

<!-- name: tên của biến được gửi lên server khi dùng trong thẻ Form -->
<div name="form_field_name"></div>

<!-- style: định dạng cho thẻ như css, dùng khi lười hoặc định dạng đơn giản -->
<div style="color:blue"></div>

<!-- data-*: thẻ tùy biến cho người dùng -->
<div data-page-index="1" data-count="10" data-created-at="2022-12-07">
    Thẻ với nhiều loại data-
</div>
```

### Đường dẫn đến nội dung (Path)
Có 2 loại đường dẫn (path):
1. Absolute path (Đường dẫn tuyệt đối):
    - Là đường dẫn đầy đủ đến tài nguyên (trang web, hình, tập tin).
    - Có thể dùng để mở tập tin ở bất kỳ đâu.

2. Relative path (Đường dẫn tương đối):
    - Là đường dẫn tính từ nơi đang gọi trở đi
    - Không thể dùng để mở tập tin ở nơi khác.
    - Luôn ưu tiên dùng Relative Path.
    - Đường dẫn tương đối bắt đầu bằng 1 trong 3 cách:
        - Đường dẫn tính từ root folder trở vào trong thư mục con. Bắt đầu bằng `/`.
        - Đường dẫn tính từ vị trí của nơi dùng trở vào trong thư mục con. Bắt đầu bằng `./` hoặc ko có gì.
        - Đường dẫn tính từ vị trí của nơi dùng trở ra ngoài thư mục cha. Bắt đầu bằng `../`.

Ví dụ: Folder của source code là:
```
src
    images
        thumbnails
            thumb-1.png
            thumb-2.png
        products
            product-1.png
            product-2.png
        logo.png
    admin
        icons
            ic-1.ico
            ic-2.ico
        admin.html
    index.html
```

Giả sử server chạy ở `localhost:8080` và folder chạy (root folder) là `src`.

Nội dung file `src/index.html` như sau:
```html
<!DOCTYPE html>
<html>
<body>
    <!-- 
    Đây là Absolute Path, ko fai /src/images/logo.png 
    vì root folder đang là src.
    -->
    <image src="http://localhost:8080/images/logo.png" />

    <!-- 
    Đây là Relative Path 1, đường dẫn sẽ tính từ root folder.
    -->
    <image src="/images/logo.png" />

    <!-- 
    Đây là Relative Path 2, đường dẫn sẽ tính từ vị trí
    của file index.html và tính vào thư mục con.
    -->
    <image src="./images/logo.png" />
    <!-- 
    Đây là Relative Path 2, tương tự trên, ko có gì ở đầu đường dẫn.
    -->
    <image src="images/logo.png" />
</body>

</html>
```

Nội dung file `src/admin/admin.html` như sau:
```html
<!DOCTYPE html>
<html>
<body>
    <!-- 
    Đây là Relative Path 3, đường dẫn sẽ tính từ vị trí
    của file admin/admin.html và tính trở ra thư mục cha.
    -->
    <image src="../images/logo.png" />
</body>

</html>
```

### HTML Forms
Cấu tạo của form gồm:
- Các thẻ nhập liệu (Input elements)
- Các thẻ hiển thị nội dung (thẻ bất kỳ)
- Các nút bấm (Button)

```html
<form method="post" action="/dang-ky-ban-tin.aspx" target="_blank">
    <label for="un">Nhập username:</label>
    <input id="un" type="text" name="username">

    <p>Chọn nội dung muốn gửi thông báo:</p>

    <input id="hot" type="checkbox" name="hot" value="Hot">
    <label for="hot">Tin nóng</label>

    <input id="eco" type="checkbox" name="economy" value="Economy">
    <label for="eco">Tài chính</label>

    <input id="tech" type="checkbox" name="tech" value="Technology">
    <label for="tech">Công nghệ</label>

    <p>Chọn thời gian cập nhật:</p>

    <input id="daily" type="radio" name="daily" value="Daily">
    <label for="hot">Hàng ngày</label>

    <input id="weekly" type="radio" name="weekly" value="Weekly">
    <label for="eco">Hàng tuần</label>

    <input id="monthly" type="radio" name="monthly" value="Monthly">
    <label for="tech">Hàng tháng</label>

    <input type="submit" value="Submit">
</form>
```

### Các nội dung nâng cao có thể tìm hiểu thêm
- HTML responsive với:
    + Viewport meta trong thẻ Head
    + Sử dụng Viewport width & height (vh, vw)
    + Flexbox, Float, Grid
    + Sử dụng thẻ `<picture>` cho việc hiển thị các hình khác nhau theo kích thước màn hình
    + Sử dụng media queries `@media` to apply CSS tương ứng
    + Một số thẻ dùng định dạng nội dung kiểu code như `<code>`, `<pre>`, `<kbd>`, `<samp>`, `<var>`.
