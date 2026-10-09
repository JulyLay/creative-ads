# Шаблони статичних креативів

Використовуй цей файл для генерації AI-промтів статичних рекламних зображень. Кожен шаблон адаптується під конкретний сегмент, біль і ступінь усвідомленості.

## 5 типів візуалів

### 1. Lifestyle (людина в ситуації)

**Коли використовувати:** Pain-agitate (ступені 0-1), Transformation (ступені 2-4), Trigger-moment (ступені 0-2)

**Структура промта:**
```
[Опис людини: вік, стать, зовнішність з ДНК-портрета], [дія/ситуація з больової ситуації ДНК], [локація: конкретне місце], [освітлення: відповідає емоції], [стиль: documentary/editorial/candid photography], [камера: Canon/Sony + об'єктив], [глибина різкості], [кольорова палітра: відповідає емоції], [настрій] --ar [за платформою] --v 6.1 --style raw --no text watermark logo
```

**Шаблон для болю (pain-agitate):**
```
A [вік]-year-old [стать] [дія з больової ситуації], [деталі оточення з ДНК], [емоційні деталі: вираз обличчя, поза], intimate documentary photography style, [камера] [об'єктив], shallow depth of field, [холодна/приглушена палітра], [настрій: melancholic/anxious/exhausted] --ar [ratio] --v 6.1 --style raw --no text watermark logo
```

**Шаблон для трансформації (transformation):**
```
A [вік]-year-old [стать] [дія з ідеальної трансформації ДНК], [яскрава, позитивна локація], [впевнена поза, усмішка, енергія], lifestyle editorial photography, [камера] [об'єктив], golden hour lighting, [тепла/яскрава палітра], [настрій: empowered/confident/joyful] --ar [ratio] --v 6.1 --style raw --no text watermark logo
```

### 2. Text-heavy (мінімалістичний фон + великий текст)

**Коли використовувати:** Myth-busting (ступені 1-3), FOMO (ступені 0-1), Urgency (ступені 4-5)

**Структура промта:**
```
Minimalist [колір] gradient background, clean modern design, soft lighting, no objects, [текстура: subtle grain/smooth/bokeh], professional advertising backdrop --ar [ratio] --v 6.1 --no text watermark logo people
```

**Тексти на картинці (накладаються в редакторі):**
- Заголовок: великий, по центру або верхня третина
- Підзаголовок: дрібніший, під заголовком
- CTA: контрастна кнопка, нижня третина

### 3. Before-After (спліт-композиція)

**Коли використовувати:** Transformation (ступені 2-4), Myth-busting (ступені 2-3)

**Структура промта:**
```
Split image composition, left side: [опис ситуації «до» з ДНК - біль, втома, проблема], right side: [опис ситуації «після» з ідеальної трансформації ДНК], [стиль фотографії], clear visual contrast between both sides, same person in both, [палітра: cold left / warm right] --ar [ratio] --v 6.1 --style raw --no text watermark logo
```

### 4. Testimonial / UGC-стиль

**Коли використовувати:** Social proof (ступені 3-5), UGC (усі ступені)

**Структура промта для UGC:**
```
Selfie-style photo of a [вік]-year-old [стать] [емоція: happy/relieved/excited], [casual setting: home/cafe/park], looking directly at camera, natural smartphone lighting, slightly imperfect composition, authentic candid feel, iPhone photography style, warm natural tones --ar [ratio] --v 6.1 --style raw --no text watermark logo
```

**Структура промта для testimonial:**
```
Portrait of a [вік]-year-old [стать] with genuine smile, [professional/casual setting], soft natural lighting, clean background with subtle [колір] tones, editorial portrait style, space for quote overlay on [left/right/top] side --ar [ratio] --v 6.1 --style raw --no text watermark logo
```

### 5. Product-hero (продукт у центрі)

**Коли використовувати:** Direct offer (ступені 4-5), Bonus stack (ступінь 5)

**Структура промта:**
```
[Продукт/mockup] centered on [мінімалістичний фон], professional product photography, soft studio lighting with [accent color] rim light, clean composition with space for text overlay, premium feel, [стиль: flat lay/floating/3D render] --ar [ratio] --v 6.1 --no text watermark logo
```

## A/B варіації

Для КОЖНОГО креативу генеруй 3 варіації:

**Варіація A (базова):** Основний промт + основний заголовок + основний CTA

**Варіація B (тест хука):**
- Той самий візуал (промт)
- Інший заголовок (тестуємо формулювання hook)
- Той самий CTA
- Позначка: «Тестуємо: hook (A: [тип] vs B: [тип])»

**Варіація C (тест візуалу):**
- Інший візуал (інший промт - інша композиція або ракурс)
- Той самий заголовок
- Той самий CTA
- Позначка: «Тестуємо: візуал (A: [опис] vs C: [опис])»

## Формули заголовків за ступенями

### Ступені 0-1 (холодний трафік)
- **Питання з монологу:** «Ти знову [больова ситуація]?»
- **FOMO:** «Поки ти [поточна дія], інші вже [результат]»
- **Шок-статистика:** «[Число]% [аватарів] роблять цю помилку»
- **Контраст:** «[Больова ситуація] vs [трансформація] - різниця в одному кроці»

### Ступені 2-3 (теплий трафік)
- **Myth-bust:** «„[Міф з ДНК]" - найгірша порада при [проблемі]»
- **Система:** «[Число] кроків від [болю] до [трансформації]»
- **How-to:** «Як [результат] без [зусилля/жертви з ДНК]»
- **Education:** «Чому [хибне рішення] не працює (і що працює)»

### Ступені 4-5 (гарячий трафік)
- **M-A-G-I-C:** «[Магнітна причина]: [Результат] за [Час] для [Аватар]»
- **Social proof:** «[Число] [аватарів] уже [результат]. Ось що вони кажуть»
- **Guarantee:** «[Результат] або [гарантія]. Без питань»
- **Urgency:** «Залишилось [число] місць. Старт [дата]»

## Формули CTA за ступенями

| Ступінь | Тип CTA | Приклади |
|---------|---------|---------|
| 0-1 | М'який, інформаційний | «Дізнайся детальніше →», «Забери безкоштовний гайд», «Дивись відео» |
| 2-3 | Середній, залучаючий | «Отримай план дій», «Записатись на розбір», «Завантаж чек-лист» |
| 4-5 | Прямий, конверсійний | «Забронювати місце», «Оплатити зі знижкою», «Записатись зараз» |

## Кольорова палітра за емоціями

| Емоція з ДНК | Палітра | Hex приклади |
|---------------|---------|-------------|
| Тривога, страх | Холодні сині, сірі | #2C3E50, #34495E, #7F8C8D |
| Втома, вигорання | Приглушені, десатуровані | #95A5A6, #BDC3C7, #D5DBDB |
| Надія, трансформація | Теплі золоті, бурштинові | #F39C12, #E67E22, #F1C40F |
| Впевненість, сила | Глибокі, насичені | #2980B9, #8E44AD, #27AE60 |
| Терміновість, urgency | Червоні, помаранчеві | #E74C3C, #C0392B, #E67E22 |
| Преміум, довіра | Темні + акценти | #1A1A2E, #16213E, #D4AF37 |
