# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` | Xe ô tô chở người thông thường | Sedan, hatchback, SUV, crossover |
| `truck` | Xe tải dùng để chở hàng | Có thùng hàng hoặc khoang chở hàng riêng |
| `bus` | Xe buýt hoặc xe khách nhiều chỗ ngồi | Kích thước lớn, phục vụ vận chuyển hành khách |
| `van` | Xe van hoặc xe giao hàng thân liền khối	 | Thân xe dạng hộp, nhỏ hơn bus, thường không có thùng tải hở |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: Bounding box bao phủ toàn bộ thân xe nhìn thấy được và hạn chế lấy nền xung quanh.
- Vật thể bị che khuất: Vẫn gán nhãn nếu còn đủ phần xe để nhận biết loại phương tiện.
- Vật thể bị cắt bởi rìa ảnh: Vẫn gán nhãn phần còn nhìn thấy nếu có thể xác định.
- Vật thể rất nhỏ/mơ hồ: Không gán nhãn nếu không đủ thông tin của xe

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_...` | Xe bị che khuất một phần phía sau xe khác | Label car | Vẫn nhận diện được hình dạng xe con |
| `drive_...` | Phương tiện thân dài dạng chở khách | Label car | Kích thước lớn và là xe chở hành khách |
| `drive_...` | Xe thân hộp nhỏ dùng giao hàng | Label car | Thân xe liền khối, phù hợp lớp van |
