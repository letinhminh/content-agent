---
name: brand-review
description: "Review nội dung đối chiếu với brand voice, style guide và trụ cột thông điệp, đánh dấu mức độ nghiêm trọng kèm gợi ý sửa cụ thể (trước/sau). Dùng khi kiểm tra bản nháp trước khi xuất bản, khi audit copy về nhất quán giọng điệu và thuật ngữ, hoặc khi rà soát tuyên bố không có căn cứ, thiếu disclaimer và các cờ pháp lý khác."
argument-hint: "<nội dung cần review>"
---

# Review thương hiệu (Brand Review)

Review nội dung marketing đối chiếu với brand voice, style guidelines và tiêu chuẩn thông điệp. Đánh dấu các điểm lệch và đưa gợi ý cải thiện cụ thể.

## Kích hoạt

Người dùng chạy `/brand-review` hoặc yêu cầu review, kiểm tra, audit nội dung đối chiếu với brand guidelines.

## Đầu vào

1. **Nội dung cần review** — nhận nội dung dưới dạng:
   - Dán trực tiếp vào cuộc trò chuyện
   - Đường dẫn file hoặc tham chiếu tới knowledge base (ví dụ: trang Notion, shared doc)
   - URL tới trang đã xuất bản
   - Nhiều nội dung để review hàng loạt

2. **Nguồn brand guidelines** (tự động xác định):
   - Nếu đã cấu hình brand style guide trong cài đặt local, dùng tự động
   - Nếu chưa cấu hình, hỏi: "Bạn có brand style guide hoặc hướng dẫn brand voice không? Bạn có thể dán nội dung, chia sẻ file, hoặc mô tả brand voice. Nếu không, tôi sẽ review chung về độ rõ ràng, nhất quán và chuyên nghiệp."

## Quy trình review

### Khi đã có Brand Guidelines

Đánh giá nội dung theo từng chiều sau:

#### Brand voice và tone
- Nội dung có khớp với các thuộc tính brand voice đã định nghĩa không?
- Tone có phù hợp với loại nội dung và đối tượng không?
- Có điểm lệch giọng điệu nào không nhất quán không?
- Đánh dấu câu hoặc cụm từ cụ thể bị lệch kèm giải thích vì sao

#### Thuật ngữ và ngôn ngữ
- Có dùng đúng các thuật ngữ brand ưu tiên không?
- Có xuất hiện thuật ngữ hoặc cụm từ "nên tránh" không?
- Mức độ chuyên môn (jargon) có phù hợp với đối tượng mục tiêu không?
- Tên sản phẩm, tên tính năng, thuật ngữ thương hiệu có đúng cách viết (viết hoa, định dạng) không?

#### Trụ cột thông điệp (Messaging pillars)
- Nội dung có khớp với các trụ cột thông điệp hoặc value proposition đã định nghĩa không?
- Tuyên bố có nhất quán với thông điệp đã duyệt không?
- Nội dung củng cố hay mâu thuẫn với định vị thương hiệu?

#### Tuân thủ style guide
- Ngữ pháp và dấu câu theo style guide (ví dụ: dấu phẩy Oxford, viết hoa đầu câu hay Title Case cho tiêu đề)
- Quy ước định dạng (tiêu đề, danh sách, in đậm/nhấn)
- Định dạng số, định dạng ngày
- Cách dùng acronym (có định nghĩa lần đầu tiên không)

### Khi chưa có Brand Guidelines (review chung)

Đánh giá nội dung theo:

#### Độ rõ ràng (Clarity)
- Thông điệp chính có rõ trong đoạn đầu tiên không?
- Câu có ngắn gọn, dễ hiểu không?
- Cấu trúc có logic, dễ theo dõi không?
- Có phát biểu mập mờ hoặc tham chiếu không rõ ràng không?

#### Nhất quán (Consistency)
- Tone có nhất quán trong toàn bộ nội dung không?
- Thuật ngữ có nhất quán không (không đổi qua lại giữa các từ đồng nghĩa cho cùng một khái niệm)?
- Định dạng có nhất quán không (tiêu đề, danh sách, viết hoa)?

#### Chuyên nghiệp (Professionalism)
- Nội dung có sạch lỗi chính tả, ngữ pháp, câu chữ lủng củng không?
- Tone có phù hợp với đối tượng mục tiêu không?
- Tuyên bố có được hậu thuẫn hoặc có căn cứ không?

### Cờ pháp lý và tuân thủ (luôn kiểm tra)

Bất kể đã cấu hình guidelines hay chưa, luôn đánh dấu:
- **Tuyên bố không có căn cứ** — tính từ nhất ("tốt nhất", "nhanh nhất", "duy nhất") không có bằng chứng đi kèm
- **Thiếu disclaimer** — tuyên bố về tài chính, sức khỏe, hoặc cam kết có thể cần disclaimer pháp lý
- **Tuyên bố so sánh** — so sánh với đối thủ có thể bị thách thức
- **Ngôn ngữ pháp lý** — nội dung có thể cần review pháp lý (dịch vụ tài chính, y tế...)
- **Vấn đề testimonial** — quote hoặc đánh giá không có nguồn hoặc không công bố quan hệ
- **Vấn đề bản quyền** — nội dung dường như diễn giải lại quá sát từ nguồn khác

## Tài liệu brand voice tham khảo

Dùng các framework này để đánh giá nội dung đối chiếu với tiêu chuẩn thương hiệu hoặc giúp người dùng xây dựng brand voice.

### Framework tài liệu brand voice

Một tài liệu brand voice đầy đủ nên bao phủ các lĩnh vực sau:

1. **Brand personality** — Định nghĩa thương hiệu như một con người. Ví dụ: "Nếu thương hiệu của chúng ta là một con người, đó sẽ là đồng nghiệp am hiểu, giải thích điều phức tạp đơn giản, thật lòng ăn mừng thắng lợi của bạn và không bao giờ tỏ ra bề trên."
2. **Thuộc tính brand voice** — 3-5 thuộc tính định nghĩa cách thương hiệu giao tiếp, mỗi thuộc tính gồm: ý nghĩa thực tế, ý nghĩa "không phải" (để tránh hiểu lầm), và ví dụ.
3. **Nhận thức đối tượng** — thương hiệu nói với ai (chính và phụ), họ quan tâm gì, trình độ chuyên môn, và cách họ muốn được xưng hô.
4. **Trụ cột thông điệp cốt lõi** — 3-5 chủ đề chính thương hiệu luôn truyền đạt, thứ bậc các thông điệp, và cách mỗi trụ cột gắn với nhu cầu đối tượng.
5. **Phổ tone (Tone spectrum)** — giọng điệu thay đổi thế nào qua các bối cảnh nhưng vẫn nhận ra là cùng một thương hiệu.
6. **Quy tắc style** — quy tắc ngữ pháp, định dạng và ngôn ngữ cụ thể.
7. **Thuật ngữ** — danh sách thuật ngữ ưu tiên và cần tránh.

### Phổ thuộc tính voice

Khi định nghĩa hoặc đánh giá brand voice, định vị các thuộc tính trên phổ:

| Phổ | Một cực | Cực còn lại |
|----------|---------|-------------|
| Độ trang trọng | Trang trọng, có tổ chức | Thân mật, gần gũi |
| Thẩm quyền | Chuyên gia, có thẩm quyền | Bình đẳng, cộng tác |
| Cảm xúc | Ấm áp, đồng cảm | Trực tiếp, thẳng thắn |
| Độ phức tạp | Kỹ thuật, chính xác | Đơn giản, dễ hiểu |
| Năng lượng | Táo bạo, sôi nổi | Bình tĩnh, đo lường |
| Hài hước | Vui nhộn, dí dỏm | Nghiêm túc, chân thành |
| Đổi mới | Đi đầu, nhìn xa | Đã được kiểm chứng, ổn định |

Với mỗi thuộc tính đã chọn, ghi theo format:

**[Tên thuộc tính]**
- **Chúng ta là**: [ý nghĩa thực tế]
- **Chúng ta không phải**: [hiểu lầm thường gặp cần tránh]
- **Nghe như**: [câu ví dụ thể hiện thuộc tính]
- **Không nghe như**: [câu ví dụ vi phạm thuộc tính]

Ví dụ:

**Gần gũi (Approachable)**
- **Chúng ta là**: thân thiện, rõ ràng, không chuyên môn sâu, chào đón cả người mới lẫn người có kinh nghiệm
- **Chúng ta không phải**: đơn giản hóa quá đà, quá thân mật, hoặc thiếu nội dung
- **Nghe như**: "Dưới đây là cách bắt đầu, chỉ mất khoảng 5 phút."
- **Không nghe như**: slang mạng, cợt nhả quá mức.

### Điều chỉnh tone theo kênh và bối cảnh

Brand voice giữ nhất quán, tone điều chỉnh theo bối cảnh. Tone là sắc thái cảm xúc áp lên voice.

#### Tone theo kênh

| Kênh | Điều chỉnh tone | Ví dụ |
|---------|----------------|---------|
| Blog | Cung cấp thông tin, gần gũi, giáo dục | "Hãy cùng nhau tìm hiểu cách này hoạt động và vì sao nó quan trọng với team bạn." |
| Social media (LinkedIn) | Chuyên nghiệp, gợi suy nghĩ, súc tích | "Ba điều chúng tôi rút ra từ 50 chiến dịch trong quý này." |
| Social media (X/Twitter) | Ngắn gọn, trực tiếp, đôi khi dí dỏm | "Landing page của bạn có 3 giây. Hãy tận dụng tốt." |
| Email marketing | Cá nhân, hữu ích, hướng hành động | "Chúng tôi đã chuẩn bị một thứ bạn có thể thấy hữu ích." |
| Sales collateral | Tự tin, nhấn vào lợi ích, cụ thể | "Team dùng nền tảng của chúng tôi giảm thời gian báo cáo 40%." |
| Tài liệu hỗ trợ | Rõ ràng, kiên nhẫn, từng bước | "Nếu gặp lỗi này, dưới đây là cách sửa." |
| Thông cáo báo chí | Trang trọng, thực tế | "Hôm nay công ty công bố ra mắt..." |
| Thông báo lỗi | Đồng cảm, hỗ trợ, không đổ blame | "Có sự cố ở phía chúng tôi. Đang kiểm tra." |

#### Tone theo tình huống

| Tình huống | Điều chỉnh tone |
|-----------|----------------|
| Ra mắt sản phẩm | Hào hứng, tự tin, hướng tới tương lai |
| Sự cố hoặc gián đoạn | Minh bạch, đồng cảm, có trách nhiệm |
| Câu chuyện thành công khách hàng | Ăn mừng, cụ thể, ghi nhận khách hàng |
| Thought leadership | Có thẩm quyền, sắc sảo, dựa trên bằng chứng |
| Onboarding | Chào đón, khích lệ, rõ ràng |
| Tin xấu (tăng giá, ngừng tính năng) | Trung thực, tôn trọng, hướng giải pháp |
| So sánh cạnh tranh | Tự tin nhưng công bằng, dựa trên fact, không disparaging |

#### Quy tắc điều chỉnh tone
Thuộc tính voice giữ cố định. Tone chỉnh lên/xuống theo bối cảnh. Ví dụ, thương hiệu "táo bạo và ấm áp":
- Khi ra mắt sản phẩm, đẩy mạnh táo bạo
- Khi phản hồi sự cố, đẩy mạnh ấm áp
- Cả hai thuộc tính không biến mất; chỉ thay đổi tỷ lệ

### Thực thi style guide

#### Ngữ pháp và cơ chế
Ghi và thực thi các lựa chọn nhất quán:

| Quy tắc | Lựa chọn | Ví dụ |
|---------|----------|-------|
| Dấu phẩy Oxford | Có / Không | "nhanh, tin cậy và an toàn" vs "nhanh, tin cậy, an toàn" |
| Viết hoa tiêu đề | Câu / Title Case | "Cách bắt đầu" vs "Cách Bắt Đầu" |
| Rút gọn (contractions) | Dùng / Tránh | "chúng tôi" vs cách rút gọn (áp dụng cho tiếng Anh: "we're" vs "we are") |
| Khoảng cách quanh gạch ngang em dash | Không / Có | "điều này – và hơn nữa" vs "điều này—và hơn nữa" |
| Số | Viết chữ 1-9, số 10+ / Luôn dùng số | "năm tính năng" vs "5 tính năng" |
| Phần trăm | % / chữ | "50%" vs "50 phần trăm" |
| Định dạng ngày | Tháng DD, YYYY / DD/MM/YYYY | "15/01/2025" hoặc "January 15, 2025" |
| Định dạng giờ | 12 giờ / 24 giờ | "15:00" vs "3:00 PM" |
| Danh sách | Có dấu chấm / Không | "Thiết lập tài khoản." vs "Thiết lập tài khoản" |

#### Quy ước định dạng
- Thứ bậc tiêu đề (khi nào dùng H1, H2, H3)
- Cách dùng in đậm và in nghiêng (đậm để nhấn, nghiêng cho tựa đề/thuật ngữ)
- Link text (mô tả rõ, không dùng "click here")
- Yêu cầu alt text cho hình ảnh
- Cách viết code (với thương hiệu kỹ thuật)
- Cách dùng callout hoặc hộp highlight

#### Dấu câu và nhấn mạnh
- Chính sách dấu chấm than (dùng ít, không bao giờ hơn 1)
- Dấu ba chấm (tránh trong hầu hết ngữ cảnh chuyên nghiệp)
- Chính sách viết hoa toàn bộ (tránh; dùng in đậm để nhấn)
- Cách dùng emoji theo kênh (kênh chuyên nghiệp: tối thiểu hoặc không có; social: phù hợp)

### Quản lý thuật ngữ

#### Thuật ngữ ưu tiên

Duy trì danh sách thuật ngữ ưu tiên và lựa chọn sai:

| Dùng | Không dùng | Ghi chú |
|------|-----------|---------|
| Đăng ký (động từ) | signup (động từ) | "signup" là dạng danh từ |
| Đăng nhập (động từ) | login (động từ) | "login" là danh từ/tính từ |
| Thiết lập (động từ) | setup (động từ) | "setup" là danh từ |
| Email | e-mail | Không có gạch ngang |
| Website | web site | Một từ |
| Dữ liệu (data) | data are (nếu không yêu cầu số nhiều) | Theo quy định của ấn phẩm |

#### Tên sản phẩm và tính năng
- Cách viết hoa chính thức cho tên sản phẩm
- Khi nào dùng tên sản phẩm đầy đủ vs viết tắt
- Có dùng "the" trước tên sản phẩm không
- Cách xử lý phiên bản trong copy
- Ký hiệu trademark (khi bắt buộc và khi bỏ qua)

#### Ngôn ngữ bao quát (Inclusive language)
- Dùng ngôn ngữ trung tính giới tính
- Tránh ngôn ngữ phân biệt khả năng ("crazy", "blind spot", "lame")
- Dùng người trước, khuyết tật sau ở nơi phù hợp
- Tránh thành ngữ đặc thù văn hóa khó dịch
- Dùng "đơn giản", "thẳng thắn" thay vì "dễ" (độ dễ tùy thuộc từng người)

#### Quản lý jargon ngành
- Định nghĩa thuật ngữ kỹ thuật nào đối tượng hiểu mà không cần giải thích
- Liệt kê jargon luôn phải định nghĩa hoặc thay bằng ngôn ngữ đơn giản
- Chỉ định acronym nào cần viết đầy đủ ở lần xuất hiện đầu tiên
- Bảng thuật ngữ theo đối tượng cho từ ngữ có nghĩa khác nhau với độc giả khác nhau

#### Thuật ngữ cạnh tranh và danh mục
- Cách gọi danh mục sản phẩm của bạn (dùng framework ưu tiên của bạn)
- Cách gọi đối thủ (theo tên hay chung chung)
- Thuật ngữ đối thủ đã tạo mà bạn nên tránh (để không củng cố định vị của họ)
- Ngôn ngữ phân biệt ưu tiên của bạn

## Format đầu ra

Trình bày review theo:

### Tóm tắt
- Đánh giá tổng thể: nội dung khớp với tiêu chuẩn thương hiệu đến mức nào (hoặc chất lượng tổng thể)
- 1-2 câu về điểm mạnh lớn nhất
- 1-2 câu về cải thiện quan trọng nhất

### Phát hiện chi tiết

Với mỗi vấn đề phát hiện, đưa:

| Vấn đề | Vị trí | Mức độ | Gợi ý |
|--------|--------|--------|-------|

Trong đó mức độ là:
- **Cao** — mâu thuẫn với brand voice, có rủi ro tuân thủ, hoặc làm suy yếu đáng kể thông điệp
- **Trung bình** — không nhất quán với guidelines nhưng chưa gây hại
- **Thấp** — vấn đề style nhỏ hoặc theo sở thích

### Các mục đã sửa

Với 3-5 vấn đề mức cao nhất, đưa bản trước/sau: nội dung gốc và gợi ý sửa.

### Cờ pháp lý/tuân thủ

Liệt kê riêng các vấn đề pháp lý hoặc tuân thủ kèm hành động đề xuất.

## Sau khi review

Hỏi: "Bạn muốn tôi:
- Sửa toàn bộ nội dung theo gợi ý này?
- Chỉ sửa các vấn đề mức cao?
- Review thêm nội dung khác theo cùng guidelines?
- Giúp bạn tài liệu hóa brand voice cho các lần review sau?"
