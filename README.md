# BÀI TẬP: SO SÁNH ZERO-SHOT VÀ FEW-SHOT PROMPTING

## 1. Prompt 1 – Zero-shot

```text
Bạn là nhân viên chăm sóc khách hàng. Hãy phân loại 5 phản hồi sau thành 3 nhãn:
- Tích cực: Khách hàng hài lòng, khen ngợi.
- Tiêu cực: Khách hàng phàn nàn, không hài lòng.
- Yêu cầu hỗ trợ: Khách hàng cần giải quyết vấn đề cụ thể.

Phản hồi:
1. Sản phẩm đẹp, giao hàng nhanh, rất hài lòng.
2. Tôi đã đặt hàng 5 ngày nhưng chưa nhận được.
3. Tai nghe không kết nối được Bluetooth.
4. Nhân viên tư vấn rất nhiệt tình.
5. Tôi muốn hoàn tiền vì sản phẩm bị lỗi.

Xuất kết quả thành bảng Markdown gồm: STT, Phản hồi, Nhãn phân loại, Lý do.
```

## 2. Prompt 2 – Few-shot

```text
Bạn là nhân viên chăm sóc khách hàng. Hãy phân loại phản hồi thành 3 nhãn: Tích cực, Tiêu cực, Yêu cầu hỗ trợ.

Ví dụ:
1. "Điện thoại đẹp, sử dụng tốt." -> Tích cực.
2. "Giao hàng quá chậm." -> Tiêu cực.
3. "Máy bị lỗi, tôi muốn đổi hàng." -> Yêu cầu hỗ trợ.

Hãy phân loại các phản hồi:
1. Sản phẩm đẹp, giao hàng nhanh, rất hài lòng.
2. Tôi đã đặt hàng 5 ngày nhưng chưa nhận được.
3. Tai nghe không kết nối được Bluetooth.
4. Nhân viên tư vấn rất nhiệt tình.
5. Tôi muốn hoàn tiền vì sản phẩm bị lỗi.

Xuất bảng Markdown gồm: STT, Phản hồi, Nhãn phân loại, Lý do.
```

## 3. Kết quả phân loại

| STT | Phản hồi | Nhãn phân loại | Lý do |
|---|---|---|---|
| 1 | Sản phẩm đẹp, giao hàng nhanh, rất hài lòng. | Tích cực | Hài lòng về sản phẩm và giao hàng. |
| 2 | Đặt hàng 5 ngày nhưng chưa nhận được. | Tiêu cực | Phàn nàn về giao hàng chậm. |
| 3 | Tai nghe không kết nối được Bluetooth. | Yêu cầu hỗ trợ | Gặp lỗi kỹ thuật. |
| 4 | Nhân viên tư vấn rất nhiệt tình. | Tích cực | Khen ngợi nhân viên. |
| 5 | Muốn hoàn tiền vì sản phẩm bị lỗi. | Yêu cầu hỗ trợ | Cần hỗ trợ hoàn tiền. |

## 4. So sánh kết quả

- **Zero-shot:** Không cần ví dụ mẫu, thực hiện nhanh nhưng có thể nhầm lẫn giữa các nhãn.
- **Few-shot:** Có ví dụ hướng dẫn, giúp AI hiểu quy tắc và phân loại nhất quán hơn.

