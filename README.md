# GitHub – Cách đưa code lên GitHub

---
- Xem mục [Các câu lệnh cơ bản Git](./git-commands.md)
- Xem mục [Các câu lệnh với GitHub](./git-commands2.md)

## Bước 1: Tạo tài khoản GitHub và download Git

Ở bước này mình để hai đường dẫn bên dưới.

- Link GitHub: https://github.com/
- Link download Git: https://git-scm.com/downloads

## Bước 2: Tạo một repository mới trên Github

Sau khi các bạn đã thực hiện bước 1 xong, các bạn đăng nhập vào GitHub và tạo một repository mới để đưa code lên GitHub. Các bạn thực hiện giống như ảnh bên dưới:

![repository](./images/001.png 'repository')

Sau đó các bạn nhấn `Create repository`

Sau khi các bạn chọn `Create repository` thì sẽ được như hình bên dưới đây:

![repository](./images/002.png 'repository')

## Bước 3: Đưa code lên GitHub

Để đẩy source code lên repository trên GitHub, bạn có thể sử dụng các câu lệnh Git cơ bản sau:

Khởi tạo Git trong thư mục dự án (nếu chưa có):
```cmd
git init
```
Thêm các tệp vào staging area:

```cmd
git add .
```
Commit các tệp với một thông điệp:

```cmd
git commit -m "Initial commit"
```
Thêm remote repository:
```cmd
git remote add origin <URL của repository>
```
Đẩy code lên repository:
```cmd
git push -u origin master
```
Nếu bạn cần thêm thông tin chi tiết hoặc gặp vấn đề gì, cứ cho mình biết nhé! 😊

## Bước 3: Đưa code lên GitHub

Đầu tiên các bạn mở `VSCode` lên vào thư mục mà bạn muốn đưa code lên `GitHub`. Các bạn vào `Terminal` chọn `New Terminal`

![code lên GitHub](./images/003.png 'code lên GitHub')

Tiếp theo bạn gõ `git init` để khởi tạo 1 git repository 1 project mới hoặc đã có (nếu bước này các bạn bị lỗi thì các bạn chưa download Git về hoặc cài đặt chưa thành công)
> git init

![code lên GitHub](./images/004.png 'code lên GitHub')

Sau đó ta gõ `git status` để check những file chưa được đưa lên hoặc đã thay đổi trong thư mục
> git status

![code lên GitHub](./images/005.png 'code lên GitHub')

Ở đây mình có tất cã 7 File

![code lên GitHub](./images/006.png 'code lên GitHub')

Tiếp theo ta add những file cần đưa lên github ta dùng `git add`
> git add *

![git add](./images/007.png 'git add')

Để kiểm tra mình đã add thành công hay chưa các bạn gõ `git status` lại để check

![git add](./images/008.png 'git add')

Tất cã các file đã được add thành công

Tiếp theo các bạn gõ lệnh `git commit -m “Add new project manu”` . Lệnh này dùng để note lại các thay đổi để dễ dàng theo dõi nhe.
> git commit -m “Add new project manu”

![git add](./images/009.png 'git add')

Kế tiếp các bạn gõ lệnh `git branch -M main`

> git branch -M main

![git add](./images/010.png 'git add')

Sau đó các bạn gõ lệnh git remote add origin https://github.com/nguyenhuudongkhanh/manut.git (lưu ý đừng link là trên trang `Github` lúc đầu các bạn tạo `repository` không phải đừng link trong bài viết này)

![git add](./images/011.png 'git add')

Cuối cùng các bạn gõ lệnh git `push -u origin main` để đưa code lên Github

> push -u origin main

![git add](./images/012.png 'git add')

Các bạn `reload` lại trang `Github` để kiểm tra code đã được đưa lên chưa

![git add](./images/013.png 'git add')

Như vậy, quá trình đẩy code lên `gitHub` đã thành công.Chúc các bạn có thể làm được!!!

----------------------------------------------------------------


**Hướng dẫn khắc pục lỗi Updates were rejected because the tip of your current branch is behind**

## Cách 1: 
> git push -f origin master
## Cách 2:
- Thực hiện:
> git pull origin fixbug
> git push origin fixbug
- Sau đó:
> git push -f origin fixbug


**_Lưu ý:_**
- Bạn có thể buộc (force) `push local code` của mình bằng -f
- Làm điều này, nếu bạn chắc chắn rằng trạng thái commit của bạn ở nhánh local cũng sẽ được ánh xạ trong remote.
> git push -f origin master


