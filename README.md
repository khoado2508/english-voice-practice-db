# English Voice Practice — Question Bank (v1)

Ngân hàng câu hỏi cho **AI Voice Conversation Practice Module** (Beginner & Intermediate), sinh theo đúng cấu trúc tham khảo trong `Database_tieng_anh_mau.md` và các domain/sub-topic mô tả trong `AI_VOICE_CONVERSATION_MODULE.md`.

- `beginner_questions.json` — 250 câu (A1/A2)
- `intermediate_questions.json` — 250 câu (B1/B2)

## Phân bổ theo topic / sub-topic (mỗi level)

| Topic | Sub-topic | Số câu |
|---|---|---|
| Office/Business English | Asking for Leave | 21 |
| Office/Business English | Meeting Clients | 21 |
| Office/Business English | Team Meetings | 21 |
| Office/Business English | Giving Updates | 21 |
| Office/Business English | Job Interviews | 21 |
| Office/Business English | Presentations | 20 |
| Daily Conversation | Greetings | 21 |
| Daily Conversation | Ordering Food | 21 |
| Daily Conversation | Shopping | 21 |
| Daily Conversation | Asking for Directions | 21 |
| Daily Conversation | Travel | 21 |
| Daily Conversation | Talking About Hobbies | 20 |
| **Total** | | **250** |

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

Chạy `python3 gen.py` để tái sinh + validate: không trùng `id`, không trùng `ai_question`, đủ field bắt buộc, đúng số lượng 250/250.

## Ghi chú

Đây là bản v1 (lần đầu) — nội dung do AI soạn dựa trên schema mẫu, **cần anh Khoa review lại một lượt** trước khi đưa vào production (đặc biệt các câu B2 dùng idiom/collocation, và distribution 20-21 câu/sub-topic có thể điều chỉnh lại nếu muốn tỷ trọng khác).
