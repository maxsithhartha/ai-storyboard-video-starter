# 02-REFERENCES — MASTER INDEX
**Project:** [Назва проекту]
**Оновлено:** [YYYY-MM-DD]

---

## ПРАВИЛО STAGE

```
attempts/    — чернетки sheets і референсні зображення
approved/    — затверджені sheets і фінальні зображення
disapproved/ — відхилені варіанти (зберігаємо — показують чого уникати)
```

**Наступний етап (03-shot-list/) будується ТІЛЬКИ з approved/.**

> 🖼️ **Дефолтна модель генерації зображень:** GPT Image 2. Замінюється тільки за явним запитом.

---

## СТРУКТУРА ПАПКИ

```
02-references/
├── INDEX.md                        ← цей файл
├── attempts/
│   └── [будь-які чернетки]
├── approved/
│   ├── characters/
│   │   ├── [ім'я]-STATE-01/
│   │   │   ├── CHARACTER_SHEET.md
│   │   │   ├── [ім'я]-turnaround-FINAL.png
│   │   │   ├── [ім'я]-emotions-FINAL.png
│   │   │   ├── [ім'я]-action-FINAL.png
│   │   │   └── [ім'я]-outfit-detail-FINAL.png
│   │   └── [ім'я]-STATE-02/       ← якщо є зміна стану
│   ├── locations/
│   │   ├── [location]-STATE-01/
│   │   │   ├── LOCATION_SHEET.md
│   │   │   ├── [location]-five-view-FINAL.png
│   │   │   ├── [location]-timeofday-FINAL.png
│   │   │   └── [location]-details-FINAL.png
│   │   └── [location]-STATE-02/
│   └── objects/
│       ├── [object]-STATE-01/
│       │   ├── OBJECT_SHEET.md
│       │   ├── [object]-turnaround-FINAL.png
│       │   └── [object]-in-context-FINAL.png
│       └── [object]-STATE-02/
└── disapproved/
    └── [відхилені варіанти]
```

---

## РЕЄСТР ПЕРСОНАЖІВ

| ID | Ім'я | Стан | Soul ID | Аркуш | Статус |
|---|---|---|---|---|---|
| CHAR-01 | | STATE-01 | | characters/[ім'я]-STATE-01/ | ☐ |
| CHAR-01 | | STATE-02 | | characters/[ім'я]-STATE-02/ | ☐ |
| CHAR-02 | | STATE-01 | | | ☐ |

---

## РЕЄСТР ЛОКАЦІЙ

| ID | Назва | Стан | Сцени | Аркуш | Статус |
|---|---|---|---|---|---|
| LOC-01 | | STATE-01 (день) | | locations/[name]-STATE-01/ | ☐ |
| LOC-01 | | STATE-02 (ніч) | | locations/[name]-STATE-02/ | ☐ |
| LOC-02 | | STATE-01 | | | ☐ |

---

## РЕЄСТР ОБ'ЄКТІВ

| ID | Назва | Категорія | Стан | Власник | Аркуш | Статус |
|---|---|---|---|---|---|---|
| OBJ-01 | | hero prop | STATE-01 | CHAR-01 | objects/[name]-STATE-01/ | ☐ |
| OBJ-01 | | hero prop | STATE-02 (зламаний) | | objects/[name]-STATE-02/ | ☐ |

---

## КОНТРОЛЬНІ ПИТАННЯ (APPROVAL GATE)

Перед переходом до `03-shot-list/` перевірити:

- [ ] Кожен персонаж, що з'являється у сценарії, має затверджений CHARACTER SHEET
- [ ] Для кожної зміни стану персонажа є окремий аркуш
- [ ] Кожна ключова локація має затверджений LOCATION SHEET
- [ ] Для кожної зміни стану локації є окремий аркуш
- [ ] Кожен hero prop має затверджений OBJECT SHEET
- [ ] Усі turnaround sheets затверджені
- [ ] Усі emotion sheets затверджені
- [ ] Soul ID / Elements зареєстровані в Higgsfield (якщо потрібно)
- [ ] Негативні промпти прописані для кожного персонажа / локації

> **Контрольне питання:** "Це ті референси, які ми фіксуємо? Чи є зміни стану, які ми пропустили?"

---

## СТАТУС STAGE

| | |
|---|---|
| **Загальний статус** | ☐ В роботі / ☐ **APPROVED** ✅ |
| **Дата затвердження** | |
