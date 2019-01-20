Difficulty

Cơ chế để điều chỉnh thời gian cần để đào được một block mới.

Difficulty ( độ khó ) là cái gì?

Difficulty là một con số để điều chỉnh bao lâu thì một miner có thể thêm được block vào blockchain

Ảnh 1

Giá trị của Difficulty được update 2 tuần một để đảm bảo cứ trung bình 10 phút thì một block mới sẽ được đưa vào blockchain

Tại sao Difficulty lại quan trọng?

Bởi vì nó đảm bảo rằng các block sẽ được add vào blockchain một cách định kỳ kẻ cả là khi có thêm nhiều miner tham gia vào trong bitcoin network.

Nếu độ khó là một hằng số nó sẽ làm chi việc  add thêm block mới vào blockchain tốn ít thời gian hơn khi có nhiều miner tham gia vào network

Khi nào  thì Difficulty thay đổi?

Difficulty sẽ được điều chỉnh sau mỗi khoảng thời gian 2016 block được thêm vào blockchain ( sấp xỉ khoảng 2 tuần )

Tại mỗi khoảng thời gian này, mỗi node sẽ tính thời gian dự kiến cho 2016 block sẽ được đào ( 2016 X 10 phút )  chia cho thời gian thực tế mà nó tiêu tốn để đào được một block

expected / actual 20160 / actual

Nếu miner có thể đào được block nhanh hơn so với thời gian dự kiến, ví dụ là 9 phút thì con số mà nó thu được sẽ là

2016 X 10/ 2016 X 9= 21060/18144=1.11

Khi đó mỗi node sẽ điều chỉnh độ khó của mình cho 2016 block tiếp theo như sau

difficulty x 1.11 = new difficulty

Nếu tỉ số ở trên lớn hơn 1 thì tức là block sẽ được đào nhanh hơn dự kiến thì độ khó Difficulty sẽ được điều chỉnh tăng lên

Nếu tỉ số ở trên nhỏ hơn 1 tức là block sẽ được đào chậm hơn so với với dự kiến thì độ khó Difficult sẽ được điều chỉnh giảm đi

Và như vậy mỗi miner sẽ trong mạng bitcoin network sẽ làm việc với một độ khó mới cho 2016 block tiếp theo.

Độ khó ( Difficulty )sẽ chỉ điều chỉnh theo hệ số tối đa là 4 (tức là một số không lớn hơn 4 hoặc nhỏ hơn 0,25). Điều này là để ngăn chặn những thay đổi đột ngột từ khó khăn này sang khó khăn khác.

Làm thế nào để Difficulty có thể điều khiển được thời gian giữa các block?

Ok, chúng ta sẽ bắt đầu từ một ví dụ đơn giản cho dễ hiểu

1. Ví dụ đơn giản

Giả sử bạn có 1 dãy số từ 1 đến 100

Ảnh 2

Bây giờ mỗi phút bạn có thể sinh ra một con số ngẫu nhiên nằm trong dãy từ 1 đến 100 này. Và mục tiêu của bạn là phải sinh ra được một con số nằm dưới giá trị Target.

Giả sử giá trị Target được đặt là 50

Ảnh 3

Hãy xem lại nhé, tốc độ để bạn sinh ra 1 só trong khoảng từ 1-100 là một phút, nhưng khi Target bị giảm xuống còn 50 thì xác suất để sinh ra một số nhỏ hơn 50 trong khoảng từ 1-100 sẽ giảm đi một nửa nên thời gian trung bình để sinh ra con số đó sẽ mất khoảng 2 phút. Nếu giảm Target xuống còn 20 thì cơ hội để bạn sinh ra số thỏa mãn điều kiện nhỏ hơn Target sẽ chỉ là 1/5 so với ban đầu, và thời gian để sinh ra một số như thế sẽ là 5 phút. 

Ảnh 4

Càng hạ thấp số Target thì càng khó để sinh ra con số ( winning number ) thỏa mãn yêu cầu.

Không phải lúc nào cũng cần đến 5 phút để bạn giành chiến thắng, đôi khi bạn gặp may mắn hơn ngay ở lần đầu tiên và tìm được con số may mắn bởi vì các số được sinh ra một cách ngẫu nhiên. Nhưng trong quá trình lâu dài thì 5 phút sẽ là con số trung bình để đạt được điều đó

Do đó dựa trên việc có bao nhiêu con số có thể sinh ra trong 1 phút chúng ta có thể điều chỉnh Target để kiểm soát việc mất bao lâu để có thể tìm ra con số wining number.

Thiết lập Difficulty

Đối với máy tính thay vì nói cho bạn một giá trị Target giống như ở ví dụ trên thì nó sẽ đưa cho bạn giá trị Target bằng cách phân chia khoảng các số bằng con số mới

Hình 5

Con số mới này có thể kiểm soát giá trị Target

Con số mới đó chính là Difficulty, có thể dễ dàng sử dụng nó để điều chỉnh giá trị Target

Đây là phương trình để tìm giá trị Target

target = targetmax / difficulty
