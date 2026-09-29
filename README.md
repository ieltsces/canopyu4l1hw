# 🎨 Unit 4 — My Hobbies · 我的爱好 (Wǒ de àihào)

Trang web học đa ngữ (Anh – Trung) cho trẻ **4–10 tuổi**. Trẻ chọn từng hoạt động, và **được dán ⭐ khi hoàn thành**. Hai hoạt động đầu là **Phòng lồng tiếng**: trẻ xem hoạt hình, luyện từng câu, rồi **tự lồng tiếng và ghi hình** để có video nhân vật gốc với giọng của chính mình.

Bài: *Magic Marker – Episode 29: What Do You Do on Tuesdays? / 你每个星期二做什么？* (Little Fox).

## 📚 7 hoạt động

1. 🃏 **Flashcards** (Wordwall)
2. 🀄 **Chinese vs Pinyin** (Wordwall)
3. ✏️ **Quiz** (Wordwall)
4. 🧩 **Unjumble** (Wordwall)
5. ✍️ **Let's Write** (trang web nhúng)
6. 🎬 **Listen & Repeat — English** — Phòng lồng tiếng tiếng Anh
7. 🎙️ **Listen & Repeat — Chinese** — Phòng lồng tiếng tiếng Trung (có pinyin)

> Trong **hai phòng lồng tiếng** có sẵn **bảng từ vựng** ngay dưới video, kèm nút loa 🔊 đọc cả tiếng Anh và tiếng Trung. Âm thanh dùng giọng đọc sẵn của trình duyệt/thiết bị (không cần file mp3). Muốn nghe tiếng Trung, thiết bị cần có giọng đọc tiếng Trung — hầu hết điện thoại/máy tính đời mới đều có sẵn.

Có **nút Trang chủ**, thanh **tab trượt ngang** để chuyển qua lại, **tự đánh dấu hoàn thành** (✓/✅), thanh **tiến trình ⭐**, màn **ăn mừng 🏆** khi đủ 7 mục, và nút **Đặt lại tiến trình** cho học sinh mới.

## 📁 Các file cần tải lên (để chung một chỗ)

```
unit4/
├── index.html          # Trang chủ (hub 7 hoạt động)
├── dub-english.html    # Phòng lồng tiếng tiếng Anh
├── dub-chinese.html    # Phòng lồng tiếng tiếng Trung
├── README.md
├── english.mp4         # Video lồng tiếng (EN)
├── english-mau.mp3     # Âm thanh gốc có giọng đọc (EN) — cho nút "Nghe mẫu"
├── english-poster.jpg
├── chinese.mp4         # Video lồng tiếng (CN) — đã xoá giọng
├── chinese-mau.mp3     # Âm thanh gốc có giọng đọc (CN)
└── chinese-poster.jpg
```

> ⚠️ Phải giữ **đúng tên file** (phân biệt hoa/thường). Cả 10 file để cùng một thư mục gốc với `index.html`.

## 🚀 Đưa lên GitHub Pages

1. Tạo repository mới (ví dụ `unit4-my-hobbies`).
2. **Add file → Upload files**, kéo **tất cả 10 file** vào (giữ Ctrl để chọn nhiều), rồi **Commit changes**.
3. **Settings → Pages → Source**: chọn **Deploy from a branch**, nhánh `main`, thư mục `/ (root)`, **Save**.
4. Đợi 1–2 phút, mở link `https://<tài-khoản>.github.io/unit4-my-hobbies/`.

> 🎥 **Micro & camera của phòng lồng tiếng chỉ chạy qua https** (GitHub Pages có sẵn). Mở file trực tiếp trên máy (`file://`) hoặc xem ở ô xem trước sẽ **không** ghi hình được, và video/trò chơi có thể bị chặn. Luôn mở bằng link GitHub Pages.
>
> Trong phòng lồng tiếng có nút **"⛶ Mở toàn màn hình"** — nên dùng khi ghi hình để thoải mái nhất.

## ⚠️ Hai điều nên biết

1. **Video tiếng Anh chưa xoá hẳn giọng đọc.** File `english_no_vocal` cô gửi vẫn còn tiếng người dẫn (bản xuất chưa tách giọng). Phòng lồng tiếng vẫn chạy tốt (đã hạ nhỏ tiếng nền khi ghi), nhưng sẽ nghe thoáng giọng gốc phía sau. Muốn sạch hẳn: xuất lại video tiếng Anh đã **Remove vocal** (CapCut) rồi thay file `english.mp4`. Bản **tiếng Trung đã xoá giọng sạch** ✔.
2. **Thời điểm từng câu (timing) là ước lượng** từ hình trong video. Câu chữ và nghĩa thì chính xác; nếu thấy chữ vàng hiện hơi lệch so với lời, cô chỉnh 2 con số `s` (bắt đầu) và `e` (kết thúc) của câu đó trong `CUES` — xem mục dưới.

## ✏️ Chỉnh lời thoại / thời gian

Mở `dub-english.html` hoặc `dub-chinese.html`, tìm `const CUES=[ ... ]` gần cuối. Mỗi câu:

```js
{en:"Sue: I play soccer.", vi:"Sue: Cháu chơi bóng đá.", s:21.2, e:23.4}
// tiếng Trung có thêm pinyin:
{en:"苏：我踢足球。", py:"Sū: Wǒ tī zúqiú.", vi:"Sue: Cháu chơi bóng đá.", s:22.6, e:25.2}
```

`s` = giây bắt đầu nói, `e` = giây kết thúc (xem theo đồng hồ của video). `vi` là nghĩa tiếng Việt hiện làm phụ đề.

### Đổi bài khác
Trong `dub-*.html`, sửa `VIDEO_SRCS` (video đã xoá giọng), `MODEL_SRCS` (âm thanh gốc có giọng), `POSTER_SRCS` (ảnh bìa), tiêu đề `<title>`/`<h1>`, và danh sách `CUES`.

## 🔗 Nội dung nhúng của các trò chơi

| Hoạt động | Nguồn |
|-----------|-------|
| Flashcards | Wordwall `117264/003/417` |
| Chinese vs Pinyin | Wordwall `117264/127/539` |
| Quiz | Wordwall `117264/676/363` |
| Unjumble | Wordwall `120031/273/989` |
| Let's Write | https://1907010302-design.github.io/canopyu4l1/ |

Muốn đổi: mở `index.html`, sửa danh sách `CATS` ở gần cuối. Với Wordwall/link dán **cả link nhúng**; với phòng lồng tiếng để nguyên `type:'dub'` và tên file `.html`.

## 🎓 Hướng dẫn cho học sinh (phòng lồng tiếng)

1. Tab **🔊 Nghe bài mẫu**: xem cả câu chuyện; bấm từng câu để nghe lại cho thuộc.
2. Sang tab **🎥 Ghi hình**, bấm **Cho phép** khi trình duyệt hỏi camera & micro. 🎧 Nên đeo tai nghe.
3. Luyện từng câu: **Nghe mẫu → Thu âm → Nghe giọng em**. Chọn **🎭 Mặt nạ** nếu thích.
4. Bấm **🎥 Bắt đầu ghi hình**, nói theo khi chữ chuyển **vàng** cho tới hết bài.
5. **▶ Xem lại** → ưng thì **⬇ Tải video về** nộp cho cô, chưa ưng thì **🔁 Ghi lại**.

## 📌 Ghi chú kỹ thuật

- Tiến trình lưu bằng `localStorage`, khóa riêng `progress_u4_lesson1_v1` (không đè lên các bài khác).
- Phòng lồng tiếng dùng HTML/CSS/JS thuần: Web Audio trộn giọng với nhạc nền, MediaRecorder ghi âm/ghi hình, Canvas ghép khung camera. Mặt nạ dùng MediaPipe (tải khi chọn lần đầu, cần mạng).
- Hình và tiếng thu được **không gửi đi đâu**, chỉ nằm trên máy của trẻ.
- Video © Little Fox Co., Ltd. — dùng cho mục đích học tập trong lớp.
