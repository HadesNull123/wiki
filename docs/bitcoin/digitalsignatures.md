
# Chữ ký số

Một con số được tạo ra từ private key chứng minh rằng bạn sở hữu public key

## Chữ ký số là gì?

Chữ ký số là một con số có kết nối, liên hệ toán học với publickey, mà bạn có thể dùng để chứng minh rằng mình biết private key mà không cần phải cho người khác xem private key

H1

Nếu ai đó từng hỏi bạn rằng bạn có private key cho một địa chỉ hay public key nào đó không thì bạn có thể đưa chữ ký số ra để chứng minh là quyền sở hữu của mình

> Bạn cần phải thực hiện một chút công việc tính toán số học để chứng minh rằng chữ ký số có liên kết toán học đối với public key

# **Tại sao chúng ta sử dụng chữ ký số trong bitcoin?**

Bởi vì khi bạn tạo ra một transaction thì bạn cần unlock các output để sử dụng. Điều này có thể thực hiện được bằng cách chứng minh bạn sở hữu output. Và bạn làm điều đó bằng cách chứng tỏ rằng bạn biết private key của các output được khóa 

H2

Nhưng nếu bạn đưa private key của mình vào dữ liệu transaction thì mọi người trên network đều có thể nhìn thấy nó

H3

Nếu mọi người có private key của bạn thì họ có thể dùng nó để unlock các output đang bị lock và gửi nó đi từ địa chỉ bitcoin của bạn, tất nhiên như thế bạn sẽ bị mất tiền.

Vậy làm thế nào để unlock các output mà không cần đưa private key ra?

# **Hãy nhập vào chữ ký số**

Một chữ ký số được dùng để unlock các output, bởi vì nó chứng tỏ rằng chúng ta biết private key của một địa chỉ.

Điều tuyệt vời nhất là chúng ta có thể dùng chữ ký số mà không làm lộ private key ra ngoài network.

H4

# Điều gì ngăn chặn người khác dùng chữ ký số để unlock các output tại địa chỉ ví bitcoin của bạn?

Như chúng ta đã biết thì có thể dùng private key để unlock các output trong 1 địa chỉ vậy thì tại sao chúng ta không thể làm được điều tương tự nếu dùng chữ ký số?

> Câu trả lời là: Bởi vì mỗi chữ ký số là duy nhất đối với một transaction. Điều này có nghĩa là tương ứng với mỗi transaction thì chỉ có một chữ ký số duy nhất mà thôi.

Nói cách khác thì chúng ta không chỉ sử dụng mỗi private key để tạo một chữ ký số, mà chúng ta đồng thời sử dụng cả private key lẫn dữ liệu của chính bản thân transaction để làm đầu vào tạo ra chữ ký số

H5

Do đó mỗi chữ ký số sẽ được ràng buộc với transaction mà nó được sử dụng trong đó.

H6

Nếu ai đó sử dụng chữ ký số này để trong một transaction khác thì nó sẽ bị xung đột với các dữ liệu về transaction đó. Các node mạng network sẽ không chấp nhận transaction này.

H7

Và kết quả là chữ ký số cũng bảo vệ giao dịch mà nó được sử dụng, cơ chế này chống lại bất cứ ai can thiệp vào transaction có chữ ký số đó.

# Làm thế nào để chữ ký số hoạt động?

Chữ ký số hoạt động được là nhờ toán học.

1\. Chúng ta sử dụng kết hợp cả private key và dữ liệu của transaction ( `private key`\+`transaction data)` , bằng biến đổi toán học chúng ta sẽ tạo ra được chữ ký số.

2\. Chúng ta sử dụng bộ dữ liệu ( *digital signature*\+`transaction data`\+`public key  )`và  cũng bằng những biến đổi toán học chúng ta cũng đưa ra được một kết quả private key hợp lệ đã được sử dụng để tạo ra chữ ký số.

Hãy nhớ rằng, mục đích của chữ ký số là để nhằm chứng minh rằng bạn là chủ sở hữu của public key.

Nghe thì có vẻ ảo diệu nhưng thật ra tất cả bí mật đều nằm ở các phép biến đổi toán học và chúng ta sẽ biết nó hoạt động thế nào trong phần [Chữ ký số ( Ký và xác nhận )](http://trada.tech)

# [\
](http://trada.tech)
