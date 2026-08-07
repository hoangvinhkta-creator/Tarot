# Nguồn tranh 78 lá

## Tác phẩm gốc

Bộ **Rider–Waite–Smith** (1909), tranh của **Pamela Colman Smith** (1878–1951),
xuất bản lần đầu bởi William Rider & Son, London.

Việt Nam bảo hộ quyền tác giả theo công thức *đời tác giả + 50 năm*
(Luật Sở hữu trí tuệ, Điều 27). Pamela Colman Smith mất năm 1951, nên bộ tranh
đã thuộc **phạm vi công cộng tại Việt Nam từ năm 2002**.

## Bản dùng trong dự án

Ảnh scan lấy từ gói npm `@cometpisces/tarot-kit-images` (78 file PNG, 300×527).
Phần mã của gói theo giấy phép MIT. Về phần tranh, gói ghi rõ:

> The Rider-Waite tarot card images included in this package are believed to be
> in the public domain in many jurisdictions. However, their copyright status may
> vary by country and intended use. Users are responsible for verifying the
> licensing requirements in their jurisdiction […] For commercial projects, please
> consult with a legal professional.

**Cần làm trước khi thu phí:** nhờ luật sư xác nhận lại tình trạng bản quyền cho
đúng thị trường và mô hình kinh doanh của dự án. Kết luận ở trên là căn cứ pháp lý
phổ thông, không thay thế ý kiến tư vấn.

## Xử lý ảnh

Mỗi file được resize về 384×674, đưa qua bảng màu song sắc (duotone) sắc tro
trung tính rồi lưu WebP chất lượng 70 — trung bình 22 KB/lá, tổng 1,7 MB.
Tên file `NN.webp` khớp đúng thứ tự `DECK` trong `index.html`:

| Chỉ số | Nhóm |
|---|---|
| 00–21 | Ẩn chính (The Fool → The World) |
| 22–35 | Gậy (Ace → King of Wands) |
| 36–49 | Cốc |
| 50–63 | Kiếm |
| 64–77 | Tiền |

## Vì sao chỉ có một bộ file

Ba bộ sưu tập trong app đều dùng chung đúng 78 file này; mỗi bộ chỉ là một
công thức `filter` CSS phủ lên trên (xem `COLLECTIONS` trong `index.html`):

- **Bản Mộc** — không phủ gì, sắc tro nguyên bản
- **Ánh Kim** — `brightness(1.02) sepia(.85) saturate(1.9)`
- **Hắc Diệu** — `brightness(.78) sepia(.95) hue-rotate(185deg) saturate(1.7)`

Thêm một bộ mới cho đợt phát hành hàng tháng chỉ tốn thêm một dòng công thức,
không tốn thêm một byte dung lượng nào.
