
# Private Key

Là một rất lớn được sinh ra một cách ngẫu nhiên.

Ví dụ

> Private Key dạng thập phân: 108165236279178312660610114131826512483935470542850824183737259708197206310322

Giải thích một cách chính xác hơn nữa thì vì bitcoin sử dụng 256 bit nên biểu diễn dưới dạng nhị phân chúng ta sẽ thấy private key như sau

> Private Key dạng nhị phân 1110111100100011010110101010110011111001000011011001111101001010101011011101100011001001001011100100101100100101011000101110000111011001111010111001011111110000110111111001101110100011101101010000100000100101100001110011100111001011000000010011110110110010

Chúng ta cũng có thể có dạng biểu diễn dạng thập lục phân

> Private key thập lục phân ef235aacf90d9f4aadd8c92e4b2562e1d9eb97f0df9ba3b508258739cb013db2u

Thông thường đây là dạng phổ biến nhất mà chúng ta thấy.

# Số 256 bit là gì?

Bit là đơn vị nhỏ nhất của dữ liệu trong máy tính.  Nó chỉ có thể lưu được 1 giá trị là 0 hoặc 1.

H1

Tuy nhiên bạn có thể dùng nhiều bit để biểu diễn mọi loại dữ liệu như là các con số mà chúng ta thấy hàng ngày. Hình ảnh dưới đây cho chúng ta thấy cách mà máy tính sử dụng bit để lưu trữ các số khác nhau

H2

Một số 256 bit là một số được biểu diễn bằng 256 bit

H3

Ở trên là giá trị lớn nhất có thể biểu diễn được bằng 256 bit. Nên có thể nói 1 số 256 bit là một số nằm giữa khoảng\\

Min: 0

Max: 115792089237316195423570985008687907853269984665640564039457584007913129639935

256 bit cho ta không gian để biểu diễn một lượng số khá lớn. Tổng số các số mà 256 bit có thể biểu diễn là 2 mũ 256.

# Private Key từ đâu ra?

Nhưng đã nói ở trên, nó được sinh ra một cách ngẫu nhiên. Chương trình sinh ra số ngẫu nhiên thì đơn giản thôi, và nó có 1 chương trình sinh số ngẫu nhiên 256 bit được nhúng trong phần mềm bitcoin.

H4

Nếu muốn thì bạn có thể tự mình tạo ra một số ngẫu nhiên bằng 3 cách sau

1\. Tung đồng xu 256 lần

H5

Kết quả sẽ cho bạn 1 số nhị phân biểu diễn bằng 256 bit và bạn có thể chuyển đổi sang các dạng khác

2\. Dùng một ngôn ngữ lập trình ưa thích để viết một hàm sinh ra số ngẫu nhiên

`# need to use the operating system's random number generator for security import random random.SystemRandom().randint(1, 115792089237316195423570985008687907852837564279074904382605163141518161494337)`

Hàm này sẽ sinh ngẫu nhiên cho bạn một số thập phân.

3\. Băm dữ liệu (hash ) sử dụng hàm SHA256\
\
H6

Hàm này sẽ trả về cho ta một số thập lục phân

Tất cả các cách trên đều cho ta một số 256 bit. Và chỉ cần có số này bạn sẽ có private key

# Điều gì xảy ra nếu người khác cũng sinh ra một private key giống như bạn?

Nếu họ có 1 private key giống như bạn thì tức là họ cũng sẽ ăn trộm được bitcoin từ ví của bạn. Tuy nhiên bạn đừng lo về vấn đề này.  Không ai có thể sinh ra ngẫu nhiên con số private key giống như của bạn.

# Chẳng lẽ lại không thể xảy ra tình huống đó ?

Về lý thuyết thì là có, nhưng tùy thuộc vào phạm vi của của private key mà điều này gần như là không thể xảy ra. 

Ví dụ bạn có 1 triệu con khỉ mà mỗi con trong số chúng có thể sinh ra 1 triệu private key trong vòng 1 giây ( nếu những con khỉ của bạn đủ thông minh để bạn huấn luyện chúng làm điều đó ) thì trung bình cũng sẽ mất khoảng thời gian là 3,671,743,063,080,802,746,815,416,825,491,118,336,277,193,184,902,172 triệu năm để một con khỉ có thể sinh ra được 1 private key giống như bạn.

Như bạn thấy, không ai có thể làm được điều đó. Phạm vi của 1 số 256 ( cũng là phạm vị mà các private key ) được sinh ra là vô cùng lớn.  Trí óc con người không có đủ khả năng để trực quan hóa phạm vi của vũ trụ cũng như phạm vi số học của 256 bit này. Vây nên nếu bạn có chút nghi ngờ nào về mức độ an toàn của thì có thể là do bạn đã dùng 1 chương trình ( phần mềm ) sinh số ngẫu nhiên không đáng tin cậy  hoặc bạn chưa hình dung và đánh giá đúng về độ lớn của số private key thôi.


`keys = 115792089237316195423570985008687907852837564279074904382605163141518161494337
monkeys = 1000000
monkeyhashrate = 1000000

keyspersecond = monkeys * monkeyhashrate

seconds = keys / keyspersecond
minutes = seconds / 60
hours = minutes / 60
days = hours / 24
years = days / 365
millionyears = years / 1000000

print millionyears`
