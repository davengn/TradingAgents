# TradingAgents (bản fork cá nhân của Duy)

Hệ thống đa agent hỗ trợ một nhà đầu tư cá nhân trung hạn trên chứng khoán Việt Nam theo phong cách "phụ trợ": tìm xu hướng có bằng chứng, chọn mắt xích bắt buộc, và khuyến nghị thời điểm giải ngân DCA.

## Language

**Xu hướng chủ đạo**:
Một thay đổi cấu trúc đang thực sự diễn ra ở Việt Nam, được chứng minh bằng số liệu định lượng, không phải một chủ đề báo chí hay kỳ vọng.
_Avoid_: theme, trend (khi chưa có bằng chứng), hot topic

**Mắt xích bắt buộc**:
Doanh nghiệp mà mọi bên tham gia một Xu hướng chủ đạo đều phải đi qua hoặc trả tiền cho (nút thắt hạ tầng, đầu vào độc quyền hoặc gần độc quyền, giấy phép, logistics, năng lượng). Doanh nghiệp thay thế được thì không phải mắt xích bắt buộc.
_Avoid_: picks and shovels (chỉ dùng như tên phong cách), cổ phiếu hưởng lợi gián tiếp, supplier

**Cổ phiếu headline**:
Cổ phiếu được thị trường gắn trực tiếp với một Xu hướng chủ đạo. Hệ thống không mua loại này trừ khi nó cũng là Mắt xích bắt buộc.
_Avoid_: cổ phiếu dẫn sóng

**Watchlist**:
Danh sách các Mắt xích bắt buộc do hệ thống xác định, là đầu vào cho phân tích từng mã.
_Avoid_: danh mục (portfolio là sổ nắm giữ thực tế của Duy)

**Cổng giá tốt**:
Bước cuối quyết định một Mắt xích bắt buộc trong Watchlist có đủ điều kiện nhận khoản DCA tháng này hay phải chờ.
_Avoid_: tín hiệu mua

**Khuyến nghị giải ngân**:
Kết quả hằng kỳ của hệ thống cho Duy: mã nào đủ điều kiện nhận DCA, hoặc chờ, kèm lý do. Hệ thống chỉ khuyến nghị; Duy tự đặt lệnh.
_Avoid_: lệnh, order, tự động giao dịch

**Ngân sách DCA**:
Số tiền tối đa Duy giải ngân mỗi tháng (dưới 10 triệu VNĐ), là tham số cấu hình của Cổng giá tốt.
_Avoid_: vốn, khẩu vị rủi ro

**Sổ trắng**:
Trạng thái Duy chưa nắm giữ mã nào và đã khai báo điều đó cho hệ thống. Khác với "không có thông tin sổ", nơi hệ thống không được suy ra là Duy chưa có gì.
_Avoid_: portfolio rỗng, danh mục trống

**Khởi động đầu**:
Lần chạy đầu tiên dựng Xu hướng chủ đạo và Watchlist ban đầu từ Sổ trắng, trước khi vào nhịp chạy hằng ngày.
_Avoid_: bootstrap, cold start

**Backend agent**:
Một agent dạng CLI/IDE (Claude Code, Codex, Antigravity) được dùng như nguồn LLM qua gói đăng ký của Duy, thay cho API key.
_Avoid_: provider (provider là khái niệm sẵn có của repo, gồm cả API key)
