# Báo cáo cá nhân — Ngày 2 Object Detection

Đổi tên file theo `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md`. Điền kết quả thật, xóa dòng hướng dẫn khi nộp. Xem [quy định nộp](../../SUBMISSION.md).

## 1. Thông tin học viên

- Họ tên: Đinh Hữu Thái An 
- MSSV: 2A202603283
- Email: dinhhuuthaian9191@gmail.com
- Lớp: AI.20K E403
- Link repo bài làm: https://github.com/dinhhuuthaian/K5-L2-Day02-DinhHuuThaiAn-2A202603283-ObjectDetection
- Link Colab đã chạy:

## 2. Schema và mini guideline

Dẫn tới [GUIDELINE_MINI.md](../../GUIDELINE_MINI.md). Tóm tắt ba ca mơ hồ đã quyết định, cách áp dụng schema và phần cần giảng viên làm rõ.

## 3. Annotation và self-QC

- Số file nhãn train:
- Kết quả checker và lỗi đã xử lý:
- Danh sách ít nhất 10 ảnh đã rà bằng mắt:
- Lỗi bỏ sót/box/class phát hiện khi rà và cách sửa:
- Commit khóa nhãn ban đầu:

## 4. Gold QC và rework

| Chỉ số | Trước sửa | Sau sửa nếu có |
|---|---:|---:|
| TP | 454 | |
| FP | 625 | |
| FN | 199 | |
| Precision | 0.4208 | |
| Recall |  0.6953 | |
| F1 | 0.5242 | |
| mean_iou_of_matches |  0.8022 | |
| passed | false (Chưa đạt ngưỡng yêu cầu) | |

Nhận xét:

TP = 454 cho thấy đa số đối tượng trong bộ dữ liệu đã được gán nhãn.
FP = 625 còn khá cao, nguyên nhân có thể do gán nhãn dư hoặc nhãn chưa thống nhất với gold set.
FN = 199 cho thấy vẫn còn một số đối tượng bị bỏ sót.
Mean IoU = 0.8022 đạt ngưỡng yêu cầu, chứng tỏ các bounding box khớp thường có độ chính xác vị trí tốt.
F1 = 0.5242 thấp hơn ngưỡng yêu cầu 0.8 nên chưa đạt tiêu chí chất lượng annotation.
Em coi hình trong gold train em thấy xe bus mà nó để là xe van em k biết đó có phải là lí do của em không đạt không ạ

## 5. Kết quả YOLO

- Runtime, GPU/CPU, phiên bản Ultralytics và Torch:
- Các tham số thay đổi so với notebook nếu có và lý do:
- Đường dẫn best checkpoint trong phiên chạy:

| Chỉ số trên 10 ảnh eval | Giá trị |
|---|---:|
| Precision | |
| Recall | |
| mAP50 | |
| mAP50–95 | |

Đặt cả 2 folder `assets/eval_predictions/` và `assets/yolo26_runs/` (giải nén từ `day2_colab_outputs.zip`) cạnh báo cáo và dẫn link tương đối. Không chỉ ghi số; chỉ ra ít nhất một ảnh và vật thể cụ thể.

Trả lời bốn câu hỏi cuối notebook:

1. Lớp nào recall thấp nhất? Ảnh nào minh họa?
2. Nếu mAP50 cao nhưng mAP50–95 thấp, cần kiểm điều gì trên box?
3. Lỗi class nào có thể liên quan guideline? Dữ kiện nào hỗ trợ nhận xét?
4. Vì sao không dùng 10 ảnh eval để train? Vai trò validation của chúng trong notebook là gì?

## 6. Khó khăn và cách xử lý

| Bước/thời điểm | Lỗi quan sát | Cách đã thử | Kết quả/còn thiếu |
|---|---|---|---|
| | | | |

## 7. Tự đánh giá theo rubric

Đối chiếu [RUBRIC.md](../../RUBRIC.md): phần nào đã có kết quả, phần nào còn thiếu hoặc chưa kiểm được. Không tự nhận hoàn thành bước chưa chạy.
Hoàn thành gán nhãn 50 ảnh train.
Hoàn thành cấu trúc dataset theo định dạng YOLO.
Hoàn thành kiểm tra bằng check_yolo_labels.py.
Đã chạy evaluate_annotations.py và nhận kết quả đánh giá.
Chưa thực hiện huấn luyện YOLOv11/YOLOv8 trên Colab.
Chưa có kết quả mAP50 và mAP50-95 của mô hình.
## 8. Công cụ AI và tài liệu tham khảo

Ghi công cụ đã dùng, dùng ở bước nào và phần đã tự kiểm tra; không dùng thì ghi rõ. Liệt kê nguồn ngoài repo được sử dụng. Không ghi mật khẩu/token hoặc đính kèm gold train.
Microsoft Copilot: hỗ trợ giải thích các chỉ số Precision, Recall, F1, TP, FP, FN và rà soát nội dung báo cáo.
ChatGPT: hỗ trợ giải thích quy trình Object Detection và định dạng báo cáo Markdown.
