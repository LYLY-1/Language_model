# Search_Estates
Bước đầu tiên để xử lí ngôn ngữ tự nhiên thì quan trọng nhất vẫn là xử lí data.

Ở đây mình nhận thấy trong file data real_estates.txt có rất nhiều emoji, URL, từ viết tắt và viết không dấu, các kí tự không cần thiết. Nên tôi đã xử lí emoji qua hàm remove_emoji(), xử các kí tự không cần thiết ở hàm remove(),... (được code ở phía dưới). file replace_with_2_space.txt lưu những từ viết tắt, viết không dấu hoặc viết sai để tiện trong việc thay thế chúng. Sau khi chạy xong hàm slove(), sẽ có 1 file là real_estates_after.txt. File này chứa data sau khi đã xử lí.

Xong phần xử lí, mình tiếp tục với việc traning model Language n-gram. Mình đã nhờ vào sự hướng dẫn của trang web: https://viblo.asia/p/language-modeling-mo-hinh-ngon-ngu-va-bai-toan-them-dau-cau-trong-tieng-viet-1VgZveV2KAw

Theo như tác giả của trang web này, Statistical Language Model, là tính xác xuất xuất hiện của một bộ từ (w_1...w_n), cái này thì chắc chắn sẽ ổn, vì thường các bộ w như thế sẽ giống văn viết hơn, và model sẽ học được từ văn viết đó. Một hướng tiếp cận cụ thể của statistical language model là N-gram language model, nghĩa là giới hạn lại n, trong bộ (w_1...w_n), và tính xác xuất có điều kiện của bộ này, dựa trên các bộ nhỏ hơn như là (w_1...w_n-1)