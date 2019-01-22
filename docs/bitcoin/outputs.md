
Outputs

Là những lô ( batch ) bitcoin mới được tạo ra trong các giao dịch ( transaction )

> Hệ thống giao dịch bitcoin liên quan đến việc gửi và nhận một lô những bitcoin được gọi là OUTPUTS

 Định nghĩa là như vậy nhưng có lẽ nó vẫn còn hơi mô hồ cho nên để thực sự hiểu nó hoạt động như thế nào thì cách tốt nhất là nhìn vào ví dụ cụ thể

H1

# Giao dịch thứ nhất- Một giao dịch đơn giản

Chúng ta cùng bắt đầu với câu chuyện với việc sinh ra một lô các bitcoin mới tinh.

Giả sử bạn đang đào coin, và nhờ phép lạ nào đó mà bạn đào được 1 block và kiếm được 25 bitcoin tiền thưởng do đào được block này

H2

Mỗi miner cũng đặt địa chỉ của mình trên top của mỗi block nếu bạn đào được 1 block thì tiền thưởng ( BLOCK REWARD ) sẽ được chuyển đến tài khoản của bạn.

Đây là trạng thái tài khoản tại địa chỉ của bạn

H3

Có tiền về thì tất nhiên là phải chúc mừng rồi. Chúng ta cùng uống bia nhé

H4

Nhưng để có bia thì phải xì tiền ra mua. Bạn sẽ lấy ra 1 bitcoin trong số tiền vừa rồi để mua bia nhé. Có vẻ bắt đầu hiểu, nhưng đây vẫn không phải là cách mà các giao dịch ( transaction ) hoạt động

H5

Thực tế sẽ không phải như thế này

Thay vào đó chúng ta sẽ phải gửi theo lô toàn bộ 25 bitcoin trong giao dịch

Nhưng cần nhớ rõ là chúng ta sẽ không tiêu cả 25 bitcoin cho việc thanh toán một đơn hàng có giá trị 1 bitcoin.  Chúng ta phải tách lô bitcoin này và gửi đến 2 đích khác nhau

1. Cửa hàng bia ( thanh toán )

2. Gửi lại cho chính địa chỉ của mình ( tiền thừa được trả lại ) 

H6

Một số lô ( batch ) mới được tạo ra gọi là Outputs

Có vẻ như là một cách làm rất lòng vòng nhưng nó cho cùng một kết quả so với cách nghĩ ban đầu

> Tại sao các giao dịch lại hoạt động theo cách này? Bởi vì nó đơn giản và an toàn hơn nếu nhìn từ khía cạnh lập trình

Đây là hình ảnh của các địa chỉ sau giao dịch

H7

Cửa hàng bia có 1 batch 1 bitcoin còn chúng ta vừa tự gửi cho mình 1 batch 24 bitcoin còn lô 25 bitcoin ban đầu được chuyển sang trạng thái "sử dụng hết".

H8

H3
