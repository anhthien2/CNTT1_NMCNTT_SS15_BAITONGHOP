# PHẦN 1 – HYBRID WORKFLOW

**1. Laptop hỏng mất file Slide có xảy ra không nếu đã dùng Hybrid?**  
**Không.** Vì Hybrid = Local + Auto Sync. File `Slide_BaoCao.pptx` làm trên máy sẽ tự động đẩy lên Cloud ngay khi bấm Ctrl+S. Hỏng ổ cứng thì chỉ cần đăng nhập OneDrive/Google Drive trên máy khác là tải lại bản mới nhất.

**2. 3 bước thiết lập Auto Sync ngay hôm nay:**

-   B1: Cài OneDrive/Google Drive Desktop, đăng nhập 1 tài khoản chung của nhóm.
-   B2: Tạo thư mục `D:\OneDrive\SmartCampus` và bật `Files On-Demand + Always keep on this device` cho thư mục dự án.
-   B3: Cả nhóm chỉ làm việc trong thư mục đó, tuyệt đối không lưu ra Desktop riêng.

**3. Lỡ xóa nhầm 2 trang trong báo cáo 10 phút trước:**  
Vào `BaoCao_CuoiKy_SmartCampus.docx` trên Drive > Chuột phải > `Version History / Lịch sử phiên bản` > Chọn bản 10 phút trước > `Restore / Khôi phục`. Không cần gõ lại.

**4. Đồng bộ cả** **`node_modules`** **và file phim 4K là 2 sai lầm:**

-   **Sai lầm 1: Đồng bộ rác kỹ thuật:** `node_modules` có hàng vạn file nhỏ làm treo Sync Engine và tràn dung lượng. **Cách xử lý:** Loại trừ bằng `mklink /D` ra ngoài OneDrive, chỉ cần giữ `package.json`.
-   **Sai lầm 2: Dùng Cloud chứa file giải trí cá nhân:** Phim 4K không phải tài liệu dự án. **Cách xử lý:** Để ở ổ D local, không cho vào thư mục Sync.

# PHẦN 2 – PHÂN QUYỀN CHIA SẺ

### PHẦN 2 – PHÂN QUYỀN CHIA SẺ

**1. Bảng phân quyền:**

| File | Mức quyền | Phạm vi chia sẻ | Giải thích |
| :--- | :--- | :--- | :--- |
| `BaoCao_CuoiKy_SmartCampus.docx` gửi giảng viên | **Viewer** | **Restricted - chỉ mail giảng viên** | Để giảng viên chấm, không cho sửa đè |
| `Slide_BaoCao.pptx` cho 5 thành viên | **Editor** | **Restricted - 5 mail thành viên** | Cả nhóm cần cùng sửa gấp |
| `GopY_BanNhap.docx` gửi anh khóa trên | **Commenter** | **Restricted - chỉ mail anh khóa trên** | Chỉ muốn nhận xét, không cho sửa trực tiếp |
| `ThongTin_CaNhan_NhomVien.xlsx` | **Restricted - Owner duy nhất** | **Chỉ trưởng nhóm - Không share** | Chứa CCCD, SĐT, tuyệt mật, không share |

**2. Quy tắc Cờ Đỏ Bảo mật:**
> Tuyệt đối không dùng `Anyone with the link + Editor` cho file chứa dữ liệu nhạy cảm. Vì ai có link cũng vào được, được quyền sửa/xóa và share tiếp ra ngoài, sẽ lộ toàn bộ CCCD cả nhóm.

**3. 2 thao tác Settings cho file Editor:**
*   **TẮT:** `Editors can change permissions and share` - Ngăn Editor tự mời thêm người lạ
*   **BẬT:** `Viewers can see version history` hoặc kiểm soát download tùy nhu cầu

# **Phần 3 –** Tổ chức giao tiếp nhóm chuẩn doanh nghiệp

**1. 3 vấn đề trong đoạn Zalo:**

-   **No-Hello:** Lan chỉ hỏi "có ai rảnh không" không có ngữ cảnh, người khác không biết trả lời sao.
-   **Spam / Chat lạc chủ đề:** Hoa gửi ảnh mèo làm loãng thông tin công việc.
-   **Tag @all giờ khuya + Thiếu ngữ cảnh:** Trưởng nhóm tag @all lúc 23:47 gây làm phiền, tin nhắn lại không nói rõ ai thiếu phần nào.

**2. 2 Channel nên tạo trên Lark/Slack:**

-   `#thong-bao-deadline` - Chỉ trưởng nhóm post thông báo quan trọng, cấm chat.
-   `#thao-luan-cong-viec` - Để hỏi đáp, góp ý báo cáo.
-   `#giai-tri-tan-gau` - Cho ảnh mèo, tám chuyện.

**3. Viết lại tin nhắn của Lan theo Asynchronous:**

> Chào mọi người, mình là Lan phụ trách phần 2.3. Mình đang kẹt ở chỗ vẽ biểu đồ, cần bạn nào rành Excel xem giúp file `BaoCao...docx` trang 10 trong 15 phút được không ạ? Cảm ơn!

**4. Viết lại tin nhắn @all lúc 23:47 dùng Schedule Send:**  
Thay vì gửi lúc 23:47, bấm `Schedule Send -> 8:00 AM mai` với nội dung:

> Chào @Nam @Tuan, 2 bạn chưa gửi phần 3.1 và 3.2, deadline là trưa mai. Nhờ 2 bạn update vào file `Slide_BaoCao.pptx` trước 10h sáng nay giúp mình nhé.

# PHẦN 4 – THÔNG BÁO TỔNG HỢP

Em đăng lên `#thong-bao` như này là đủ 3 kỹ năng:

 **[****THÔNG BÁO] Setup Cloud Workspace xong - 8h00 30/10**  
> Chào cả nhóm,
> 
> 1.  Mình đã bật Auto Sync cho thư mục `SmartCampus` trên OneDrive. Từ giờ mọi người chỉ làm việc trong thư mục đó nhé, để tránh mất file khi hỏng máy.
> 2.  File `BaoCao_CuoiKy_SmartCampus.docx` mình đã share cho cô @ với quyền Viewer / Restricted để cô chấm, không sợ bị sửa đè.
> 3.  @Nam @Tuan ơi, 2 bạn còn thiếu phần biểu đồ và kết luận trong `Slide_BaoCao.pptx`, nhờ 2 bạn vào sửa trước 10h hôm nay giúp mình nhé. Cảm ơn!  
>     File hướng dẫn phân quyền mình ghim ở đầu kênh.
