1.  Reflex Agent
    Tính điểm của trạng thái đích dựa trên khoảng cách đến thức ăn và ma xung quanh trạng thái đích.

2.  Minimax
    Sử dụng hàm đệ quy minimax nhận vào trạng thái của game, agent và độ sâu:

- Trả về đánh giá điểm của trạng thái đang xét nếu:
  - là trạng thái cuối
  - đạt đến độ sâu cần tìm
- Sử dụng biến result để lưu chỉ số min hoặc max + action đi kèm.
- Duyệt qua các nước đi hợp lệ có thể tới từ agent đang xét:
  - với mỗi nước đi chạy hàm minimax để lấy điểm
  - nếu agent là pacman thì sẽ chọn nước đi có điểm lớn nhất
  - nếu agent là ma thì sẽ chọn nước đi có điểm thấp nhất

3.  Alpha-Beta Pruning
    Tương tự minimax và có thêm thao tác cắt nhánh:

- Sau khi cập nhật maxValue, nếu maxValue > beta thì cắt nhánh, không thì cập nhật alpha = maxValue
- Sau khi cập nhật minValue, nếu minValue < alpha thì cắt nhánh, không thì cập nhật beta = minValue

4.  Expectimax
    Tương tự minimax nhưng giá trị nước đi ma = tổng giá trị của các action hợp lệ / số action hợp lệ
5.  Evaluation Function
    Tính điểm của trạng thái đích dựa vào sự ưu tiên giảm dần:
