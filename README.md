# English Voice Practice — Question Bank (v1)

Ngan hang cau hoi cho **AI Voice Conversation Practice Module** (Beginner & Intermediate), sinh theo dung cau truc tham khao trong `Database_tieng_anh_mau.md` va cac domain/sub-topic mo ta trong `AI_VOICE_CONVERSATION_MODULE.md`.

## Xem / test truc tiep

App xem va luyen tap tuong tac (khong can tai file):

**https://khoado2508.github.io/english-voice-practice-db/**

App co 2 che do: Duyet danh sach (tim kiem, loc theo Level/Topic/Sub-topic, xem chi tiet tung cau) va Che do luyen tap (flashcard xao tron, an/hien dap an). Cau B2 (idiom/collocation nang cao) duoc danh dau mau do de uu tien review.

## File du lieu

- `beginner_questions_100.json` — 100 cau (A1/A2), duoc app o tren doc truc tiep
- `intermediate_questions_100.json` — 100 cau (B1/B2), duoc app o tren doc truc tiep
- `index.html` — app xem/luyen tap (GitHub Pages)

> Ban day du **250 cau/level (500 cau tong)** da duoc gui truc tiep cho anh Khoa qua chat va qua ban xem tuong tac rieng (Claude Artifact link), khong dua len GitHub de tranh file qua nang khi thao tac. Bo 100/100 tren GitHub Pages la tap con duoc loc deu theo sub-topic tu dung bo 250 cau do — khong phai noi dung khac. Neu muon doi ban GitHub Pages nay sang full 500 cau, bao lai de push them.

## Phan bo theo topic / sub-topic (moi level, tren tong 100 cau)

| Topic | Sub-topic | So cau |
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

## Schema (mo rong so voi file mau)

```json
{
  "id": "B_OFF_LEAVE_001",
  "level": "Beginner | Intermediate",
  "topic": "Office/Business English | Daily Conversation",
  "sub_topic": "string",
  "difficulty_tier": "A1 | A2 | B1 | B2",
  "ai_question": "Cau AI hoi de mo dau/tiep tuc hoi thoai",
  "sample_pattern": "Cau tra loi mau cho nguoi hoc tham khao",
  "keywords": ["tu khoa ky vong xuat hien trong cau tra loi tot"],
  "common_mistakes": ["loi thuong gap ung voi cau nay"],
  "follow_up_question": "Cau hoi noi tiep tu nhien",
  "grammar_explanation_en": "Giai thich ngan gon bang tieng Anh",
  "grammar_explanation_vi": "Giai thich ngan gon bang tieng Viet"
}
```

## Validate

Moi file da duoc kiem tra: khong trung `id`, khong trung `ai_question`, du 12 field bat buoc, dung so luong 100/100, va moi entry duoc verify byte-for-byte (git blob SHA) sau khi push len GitHub — dam bao khong bi loi cat/nhoe noi dung trong luc upload. `index.html` cung duoc verify byte-for-byte va test tai bang trinh duyet headless truoc khi push, xac nhan tai dung 200 cau va khong loi console.

## Ghi chu

Day la ban v1 (lan dau) — noi dung do AI soan dua tren schema mau, **can anh Khoa review lai mot luot** truoc khi dua vao production (dac biet cac cau B2 dung idiom/collocation). Neu muon full 500 cau (250/250) tren GitHub Pages thay vi ban rut gon 100/100 nay, bao em de em push them.
