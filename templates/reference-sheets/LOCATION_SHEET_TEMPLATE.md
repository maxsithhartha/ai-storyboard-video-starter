# LOCATION REFERENCE SHEET
**Project:** [Назва проекту]
**Версія:** [v1.0]
**Дата:** [YYYY-MM-DD]

---

## ІДЕНТИФІКАТОР

| Поле | Значення |
|---|---|
| **Назва локації** | |
| **ID стану** | [STATE-01 / базовий стан] |
| **Тригер зміни стану** | [що змінює локацію — час доби, погода, пошкодження, інше] |
| **Попередній стан** | [посилання або "перший"] |
| **Сцени, де використовується** | [перелік шотів] |

> ⚠️ **ПРАВИЛО СТАНІВ:** День → ніч, чисто → після бійки, суха → дощова погода — кожен окремий STATE sheet. Наступні шоти будуються тільки з approved/-версії відповідного стану.

---

## 1. ОПИС ЛОКАЦІЇ (LOCATION LOCK)

```
Тип: [інтер'єр / екстер'єр / змішаний]
Загальна характеристика:
  - [напр. "занедбаний промисловий склад 1960-х"]
  - [напр. "сучасна квартира-студія у Kyiv, поверх 12"]

Розміри / масштаб: [тісний / середній / просторий / монументальний]
Час доби (у стані STATE-XX): [ранок / день / вечір / ніч]
Сезон / погода: [якщо екстер'єр]

Стиль / архітектура:
Стан / знос:
Унікальні структурні елементи:
```

---

## 2. КОЛЬОРОВА ПАЛІТРА І ОСВІТЛЕННЯ (PALETTE LOCK)

```
Домінантні кольори інтер'єру/екстер'єру:
  - стіни:
  - підлога:
  - меблі / обладнання:
  - акцентні кольори:

Джерела світла:
  - природне: [вікна / відсутнє]
  - штучне: [тип ламп, колір температури — warm/cool/mixed]
  - спецефекти: [неон, вогонь, блискавка, екрани]

Тіні: [м'які / різкі / специфічний напрямок]
Загальний тон: [warm / cool / desaturated / high-contrast / moody]
Кіно-референс (якщо є): [напр. "Blade Runner 2049 — orange-teal"]
```

---

## 3. КЛЮЧОВІ ЕЛЕМЕНТИ СЕРЕДОВИЩА

```
Постійні об'єкти (set dressing — не взаємодіють з персонажем):
  - [напр. "іржаві труби вздовж стелі"]
  - [напр. "побите скло у лівому куті"]
  - [напр. "стара неонова вивіска — не горить"]

Ключові props-зони (об'єкти, з якими взаємодіють):
  - Зона A: [назва і опис]
  - Зона B: [назва і опис]
  - Зона C: [назва і опис]

Звуковий характер: [тихо / шум вулиці / промисловий гул / інше]
Запах (для акторської підготовки): [не обов'язково]
```

---

## 4. КАМЕРНІ ЗОНИ (SHOOTING ZONES)

Попередньо визначені кути для шотів — щоб не "губити" локацію між сценами.

```
Зона CAM-A: [напр. "вхід — широкий план, камера на рівні пояса"]
Зона CAM-B: [напр. "центр — medium shot, камера фронтально"]
Зона CAM-C: [напр. "вікно — контровий світло, силует персонажа"]
Зона CAM-D: [напр. "стеля/POV — overhead, dramatic angle"]
```

---

## 5. РЕФЕРЕНСНІ ФРЕЙМИ (IMAGE REFERENCE SET)

> 🖼️ **Дефолтна модель генерації:** GPT Image 2. Замінюється тільки за явним запитом.

### 5.1 Five-View Location Sheet (Higgsfield стандарт)
```
Генерується: GPT Image 2
Prompt-шаблон:

"Create a professional location reference sheet based strictly 
on the uploaded reference image. Match exact visual style, 
lighting quality, color treatment, and texture.
Top row (4 panels): straight-on frontal view, left angled 
perspective, right angled perspective, reverse wide view.
Bottom row (3 panels): three detailed close-ups of key 
environmental elements.
Architectural consistency, accurate proportions, consistent 
lighting. Ultra-realistic, print-ready location sheet."

Файли:
  attempts/ → [location]-five-view-v01.png
  approved/ → [location]-five-view-FINAL.png
```

### 5.2 Time-of-Day Variants Sheet
```
Генерується: GPT Image 2
Якщо локація використовується в різний час доби.
Grid 1×3 або 1×4: same location — dawn / day / golden hour / night.

Prompt-шаблон:
"Location lighting variants sheet for [location description].
Four panels, identical framing and camera angle. Panel 1: dawn —
soft blue light. Panel 2: midday — harsh direct light. 
Panel 3: golden hour — warm orange. Panel 4: night — 
artificial light sources only, deep shadows."

Файли:
  attempts/ → [location]-timeofday-v01.png
  approved/ → [location]-timeofday-FINAL.png
```

### 5.3 Detail / Texture Sheet
```
Генерується: GPT Image 2

"Location detail reference sheet for [location]. 
White studio background. Grid 2×3.
Close-ups: floor texture, wall texture, main furniture surface,
key prop detail, lighting fixture, architectural detail."

Файли:
  attempts/ → [location]-details-v01.png
  approved/ → [location]-details-FINAL.png
```

### 5.4 State Comparison Sheet (якщо є зміна стану)
```
Генерується: GPT Image 2

"Location state comparison. Left panel: [STATE-01 опис]. 
Right panel: [STATE-02 опис]. Same framing, same camera angle.
Consistent architecture, only [що змінилось] differs."

Файли:
  attempts/ → [location]-state-comparison-v01.png
  approved/ → [location]-state-comparison-FINAL.png
```

---

## 6. ПРАВИЛА ЄДИНОМАНІТНОСТІ (CONSISTENCY RULES)

```
✅ ЗАВЖДИ зберігати:
- [деталь 1, напр. "тріщина у правій стіні"]
- [деталь 2, напр. "синя неонова вивіска у фоні"]
- [деталь 3, напр. "специфічний патерн підлоги"]

❌ НІКОЛИ не змінювати без нового STATE sheet:
- основне освітлення
- ключові структурні елементи
- кольорова температура

📌 Negative prompt (додавати до всіх шотів цієї локації):
"no location drift, no architectural change, consistent lighting,
no random new objects, no style shift"
```

---

## 7. СТАТУС АРКУШУ

| Статус | Дата | Автор |
|---|---|---|
| ☐ Draft | | |
| ☐ Reviewed | | |
| ☐ **APPROVED** ✅ | | |

> Наступний шот генерується тільки після APPROVED.
