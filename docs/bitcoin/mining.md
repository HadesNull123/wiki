                                                

Mining là quá trình add thêm các block vào blockchain



### Mining là gì?

Mining là quá trình thêm các transaction vào blockchain

## Quá trình này hoạt động như thế nào?

Mọi Node trên Bitcoin Network sẽ đều share thông tin chung về các transaction mới. Chúng sẽ lưu trữ các transaction này trên MEMORY TOOL của riêng mình. Dưới đây là hình dung về MEMORY TOOL.

![01-network-memory-pool.png](images/01-network-memory-pool.png)

Mỗi Node cũng có tùy chọn ( option ) để thử và đào ( mine ) các giao dịch trên MEMORY TOOL để đưa vào file chưa tất cả các transaction được xác nhận ( mine ) , file này chính là blockchain.

![02-node-pool-block.png](images/02-node-pool-block.png)

Để add được 1 transaction từ Memory Pool vào trong Blockchain thì Node sẽ tốn rất nhiều tài nguyên tính toán ( computer processing power ), và tất nhiên đi kèm với nó là việc tốn điện để chạy. 

Việc tốn kèm này là bắt buộc, nó tạo ra thách thức đối với Memory Pool

## Thách thức đó là gì?

Hãy tưởng tượng bạn là 1 Node, bạn có thể biến đổi các transaction thành một chuỗi các ký tự chữ và số

![03-node-pool-string.png](images/03-node-pool-string.png)

Bây giờ mục tiêu của bạn là hash chuỗi ký tự này cùng với một con số để tạo ra một chuỗi ký tự mới bắt đầu bằng một số các chữ số 0.

![04-node-pool-string-nonce.png](images/04-node-pool-string-nonce.png)

Đầu tiên chúng ta chọn 1 số nonce đem hash với chuỗi loằng ngoằng ở trên để ra một chuỗi mới.

![04-node-pool-string-nonce-success.png](images/04-node-pool-string-nonce-success.png)

Sau khi có chuỗi mới ta lại thay tiếp nonce bằng 1 số khác, thường là cứ theo thứ tự tặng dần 2,3, 4.. cho đến khi tìm được số nonce cuối cùng giúp tạo ra chuỗi thỏa mãn điều kiện giải quyết được bài toán. Ở đây số nonce tìm được cuối cùng là 80085










