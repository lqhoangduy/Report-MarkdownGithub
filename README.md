# Report-MarkdownGithub
# Report GitHub
## I. Cách thức hoạt động của GitHub.
- GitHub là một hệ thống quản lý dự án và phiên bản code, hoạt động giống như một mạng xã hội cho lập trình viên
- GitHub được sử dụng chủ yếu cho dự án có nhiều người cùng hợp tác và cần giám sát toàn bộ thay đổi của dự án, cũng như để có khả năng khôi phục code khi cần thiết.
## II. Các khái niệm
- Add
> Thêm vào index (Đề xuất thay đổi).
- Remove
> Để xóa một thư mục hay một file nào đó có thể xóa ở máy local.
- Commit
> Là thao tác thông báo cho hệ thống lưu lại trạng thái hiện hành và ghi nhận lại lịch sử các xử lý file hay thư mục trên repository.
- Push
> Dùng đề đưa nội dung cập nhật repository cục bộ lên server.
- Pull
> Lấy toàn bộ dữ liệu từ repository trên server về branch hiện tại
- Fetch
> Truy cập repository trên server và kéo toàn bộ dữ liệu từ repository đó về.
- Clone
> Sao chép một repository đã tồn tại.
- Fork
> Sao chép một repository đã tồn tại, tạo ra các thay đổi cần thiết, và lưu phiên bản mới này dưới dạng một repository độc lập hoàn toàn mới. ( Tạo dự án mới trên dự án cũ)
- Star
> Là công dụ đánh dấu một project.
- Watch
> Theo dõi một repository để nhận thông báo cho các yêu cầu mới và các vấn đề được tạo mới của repository đó.

## III. Một số lệnh trong git
### 1. Setting up Git

- Tải và cài đặt git
 	- `https://git-scm.com/download/win`
	
- Thiết lập chứng thực cá nhân
    
    - `git config --global user.name "username"`
    - `git config --global user.email "email@example.com"`
    
### 2. Generate and add SSH key 
- Bước 1: Kiểm tra xem máy có SSH key chưa
	- Mở terminal và gõ câu lệnh:
	
		`ls –al ~/.ssh`
- Bước 2: Sinh một SSH key mới
	- Chạy lệnh sau trên terminal:

		`ssh–keygen –t rsa –b 4096 –C "email@example.com"`
    - Nhấn Enter để lưu key:

		`Enter file in which to save the key (/Users/binhcq/.ssh/id_rsa): [Press enter]`
	- Nhập mật khẩu cho key:
	
 		`Enter passphrase (empty for no passphrase): [Nhập mật khẩu]`
        
   		`Enter same passphrase again: [Nhập lại mật khẩu]`
    
- Bước 3: Thêm key vào ssh-agent
	-  Đảm bảo rằng ssh-agent đã được kích hoạt bằng lệnh:
	
		`eval “$(ssh-agent -s)”`
        
        `# Agent pid 59566`
        
     - Add ssh key của bạn vào ssh-agent:

		`ssh–add ~/.ssh/id_rsa`
        
- Bước 4: Thêm SSH Public key vào tài khoản trên server
	- Copy ssh key vào clipboard:

		`pbcopy < ~/.ssh/id_rsa.pub`
        
- Bước 5: Kiểm Tra

    
		`ssh -T git@github.com`
        
 ### 3. Caching -your GitHub password in Git.
 - Nếu clone repository GitHub bằng HTTPS, bạn có thể sử dụng trình trợ giúp thông tin xác thực để Git nhớ tên người dùng và mật khẩu GitHub của bạn mỗi khi nói chuyện với GitHub.
 - Nếu bạn clone repository bằng SSH, thì bạn xác thực bằng khóa SSH thay vì tên người dùng và mật khẩu. Để được trợ giúp thiết lập kết nối SSH, hãy xem Tạo Khóa SSH.
 
- Bạn cũng có thể cài đặt trình bao Git riêng, với Git cho Windows, chạy dòng sau trong dòng lệnh sẽ lưu thông tin đăng nhập của bạn:
	- `git config --global credential.helper wincred`
      
      



# Report Markdown
## I. Markdown là gì? Markdown dùng để làm gì?
-  Markdown là một ngôn ngữ đánh dấu với cú pháp văn bản thô, được thiết kế để có thể dễ dàng chuyển thành HTML.
- Nó thường được dùng để tạo các tập tin readme, viết tin nhắn trên các diễn đàn, và tạo văn bản có định dạng bằng một trình biên tập văn bản thô.
## II. Các cú pháp thường gặp.
### 1. Tạo tiên đề
- Markdown chỉ cần chèn ký tự # ngay phía trước. Số lượng ký tự # sẽ xác định độ sâu của tiêu đề (tương đương h1-h6 trong mã HTML).
- Ví dụ :
```
# Tiên đề 1
## Tiên đề 2
### Tiên đề 3
#### Tiên đề 4
##### Tiên đề 5
###### Tiên đề 6
```
# Tiên đề 1
## Tiên đề 2
### Tiên đề 3
#### Tiên đề 4
##### Tiên đề 5
###### Tiên đề 6
### 2. Định dạng chữ
```
**In đậm**
*In nghiêng*
***In đậm và in nghiêng***
~~Chữ gạch ngang~~
```
**In đậm**

*In nghiêng*

***In đậm và in nghiêng***

~~Chữ gạch ngang~~
### 3. Tạo danh sách
- Danh sách dạng số:
```
1. Danh sách 1
2. Danh sách 2
3. Danh sách 3
```
- Danh sách dạng bullet:
```
- Danh sách 1
- Danh sách 2
- Danh sách 3
```
### 4. Chèn link, Chèn ảnh
- Chèn link:
```
[Tên link](đường dẫn)
[Facebook](https://facebook.com)
```
[Facebook](https://facebook.com)

- Chèn ảnh:
```
![](đường dẫn)
![](https://~~~)
```
![](https://zicxa.com/vi/hinh-anh/wp-content/uploads/2019/07/T%E1%BB%95ng-h%E1%BB%A3p-nh%E1%BB%AFng-b%E1%BB%A9c-%E1%BA%A3nh-h%C3%A0i-h%C6%B0%E1%BB%9Bc-nh%C3%ACn-l%C3%A0-c%C6%B0%E1%BB%9Di-ngay-27.jpg)
### 5. Tạo trích dẫn (Blockquotes)
```
>Câu trích dẫn
```
>Câu trích dẫn

### 6. Tạo bảng
```
|  1 |    2 |  3   | 4    |
|----|------|------|------|
|  2 | 2  1 | 2  2 | 2  3 |
|  3 | 3  1 | 3  2 | 3  3 |
|  4 | 4  1 | 4  2 | 4  3 |
```
|  1 |    2 |  3   | 4    |
|----|------|------|------|
|  2 | 2  1 | 2  2 | 2  3 |
|  3 | 3  1 | 3  2 | 3  3 |
|  4 | 4  1 | 4  2 | 4  3 |
