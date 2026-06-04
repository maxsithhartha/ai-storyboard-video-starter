# CHARACTER REFERENCE SHEET
**Project:** [Назва проекту]
**Версія:** [v1.0]
**Дата:** [YYYY-MM-DD]

---

## ІДЕНТИФІКАТОР

| Поле | Значення |
|---|---|
| **Ім'я персонажа** | |
| **ID стану** | [STATE-01 / базовий стан] |
| **Тригер зміни стану** | [що спричиняє зміну — сцена, подія] |
| **Попередній стан** | [посилання на попередній sheet або "перший"] |
| **Soul ID / Element ID** | [ID в Higgsfield, якщо є] |

> ⚠️ **ПРАВИЛО СТАНІВ:** Якщо у сцені персонаж змінює зовнішність (одяг, стан, вік, грим, травма) — створюється новий CHARACTER SHEET для кожного стану. Наступні шоти будуються ТІЛЬКИ з approved/-версії відповідного стану.

---

## 1. ФІЗИЧНИЙ ОПИС (IDENTITY LOCK)

```
Стать:
Вік (виглядає):
Зріст / статура:
Колір шкіри:
Форма обличчя:
Очі (колір, форма):
Ніс:
Губи:
Щелепа / підборіддя:
Вуха:
Брови (форма, колір):
Волосся (колір, довжина, стрижка, текстура):
Особливі риси (шрами, родимки, татуювання, пірсинг):
```

> 🎯 **Higgsfield Soul ID:** ці параметри = основа для тренування Soul ID (20+ фото різних ракурсів і виразів обличчя).

---

## 2. ОДЯГ І АКСЕСУАРИ (OUTFIT LOCK — стан: [STATE-XX])

```
Верхній одяг:
  - тип:
  - колір:
  - матеріал / текстура:
  - фасон / крій:
  - деталі (ґудзики, блискавки, принти):

Нижній одяг:
  - тип:
  - колір:
  - деталі:

Взуття:
  - тип:
  - колір:
  - підошва / підбор:

Аксесуари (перелік кожного окремо):
  - [ ] головний убір:
  - [ ] шарф / краватка:
  - [ ] сумка:
  - [ ] ремінь:
  - [ ] годинник:
  - [ ] ювелірні прикраси:
  - [ ] окуляри:
  - [ ] інше:

Стан одягу: [чистий / пом'ятий / брудний / пошкоджений]
```

---

## 3. ГРИМ І ВОЛОССЯ (MAKEUP & HAIR STATE)

```
Зачіска: [укладка / вільно / зібрано / інше]
Стан волосся: [чисте / мокре / розтріпане / інше]
Грим: [натуральний / вечірній / без гриму / театральний]
Спецефекти гриму: [немає / синці / порізи / бруд / кров / вік]
```

---

## 4. ЕМОЦІЙНА ПАЛІТРА (PER-CHARACTER EMOTIONS)

Для кожної сцени визначається поточна емоція. Нижче — повна палітра для референсних фреймів:

| Емоція | Опис для промпту | Використовується в шоті |
|---|---|---|
| Нейтральний | relaxed, neutral expression, soft focus | |
| Радість | genuine smile, raised cheekbones, bright eyes | |
| Задоволення | subtle smile, relaxed posture, confident | |
| Здивування | raised eyebrows, wide eyes, open mouth slightly | |
| Страх | tense jaw, wide eyes, slight head back | |
| Гнів | furrowed brow, tight jaw, intense stare | |
| Смуток | downturned eyes, slight frown, heavy eyelids | |
| Зосередженість | squinted eyes, forward lean, tight lips | |
| Сумнів | one raised eyebrow, head tilt, pressed lips | |
| Вичерпаність | heavy eyelids, slightly open mouth, drooped posture | |

---

## 5. РЕФЕРЕНСНІ ФРЕЙМИ (IMAGE REFERENCE SET)

> 🖼️ **Дефолтна модель генерації:** GPT Image 2. Замінюється тільки за явним запитом.

### 5.1 Turnaround Sheet (повнофігурний обертання — A-pose)
```
Генерується: GPT Image 2
Prompt-шаблон:

"Create a professional character reference sheet based strictly on 
the uploaded reference image. Clean neutral background. Technical 
model turnaround. Exact realistic visual style of the reference.
Top row (4 panels): full-body standing — front, left profile, 
right profile, back. A-pose, consistent scale, accurate anatomy.
Bottom row (3 panels): close-up portraits — front, left profile, 
right profile. Consistent lighting across all panels. 
Ultra-realistic, print-ready reference sheet."

Файли:
  attempts/ → [ім'я]-turnaround-v01.png, v02.png...
  approved/ → [ім'я]-turnaround-FINAL.png
```

### 5.2 Portrait Sheet (крупні плани + емоції)
```
Генерується: GPT Image 2
Prompt-шаблон:

"Professional portrait reference sheet of [character description].
Clean neutral background. Grid layout 3×3. Nine emotional states:
neutral, joy, anger, fear, sadness, surprise, focus, doubt, 
exhaustion. Each panel: ECU (extreme close-up), consistent identity,
consistent lighting, consistent outfit. Print-ready."

Файли:
  attempts/ → [ім'я]-emotions-v01.png
  approved/ → [ім'я]-emotions-FINAL.png
```

### 5.3 Action / Motion Sheet (пози в русі)
```
Генерується: GPT Image 2
Описуються ключові рухи персонажа у сценарії.

Prompt-шаблон:
"Action reference sheet of [character]. Clean background. 
Grid 2×3. Poses: walking front, walking side, running, 
reaching, sitting, standing confident. Same character, 
same outfit, same lighting across all panels."

Файли:
  attempts/ → [ім'я]-action-v01.png
  approved/ → [ім'я]-action-FINAL.png
```

### 5.4 Outfit Detail Sheet (деталі одягу і аксесуарів)
```
Генерується: GPT Image 2

"Outfit detail reference sheet for [character name]. 
White studio background. Flat lay and worn views.
Panel 1: full outfit flat lay. Panel 2: front torso close-up 
showing fabric texture and details. Panel 3: accessories 
close-up (watch/bag/belt/etc). Panel 4: shoes close-up."

Файли:
  attempts/ → [ім'я]-outfit-detail-v01.png
  approved/ → [ім'я]-outfit-detail-FINAL.png
```

---

## 6. ПРАВИЛА ЄДИНОМАНІТНОСТІ (CONSISTENCY RULES)

```
✅ ЗАВЖДИ зберігати:
- [деталь 1, напр. "шрам на лівій щоці"]
- [деталь 2, напр. "годинник на правому зап'ясті"]
- [деталь 3, напр. "специфічний відтінок волосся"]

❌ НІКОЛИ не змінювати без нового STATE sheet:
- колір / стрижка волосся
- ключові аксесуари
- характерні риси обличчя

📌 Negative prompt (додавати до всіх шотів):
"no face morph, no identity drift, no extra fingers, 
no floating objects, no costume change, stable features"
```

---

## 7. СТАТУС АРКУШУ

| Статус | Дата | Автор |
|---|---|---|
| ☐ Draft | | |
| ☐ Reviewed | | |
| ☐ **APPROVED** ✅ | | |

> Наступний шот генерується тільки після APPROVED.
