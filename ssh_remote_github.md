# Hướng dẫn truy cập GITHUB qua SSH Key

> Để truy cập cũng như đẩy code từ xa, chúng ta thiết lập kết nối git local với github.com thông qua ssh key

## 1. Tạo SSH Key
#### Trên máy tinh Window, Linux ta tạo một ssh key, tạo 1 folder để lưu thông tin ssh key c:\ssh_github_key

```diff
cd c:\ssh_github_key
ssh-keygen -t rsa -f id_rsa
```
#### Khi nó hỏi Enter passphrase có thể nhấn `Enter` để trống cái này. Kết thúc lệnh đó thì trong c:\ssh_github_key sẽ có SSH Key cho bạn gồm có public key là file id_rsa.pub và private key là file: id_rsa

```diff
C:\ssh_github_key> ssh-keygen -t rsa -f id_rsa
Generating public/private rsa key pair.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in id_rsa
Your public key has been saved in id_rsa.pub
The key fingerprint is:
SHA256:Kz+kCDCYFmkdVjVKOpifcnHqwNEjpO87aFkkP4zagHU kienn@ntk
The key's randomart image is:
+---[RSA 3072]----+
| .oooo.o         |
|o+=.o . .        |
|+*.* o           |
|*+=.E            |
|oBB*    S        |
|oo*=    ..       |
|.++o...o.        |
|ooo.. .o.        |
|. ..    ..       |
+----[SHA256]-----+
PS C:\ssh_github_key>
```

## 2. Thiết lập SSH Public key trên GITHUB

#### Mở file id_rsa.pub copy toàn bộ nội dung trong file đó vào clipboad, nội dung trong đó có dạng như:

```diff
C:\ssh_github_key> cat .\id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDalDdLstgwAoxMLcG3rTiQOhHYQ7fM9eXpgP4ZJ88+KqOC2yvnQ5XGqyrL1KB1JMHpySL8GNaBcKk1eSicThj7qcX6t7fAy/eKSn+gYJqwUlPqQsRbTBDOH0rMeNkfI62zY7OLYVuUmbsWSs+OZyxvk4441XQF2MtAiYbawwlo3nQMhGPyq9ArfL6LUo1w0yH1gk8sF6QBOcCRh+yqbMSCFYA38QOFJPWjwXOklkzoqVVBlPqOPUQRH8mwu+rv951Afh5aK4I6Y84iXcwfWNJwvMyxzDLBSehA5Pq3K5bb7WdyY++4lJuU5qO0TW+JEoEmMfCySFCsmrBcyAgXceHU574PGNkulVyzJPtK6q9yjCsWs12Hb4OyuTw98f8YR0plcvTy4A0/P73y/jScCKzVIkY5VuZxJa8MhW66nq9H/IuzpWscQvdcjH6wW0/A70EGDQpuraW6LkzMTMG70b8/txbibSBibkkCZDTotchbHwrxybg/FMnExsl1Ci+0Ln0= kienn@ntk
```

#### Đăng nhập vào tài khoản `Github` truy cập vào phần `setting` 

![Alt text][img01]





[img01]: /images/01.jpg