# **XÂY DỰNG CHUỖI PROMPT VIẾT BÀI PR SẢN PHẨM CÔNG NGHỆ**

## **1\. Tổng quan quy trình Prompt Chaining**

Prompt Chaining là kỹ thuật chia một nhiệm vụ lớn thành nhiều nhiệm vụ nhỏ. Kết quả của bước trước sẽ được sử dụng làm dữ liệu đầu vào cho bước tiếp theo.

Quy trình gồm 3 bước:

**PROMPT 1: NGHIÊN CỨU KHÁCH HÀNG**

Xác định đối tượng mục tiêu và nỗi đau khách hàng (Pain Points)

Output 1 → Input 2

**PROMPT 2: XÂY DỰNG DÀN Ý**

Tạo Outline chi tiết dựa trên kết quả nghiên cứu

Output 2 → Input 3

**PROMPT 3: VIẾT BÀI PR VÀ SEO**

Triển khai bài viết 1.000–1.500 từ, tối ưu SEO

## **2\. Thiết kế 3 Prompt thành phần**

### **Prompt 1: Nghiên cứu khách hàng mục tiêu**

**Mục tiêu:** Xác định khách hàng tiềm năng và những vấn đề mà AI Chatbot có thể giải quyết.

**PROMPT 1: NGHIÊN CỨU KHÁCH HÀNG**

Bạn là chuyên gia nghiên cứu thị trường trong lĩnh vực công nghệ và AI.

Bối cảnh: Doanh nghiệp chuẩn bị ra mắt sản phẩm AI Chatbot hỗ trợ tự động trả lời khách hàng, tư vấn sản phẩm và chăm sóc khách hàng 24/7.

Yêu cầu:

1. Xác định nhóm khách hàng mục tiêu.  
2. Phân tích nhu cầu và hành vi của từng nhóm khách hàng.  
3. Liệt kê ít nhất 5 Pain Points (nỗi đau) mà khách hàng thường gặp.  
4. Đề xuất cách AI Chatbot giải quyết từng vấn đề.  
5. Xác định lợi ích nổi bật mà sản phẩm mang lại.

Định dạng đầu ra JSON gồm:  
{  
"target\_audience": \[\],  
"customer\_needs": \[\],  
"pain\_points": \[\],  
"solutions": \[\],  
"key\_benefits": \[\]  
}

Không tự đưa ra số liệu thị trường nếu không có nguồn xác thực. Kết quả này sẽ được sử dụng làm đầu vào bắt buộc cho Prompt 2\.

**Output 1 dự kiến:**

* Khách hàng mục tiêu: Doanh nghiệp vừa và nhỏ, cửa hàng trực tuyến, bộ phận chăm sóc khách hàng.  
* Pain Points:  
  * Khách hàng phải chờ lâu để được phản hồi.  
  * Nhân viên chăm sóc khách hàng quá tải.  
  * Chi phí vận hành cao.  
  * Khó hỗ trợ khách hàng ngoài giờ làm việc.  
  * Thông tin tư vấn chưa đồng nhất.  
* Giải pháp: AI Chatbot tự động phản hồi, hỗ trợ 24/7 và cung cấp thông tin nhất quán.

  ### **Prompt 2: Xây dựng dàn ý bài PR**

**Mục tiêu:** Sử dụng kết quả nghiên cứu từ Prompt 1 để xây dựng dàn ý logic, tránh trùng lặp nội dung.

**PROMPT 2: XÂY DỰNG OUTLINE**

Bạn là chuyên gia Content Marketing và SEO.

Dữ liệu đầu vào:  
\[ DÁN TOÀN BỘ OUTPUT CỦA PROMPT 1 VÀO ĐÂY \]

Nhiệm vụ:  
Dựa hoàn toàn trên dữ liệu nghiên cứu ở trên, hãy xây dựng dàn ý chi tiết cho bài PR giới thiệu sản phẩm AI Chatbot dành cho doanh nghiệp.

Yêu cầu:

1. Đề xuất tiêu đề thu hút.  
2. Viết đoạn mở đầu đánh đúng Pain Points của khách hàng.  
3. Xây dựng các tiêu đề H2 và H3 theo trình tự logic.  
4. Làm rõ lợi ích, tính năng và giải pháp của sản phẩm.  
5. Bổ sung phần so sánh phương pháp chăm sóc khách hàng truyền thống với AI Chatbot nhưng không tự bịa số liệu.  
6. Xây dựng CTA ở cuối bài.  
7. Đề xuất từ khóa SEO chính và từ khóa phụ.

Cấu trúc đầu ra:  
{  
"headline": "",  
"lead": "",  
"outline": \[\],  
"primary\_keyword": "",  
"secondary\_keywords": \[\],  
"cta": "",  
"tone": "Chuyên nghiệp, tin cậy"  
}

Đảm bảo dàn ý phù hợp với bài viết PR dài 1.000–1.500 từ. Kết quả này sẽ là đầu vào bắt buộc cho Prompt 3\.

**Output 2 dự kiến:**

* Headline: AI Chatbot – Giải pháp nâng cao hiệu quả chăm sóc khách hàng cho doanh nghiệp.  
* Lead: Giới thiệu vấn đề doanh nghiệp thường gặp khi chăm sóc khách hàng.  
* H2: AI Chatbot là gì?  
* H2: Những khó khăn trong chăm sóc khách hàng hiện nay.  
* H2: Giải pháp AI Chatbot giúp doanh nghiệp thay đổi cách vận hành.  
  * H3: Tự động trả lời khách hàng 24/7.  
  * H3: Giảm tải công việc cho nhân viên.  
  * H3: Nâng cao trải nghiệm khách hàng.  
* H2: Lợi ích khi doanh nghiệp ứng dụng AI Chatbot.  
* H2: Cách triển khai AI Chatbot hiệu quả.  
* CTA: Liên hệ doanh nghiệp để tìm hiểu và trải nghiệm giải pháp.

  ### **Prompt 3: Viết bài PR hoàn chỉnh và tối ưu SEO**

**Mục tiêu:** Triển khai dàn ý thành bài PR chuyên sâu, có nội dung thống nhất và tối ưu công cụ tìm kiếm.

**PROMPT 3: VIẾT BÀI PR VÀ TỐI ƯU SEO**

Bạn là chuyên gia Content Marketing, SEO và Copywriting trong lĩnh vực công nghệ.

Dữ liệu đầu vào:

1. Kết quả nghiên cứu khách hàng:  
   \[ DÁN OUTPUT CỦA PROMPT 1 \]  
2. Dàn ý bài viết:  
   \[ DÁN OUTPUT CỦA PROMPT 2 \]

Nhiệm vụ:  
Triển khai thành bài PR hoàn chỉnh giới thiệu sản phẩm AI Chatbot dành cho doanh nghiệp.

Yêu cầu nội dung:

* Độ dài từ 1.000–1.500 từ.  
* Có tiêu đề Headline thu hút.  
* Có đoạn mở đầu Lead hấp dẫn, giải quyết Pain Points.  
* Sử dụng đầy đủ các tiêu đề H2, H3 theo đúng dàn ý.  
* Phân tích rõ tính năng và lợi ích sản phẩm.  
* Tích hợp từ khóa SEO chính và từ khóa phụ tự nhiên.  
* Có CTA rõ ràng ở cuối bài.

Quy tắc nhất quán:

* Giữ giọng văn chuyên nghiệp, tin cậy trong toàn bộ bài viết.  
* Không lặp ý hoặc tự ý thay đổi dàn ý.  
* Không tự bịa thông tin, tính năng hoặc số liệu sản phẩm.  
* Các phần phải liên kết logic với nhau.

Quy tắc xử lý khi bị ngắt giữa chừng:

* Ghi nhớ tiêu đề, dàn ý, từ khóa và phần nội dung đã hoàn thành.  
* Lưu lại tiêu đề H2/H3 đang viết và câu cuối cùng đã hoàn thành.  
* Khi người dùng yêu cầu tiếp tục, phải viết nối tiếp ngay sau câu cuối cùng.  
* Không viết lại nội dung cũ, không lặp lại tiêu đề hoặc đoạn văn đã hoàn thành.  
* Giữ nguyên giọng văn và cấu trúc ban đầu.

Hãy xuất bài viết theo định dạng Markdown, sau đó kiểm tra lại độ dài, từ khóa SEO, tính nhất quán và CTA.

## **3\. Xử lý khi AI bị ngắt giữa chừng (Max Token)**

Khi AI đang viết bài dài nhưng bị dừng đột ngột, cần sử dụng câu lệnh điều khiển để tiếp tục nội dung mà không làm mất ngữ cảnh.

**Prompt tiếp tục viết:**

Hãy tiếp tục viết bài PR từ chính xác vị trí đã dừng ở câu trước đó.

Yêu cầu:

* Không viết lại nội dung đã hoàn thành.  
* Không lặp lại tiêu đề hoặc đoạn văn cũ.  
* Tiếp tục đúng phần H2/H3 còn dang dở.  
* Giữ nguyên giọng văn chuyên nghiệp, tin cậy.  
* Đảm bảo nội dung liên kết tự nhiên với phần trước.  
* Tiếp tục sử dụng các từ khóa SEO đã thống nhất.  
* Hoàn thành các phần còn lại và CTA cuối bài.

Câu cuối cùng đã hoàn thành: \[DÁN CÂU CUỐI CÙNG VÀO ĐÂY\]

Phần tiếp theo cần viết: \[TÊN H2/H3 TIẾP THEO\]

## **4\. Bảng tổng hợp quy trình truyền dữ liệu**

| Giai đoạn | Đầu vào | Đầu ra |
| ----- | ----- | ----- |
| Prompt 1 | Thông tin sản phẩm | Khách hàng, Pain Points, lợi ích |
| Prompt 2 | Output 1 | Headline, Outline, từ khóa SEO |
| Prompt 3 | Output 1 \+ Output 2 | Bài PR hoàn chỉnh |
| Tiếp tục | Nội dung đã viết và vị trí dừng | Phần bài viết còn thiếu |

## **5\. Kiểm tra kết quả cuối cùng**

**Checklist kiểm tra bài PR**

0/8 hoàn thành

Bài viết có độ dài 1.000–1.500 từ.

Có Headline và Lead hấp dẫn.

Có đầy đủ tiêu đề H2, H3 theo dàn ý.

Nội dung giải quyết đúng Pain Points.

Từ khóa SEO được sử dụng tự nhiên.

Giọng văn chuyên nghiệp, tin cậy xuyên suốt.

Có CTA rõ ràng ở cuối bài.

Không lặp nội dung khi tiếp tục sau Max Token.

## **6\. Kết luận**

Kỹ thuật Prompt Chaining giúp chia nhiệm vụ viết bài PR thành 3 giai đoạn: nghiên cứu khách hàng, xây dựng dàn ý và triển khai nội dung. Việc truyền dữ liệu giữa các prompt giúp AI duy trì ngữ cảnh, hạn chế lặp ý và đảm bảo chất lượng bài viết. Đồng thời, câu lệnh tiếp tục viết giúp xử lý tình trạng ngắt quãng mà không làm thay đổi giọng văn hoặc cấu trúc bài viết.

