# button_conic_ok_2

https://www.youtube.com/watch?v=zZeyTMPVJng

lỗi để margin 0 auto 
khiến cho khi để position absoulute
t0,b0,r0,l0 -->>> sẽ dẫn đến tình trạng là không được ở giữa
--------->>> cách fix : dùng margin auto @@

??? tại sao không dùng được bottom trong  trường hợp dùng lớp giả 
::before đã được xét height 100% width 100% top:0 left:0 
-->>> thì khi viết ra mới hiểu
xét top và left sau đó xét width,height 100% mục đích để cho thẻ giả được chiếm hết phần bằng thẻ cha

--->> vậy nên chữ không được vào giữa --->>> để giải quyết cái này thì thêm line-height=height thằng cha là được 


--->>> lỗi conic-gradient --->>> màu cuối mà vẫn để dấu phẩy @@ ngáo chóa

-->>> lỗi : pseudo element không xét content khiến cho không hiển thị trong dev tool

---->>> trong video tutorial --->>> xét index của after là -1 thì nó sẽ bị background mặc định 
của thằng button đè lên --->>> vậy để giải quyết điều này thì set background của button : transparent

---->>> họ là xét cho background conic to lên rồi dùng overflow: hidden cho thằng btn 
---->>>>>>>>>> mục đích để ẩn đi --->>>> ^^ hợp lý
---->>> nhưng mà họ lại xét thủ công cái margin -->>> nên thôi mình cứ để 100% width height cho ok

--->>> bài này ta biết thêm được thuộc tính backdrop-filter: blur(20px); 
-->> LƯU Ý : mình sẽ xét cho thằng z-index trên cao mới có hiệu ứng ^^ 
như ở đây xét cho thằng ::before vì mình đã xét cho nó z-index cao nhất rồi
còn nếu mà xét là thằng ::after thì không có hiệu lực ... vì mờ bối cảnh mà nó chìm thấp nhất rồi thì 
làm quèn ^^ 


---->>> vấn đề phát sinh thêm backdrop cho thằng cao nhất thì thằng thấp nhất không ăn được border-radius
----->>> thì ok rất đơn giản như sau mình xét all đều cùng một cỡ border-radius


----->>>>>>>>>>  keyframes animation : spin xong thì mới hiểu vấn đề vì sao lại overflow 
và để thằng :after chứa background nó bao to hơn 
----->>> vì khi xoay mình làm theo kiểu mình là ko để overflow tức là sẽ có cả một khối nó xoay đằng sau ^^
như cánh quạt vậy @@
