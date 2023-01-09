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
PS C:\ssh_github_key> ssh-keygen -t rsa -f id_rsa
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

