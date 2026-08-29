# English Voice Practice — Question Bank (v1)

Ngân hàng câu hỏi cho **AI Voice Conversation Practice Module** (Beginner & Intermediate), sinh theo đúng cấu trúc tham khảo trong `Database_tieng_anh_mau.md` và các domain/sub-topic mô tả trong `AI_VOICE_CONVERSATION_MODULE.md`.

- `beginner_questions_100.json` — 100 câu (A1/A2)
- `intermediate_questions_100.json` — 100 câu (B1/B2)

> Bản đầy đủ **250 câu/level (500 câu tổng)** đã được gửi trực tiếp cho anh Khoa qua chat (không đưa lên GitHub để tránh file quá nặng khi thao tác). Bộ 100/100 trên GitHub là tập con được lọc đều theo sub-topic từ đúng bộ 250 câu đó — không phải nội dung khác.

## Phân bổ theo topic / sub-topic (mỗi level, trên tổng 100 câu)

| Topic | Sub-topic | Số câu |
|---|---|---|
| Office/Business English | Asking for Leave | 9 |
| Office/Business English | Meeting Clients | 9 |
| Office/Business English | Team Meetings | 9 |
| Office/Business English | Giving Updates | 9 |
| Office/Business English | Job Interviews | 8 |
| Office/Business English | Presentations | 8 |
| Daily Conversation | Greetings | 8 |
| Daily Conversation | Ordering Food | 8 |
| Daily Conversation | Shopping | 8 |
| Daily Conversation | Asking for Directions | 8 |
| Daily Conversation | Travel | 8 |
| Daily Conversation | Talking About Hobbies | 8 |
| **Total** | | **100** |

## Schema (mở rộng so với file mẫu)

```json
{
  "id": "B_OFF_LEAVE_001",
  "level": "Beginner | Intermediate",
  "topic": "Office/Business English | Daily Conversation",
  "sub_topic": "string",
  "difficulty_tier": "A1 | A2 | B1 | B2",
  "ai_question": "Câu AI hỏi để mở đầu/tiếp tục hội thoại",
  "sample_pattern": "Câu trả lời mẫu cho người học tham khảo",
  "keywords": ["từ khoá kỳ vọng xuất hiện trong câu trả lời tốt — dùng để chấm relevance nhanh, không cần gọi AI mỗi câu"],
  "common_mistakes": ["lỗi thường gặp ứng với câu này — giúp AI bắt lỗi chuẩn và nhanh hơn"],
  "follow_up_question": "Câu hỏi nối tiếp tự nhiên — hỗ trợ hội thoại multi-turn thay vì hỏi-đáp rời rạc",
  "grammar_explanation_en": "Giải thích ngắn gọn bằng tiếng Anh",
  "grammar_explanation_vi": "Giải thích ngắn gọn bằng tiếng Việt"
}
```

Beginner tập trung lỗi ngữ pháp cơ bản (to be, thì, mạo từ, số ít/số nhiều, giới từ...). Intermediate tập trung collocation, idiom, professional phrasing, natural expression — đúng tinh thần Part 2 của spec.

## Validate

Mỗi file đã được kiểm tra: không trùng `id`, không trùng `ai_question`, đủ 12 field bắt buộc, đúng số lượng 100/100, và mỗi entry được verify byte-for-byte (git blob SHA) sau khi push lên GitHub — đảm bảo không bị lỗi cắt/nhòe nội dung trong lúc upload.

## Ghi chú

Đây là bản v1 (lần đầu) — nội dung do AI soạn dựa trên schema mẫu, **cần anh Khoa review lại một lượt** trước khi đưa vào production (đặc biệt các câu B2 dùng idiom/collocation). Nếu muốn full 500 câu (250/250) trên GitHub thay vì bản rút gọn 100/100 này, báo em để em push thêm.
