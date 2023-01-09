# Hướng dẫn truy cập GITHUB qua SSH Key

> Để truy cập cũng như đẩy code từ xa, chúng ta thiết lập kết nối git local với github.com thông qua ssh key

1. Tạo SSH Key
### Trên máy tinh Window, Linux ta tạo một ssh key, tạo 1 folder để lưu thông tin ssh key c:\ssh_github_key

```diff
cd c:\ssh_github_key
ssh-keygen -t rsa -f id_rsa
```