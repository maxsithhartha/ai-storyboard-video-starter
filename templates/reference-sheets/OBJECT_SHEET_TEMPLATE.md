# OBJECT / PROP REFERENCE SHEET
**Project:** [Назва проекту]
**Версія:** [v1.0]
**Дата:** [YYYY-MM-DD]

---

## ІДЕНТИФІКАТОР

| Поле | Значення |
|---|---|
| **Назва об'єкта** | |
| **Категорія** | [prop / hero prop / set dressing / vehicle / weapon / device] |
| **ID стану** | [STATE-01 / базовий стан] |
| **Тригер зміни стану** | [що змінює об'єкт — пошкодження, відкрито/закрито, увімкнено, заряд] |
| **Сцени використання** | [перелік шотів] |
| **Персонаж-власник** | [хто взаємодіє] |
| **Element ID (Higgsfield)** | [ID елементу якщо збережено] |

> ⚠️ **ПРАВИЛО СТАНІВ:** Цілий → зламаний, закритий → відкритий, чистий → брудний = окремий STATE sheet.

> 📌 **PROP vs SET DRESSING:** Якщо персонаж бере об'єкт до рук або взаємодіє з ним — це **prop**, потребує окремого sheet. Якщо стоїть у фоні як атмосфера — set dressing, достатньо згадки у Location Sheet.

---

## 1. ФІЗИЧНИЙ ОПИС (OBJECT LOCK)

```
Тип / функція:
Форма: [геометрія, силует]
Розміри (відносні): [маленький / середній / великий / монументальний]
Масштаб відносно людини: [в долоні / ручна ноша / вище зросту / інше]

Матеріал:
  - основний: [метал / дерево / шкіра / пластик / тканина / скло / інше]
  - текстура: [гладка / шорстка / матова / глянцева / іржава / полірована]

Колір (стан STATE-XX):
  - основний:
  - деталі / акценти:
  - стан поверхні: [новий / потертий / пошкоджений / брудний]

Логотип / надписи / маркування: [так / ні — якщо так, описати точно]
Рухомі частини: [є / немає — якщо є, описати]
Світлові ефекти: [є / немає — кнопки, екрани, індикатори]
```

---

## 2. ДЕТАЛІЗАЦІЯ ДЛЯ ПРОМПТУ

```
Одна ключова фраза для ідентифікації в промпті:
  [напр. "worn leather briefcase with brass clasps and initials 'M.K.'"]

Що НЕ повинно мінятися між шотами:
  - [деталь 1]
  - [деталь 2]
  - [деталь 3]
```

---

## 3. РЕФЕРЕНСНІ ФРЕЙМИ (IMAGE REFERENCE SET)

> 🖼️ **Дефолтна модель генерації:** GPT Image 2. Замінюється тільки за явним запитом.

### 3.1 Product Turnaround Sheet (основний)
```
Генерується: GPT Image 2
Prompt-шаблон:

"Professional object reference sheet. Clean white or neutral 
studio background. Grid layout 2×3.
Top row: front view, side view (left or right), back view.
Bottom row: top view / overhead, 3/4 angled view, 
detail close-up of most distinctive feature.
Consistent studio lighting (soft box, no harsh shadows).
Ultra-realistic, print-ready product reference sheet.
Object: [детальний опис об'єкта]"

Файли:
  attempts/ → [object]-turnaround-v01.png
  approved/ → [object]-turnaround-FINAL.png
```

### 3.2 In-Context Sheet (об'єкт у руках / у сцені)
```
Генерується: GPT Image 2

"Object in context reference. Two panels.
Left: [object] held in human hand, medium shot, natural grip.
Right: [object] placed on [surface/location context].
Consistent object appearance, consistent lighting.
Object: [опис]"

Файли:
  attempts/ → [object]-in-context-v01.png
  approved/ → [object]-in-context-FINAL.png
```

### 3.3 State Comparison Sheet (якщо є зміна стану)
```
Генерується: GPT Image 2

"Object state comparison sheet. Left panel: STATE-01 — [опис стану].
Right panel: STATE-02 — [опис зміни, напр. 'shattered', 'open', 'bloodstained'].
Same framing, same angle, same lighting.
Object: [опис]"

Файли:
  attempts/ → [object]-states-v01.png
  approved/ → [object]-states-FINAL.png
```

### 3.4 Detail / Texture Sheet (для hero props)
```
Генерується: GPT Image 2

"Hero prop detail sheet. Grid 2×2.
Panel 1: macro close-up of primary distinguishing feature.
Panel 2: material texture close-up.
Panel 3: secondary detail (inscription / logo / mechanism).
Panel 4: wear and aging detail.
Ultra-sharp, print-ready."

Файли:
  attempts/ → [object]-details-v01.png
  approved/ → [object]-details-FINAL.png
```

---

## 4. ПРАВИЛА ВИКОРИСТАННЯ В ШОТАХ

```
Як тримати / носити: [у правій руці / через плече / в кишені / на столі]
Орієнтація в кадрі: [завжди лейблом до камери / ручкою вгору / інше]
Взаємодія: [персонаж бере / відкриває / кидає / стріляє / інше]

Negative prompt:
"no object change, no [specific detail] modification, 
consistent [material] texture, no logo distortion"
```

---

## 5. ХІГГСФІЛД — Element ID

```
Якщо об'єкт збережено як Element в Higgsfield:

Element ID: _______________
Сумісні моделі: GPT Image 2 / Nano Banana Pro / Seedream 4.5 / Cinema Studio 2.5
Placeholder у промпті: <<<[element-id]>>>
```

---

## 6. СТАТУС АРКУШУ

| Статус | Дата | Автор |
|---|---|---|
| ☐ Draft | | |
| ☐ Reviewed | | |
| ☐ **APPROVED** ✅ | | |

> Наступний шот генерується тільки після APPROVED.
