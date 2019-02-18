
# Public Key

Một số duy nhất sinh ra từ private key

# Public Key là gì?

Nó chính là dạng nguyên thủy của một địa chỉ tài khoản bitcoin.

Giống như private key, nó là một con số và thường được biểu diễn dưới dạng số thập lục phân.

Ví dụ

> public_key  = 02b4632d08485ff1df2db55b9dafd23347d1c47a457072a1e87be26896549a8737

Và điểm thú vị nhất chính là public key của bạn được tạo ra từ private key. Nếu như bạn không tiếp tục nén public key lại thành dạng ngắn hơn là address thì bạn hoàn toàn có thể dùng nó luôn làm địa chỉ tài khoản và có thể gửi và nhận bitcoin từ tài khoản này.

# Làm thế nào có thể lấy được public key từ private key?

Bạn cần nhét private key vào một hàm toán học đặc biệt và nó sẽ trả lại cho bạn public key

# Hàm đó là hàm gì vậy?

Hàm đó được gọi là phép nhân elip nó có  dạng mô tả hình học giống như đồ thị cong như hình dưới đây

H1

Chúng ta bắt đầu với 1 điểm G nằm trên đường cong này. Và nếu chúng ta sử dụng 1 phép nhân trên đường cong này.  Ví dụ nhân G với 2 thì kết quả của phép toán này sẽ tương ứng với di chuyển hình học mô tả bằng hình dưới đây theo thứ tự sau.

1\. Vẽ một tiếp tuyến tại điểm G

2\. Chọn điểm giao cắt giữa tiếp tuyến này với đồ thị ( điểm số 2 )

3\.  Lấy giá trị nghịch đảo của điểm số  trên ( đối xứng qua trục hoành )

H2

Thực tế là chúng ta có thể vẽ một tiếp tuyến ở bất cứ đâu, và nó có thể giao với đồ thị tại một điểm khác.

Và bây giờ chúng ta có điểm 2G là đầu ra cho phép biến đổi.  Ta quá trình biến đổi vừa rồi là "phép nhân đường cong elip".  Từ giờ trở đi khi nói đến "phép nhân" chúng ta sẽ hiểu nó là "phép nhân đường cong elip" thay vì phép nhân toán học thông thường mà chúng ta vẫn thấy. Bằng cách "nhân" điểm G với 2 tà có điểm 2G như trên đồ thị.

# Làm thế nào để chúng ta có được public key?

Ở ví dụ trên chúng ta nhân điểm G với 2 và thu được 2G

Để lấy được public key thì chúng ta nhân G với private key

> Ví dụ\
> \
> private_key = ef235aacf90d9f4aadd8c92e4b2562e1d9eb97f0df9ba3b508258739cb013db2
> private_key = 108165236279178312660610114131826512483935470542850824183737259708197206310322
> 
> public_key  = 108165236279178312660610114131826512483935470542850824183737259708197206310322 \* G

Các bạn để ý thấy nếu chúng ta hình dung điểm G như quả bóng bàn thì chuyển động của nó giống như quả bóng bàn nảy qua nảy lại xung quanh trục hoành. Và khi nhân G với 2 thì số lần "bóng nảy" sẽ là 2

H3

Khi thay 2 bằng private key thì chúng ta sẽ có một chuyển động phức tạp hơn thế rất nhiều, cụ thể số lần "bóng nảy" ở đây sẽ là bằng private key.

Điểm cuối cùng trên đường cong mà chúng ta thu được sẽ cung cấp cho chúng ta một cặp tọa độ 

Ví dụ

> x = 81591541406288143274758265124625798440200740391102527151086648448953253267255
> y = 64573953342291915951744135406509773051817879333910826118626860448948679381492

Thao tác tiếp theo là chúng ta chuyển đổi các tọa độ này sang dạng thập lục phân

> public_key (x) = b4632d08485ff1df2db55b9dafd23347d1c47a457072a1e87be26896549a8737
> public_key (y) = 8ec38ff91d43e8c2092ebda601780485263da089465619e0358a5c1be7ac91f4
> 
> public_key (x,y) = b4632d08485ff1df2db55b9dafd23347d1c47a457072a1e87be26896549a87378ec38ff91d43e8c2092ebda601780485263da089465619e0358a5c1be7ac91f4
