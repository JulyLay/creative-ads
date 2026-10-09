# Майстер-гайд з AI-промтів для рекламних креативів

5 інструментів генерації. Для кожного: структура промта, найкращі практики, параметри, приклади.

---

## 1. Midjourney

### Структура промта

```
[Суб'єкт], [дія/поза], [оточення/фон], [стиль фотографії], [камера/об'єктив], [освітлення], [кольорова палітра], [настрій] --ar [співвідношення] --v 6.1 --style raw
```

### Параметри

| Параметр | Значення | Коли |
|----------|----------|-------|
| --v 6.1 | Версія моделі | Завжди |
| --style raw | Менше «прикрашання» | Для реалістичних фото |
| --ar X:Y | Співвідношення сторін | Завжди (див. platform-specs.md) |
| --s 50-150 | Стилізація | 50 = реалістично, 150 = художньо |
| --q 1 | Якість (за замовчуванням) | Стандартне |
| --no [елемент] | Виключити елемент | Якщо треба прибрати щось |
| --chaos 0-100 | Варіативність | 0 = передбачувано, 20-40 для тестів |

### Стилі для реклами

| Стиль | Ключові слова в промті | Коли |
|-------|------------------------|-------|
| Документальний | documentary photography, candid, natural, 35mm film | Pain-agitate, lifestyle |
| Студійний | studio lighting, clean background, product shot | Product-hero, offer |
| UGC | iPhone photo, casual, authentic, slightly imperfect | TikTok, social proof |
| Кінематографічний | cinematic, anamorphic, shallow depth of field | Before/After, transformation |
| Мінімалістичний | minimal, clean, white space, modern design | Text-heavy, infographic |
| Емоційний | intimate, close-up, emotional, soft light | Pain, transformation |

### Камери і об'єктиви для реалізму

| Тип | Ключові слова | Ефект |
|-----|---------------|--------|
| Портрет | Canon R5, 85mm f/1.4 | М'яке боке, фокус на обличчі |
| Lifestyle | Sony A7III, 35mm f/1.8 | Широкий контекст, природно |
| Деталь | Canon 100mm macro | Крупний план, текстура |
| Загальний план | 24mm wide angle | Простір, контекст |
| UGC | iPhone 15, selfie | Автентичність |

### Приклади за кутами

**Pain-agitate (ступінь 0-1):**
```
A 35-year-old woman sitting alone on bed at 3am, phone glow illuminating tired face, self-help books scattered on nightstand, documentary photography, Canon R5 35mm f/1.8, blue ambient light from phone screen, muted blue-grey tones, exhausted and anxious mood --ar 1:1 --v 6.1 --style raw
```

**Transformation (ступінь 3-4):**
```
Split composition, left side: exhausted woman in dark room blue tones, right side: same woman radiating confidence in bright sunlit room warm tones, clean dividing line, before and after concept, cinematic photography, balanced lighting --ar 4:5 --v 6.1 --style raw
```

**Social proof (ступінь 4-5):**
```
Smiling woman in her 30s holding phone showing positive results, cozy home office background, warm natural window light, authentic genuine expression, iPhone selfie style, casual outfit, slightly imperfect framing --ar 1:1 --v 6.1 --style raw
```

---

## 2. DALL-E (DALL-E 3)

### Структура промта

```
[Детальний опис сцени]. [Стиль і техніка]. [Композиція і ракурс]. [Освітлення і колір]. [Настрій].
```

### Особливості DALL-E

- Промти **англійською** дають кращий результат
- Підтримує **текст на зображенні** (вказуй у лапках)
- Фіксовані розміри: 1024×1024, 1024×1792, 1792×1024
- Немає параметрів на кшталт --ar, розмір вказується при виклику API
- Більш буквально інтерпретує промт (описуй точніше)

### Розміри

| Платформа | Розмір DALL-E | Примітка |
|-----------|---------------|------------|
| Meta Feed, Google Square | 1024×1024 | 1:1 |
| Stories, Reels, TikTok | 1024×1792 | ~9:16 |
| YouTube, Google Landscape | 1792×1024 | ~16:9 |

### Приклад промта

**Pain-agitate:**
```
Photorealistic image of a woman in her mid-30s sitting on the edge of her bed at 3 AM. Her face is illuminated by the blue glow of her smartphone. She looks exhausted with dark circles under her eyes. Self-help books are scattered on the nightstand. The room is dark with blue-grey ambient tones. Documentary photography style with natural, candid feel. The mood is isolated and anxious.
```

**Text-heavy (з текстом на зображенні):**
```
Clean minimalist graphic design on warm cream background. Large bold text in the center reading "90% don't know this". Subtle geometric shapes in soft coral and terracotta colors. Modern sans-serif typography. Clean and professional look suitable for social media advertising.
```

---

## 3. Nano Banana Pro

### Структура промта

```
[Опис сцени], [стиль візуалу], [композиція], [палітра], [формат/розмір]
```

### Особливості

- Оптимізований під **комерційні візуали**
- Добре працює з **product shots** і **branding**
- Підтримує вказання формату в промті
- Менш деталізований промт, ніж у Midjourney

### Стилі для реклами

| Стиль | Ключові слова |
|-------|---------------|
| Product | clean product photography, studio, white background |
| Lifestyle | lifestyle shot, natural setting, authentic |
| Branding | brand visual, corporate, polished |
| Social Media | social media graphic, vibrant, eye-catching |
| Minimal | minimalist, clean lines, negative space |

### Приклад промта

**Lifestyle (ступінь 0-1):**
```
Woman sitting alone on bed late at night looking at phone, tired expression, messy hair, blue phone glow on face, dark bedroom with soft shadows, documentary lifestyle photography, muted blue-grey palette, square format 1:1
```

**Product-hero (ступінь 4-5):**
```
Digital course mockup on modern laptop screen, woman smiling on screen, surrounded by floating benefit icons, clean white background with soft gradient, professional product photography, warm coral and white palette, vertical format 9:16
```

---

## 4. Higgsfield

### Структура промта

Заточений під **вертикальне відео** (Reels/TikTok), **UGC-стиль**.

```
[Дія персонажа], [UGC/selfie стиль], [вертикальний формат], [розмова на камеру або lifestyle], [тривалість], [настрій]
```

### Особливості

- Спеціалізація: **UGC-відео для соцмереж**
- Вертикальний формат за замовчуванням
- Найкращий результат з **talking head** і **lifestyle** сценами
- Не підходить для кінематографічного стилю

### Типи контенту

| Тип | Промт-патерн | Коли |
|-----|--------------|-------|
| Talking head | «[Person] talking directly to camera, selfie angle...» | Story, myth-busting |
| Lifestyle | «[Person] doing [action] in [location]...» | Before/after, transformation |
| Reaction | «[Person] reacting to [something] with [emotion]...» | Hook, pain |
| Tutorial | «[Person] showing [process] step by step...» | Education, solution |

### Приклади

**Hook (ступінь 0-1):**
```
Young woman talking directly to camera in her bedroom at night, selfie style, vertical format, she looks tired and frustrated, blue phone light on her face, authentic UGC feel, she starts speaking with urgency about not being able to sleep, warm indoor lighting, 3 seconds, anxious and relatable tone
```

**Story (ступінь 1-2):**
```
Woman in her 30s sitting in cozy living room, talking to camera in confessional style, vertical format, she shares personal story about trying everything for anxiety, genuine emotional delivery, natural daylight from window, 15 seconds, vulnerable but hopeful tone
```

**Transformation (ступінь 3-4):**
```
Split screen effect: left side shows stressed woman in dark room, right side shows same woman smiling confidently in bright setting, vertical format, dramatic transition between two states, before and after concept, 5 seconds, inspiring and empowering tone
```

---

## 5. Runway / Sora

### Структура промта (покадровий)

```
Scene [N]: [Опис сцени], [рух камери], [стиль], [освітлення], [тривалість]
```

### Рухи камери

| Рух | Ключові слова | Ефект |
|----------|---------------|--------|
| Статика | static shot, locked off | Стабільність, акцент на суб'єкті |
| Наїзд | slow push in, camera push in | Увага, інтимність |
| Від'їзд | slow pull back, camera pulls back | Контекст, reveal |
| Панорама | slow pan left/right | Огляд, перехід |
| Tracking | tracking shot, following | Рух, енергія |
| Crane | crane up/down | Масштаб, драматизм |
| Handheld | handheld, slight shake | Документальність, UGC |
| Timelapse | time-lapse, accelerated | Трансформація, час |

### Стилі

| Стиль | Коли | Ключові слова |
|-------|-------|---------------|
| Documentary | Pain-agitate, real stories | documentary, handheld, natural light |
| Cinematic | Transformation, premium | cinematic, anamorphic, color graded |
| UGC | TikTok, authentic | selfie camera, smartphone footage |
| Commercial | Product, offer | polished, clean, professional |
| Dramatic | Myth-busting, reveal | dramatic lighting, high contrast |

### Приклад повного сценарію (30 сек, ступінь 0-1)

```
Scene 1: Close-up of a woman's face illuminated by phone screen in dark bedroom, slight camera push in, documentary style, blue ambient light, 3 seconds

Scene 2: Same woman sitting up in bed rubbing her eyes, slow pan from hands to face revealing exhaustion, warm practical lighting from bedside lamp, 4 seconds

Scene 3: Montage of failed attempts: pill bottles, meditation app on phone, herbal tea cooling untouched, quick cuts between static shots, muted desaturated tones, 5 seconds

Scene 4: Woman looking at phone screen showing a hopeful message, her expression softens, gentle camera push in on her face, warm golden light gradually replacing blue, 5 seconds

Scene 5: Time-lapse of sunrise through bedroom window, woman doing calm breathing exercise by the window, camera slowly pulls back to reveal peaceful room, golden hour light flooding in, 8 seconds

Scene 6: Woman smiling with genuine confidence in bright sunlit room, static shot with gentle bokeh background, warm natural light, text overlay appears, 5 seconds
```

### Приклад для TikTok (15 сек, Higgsfield-стиль у Runway)

```
Scene 1: Young woman picks up phone and starts talking to camera, bedroom setting, selfie angle vertical format, natural indoor lighting, authentic and casual, 3 seconds

Scene 2: Same woman getting animated about the topic, hand gestures, slight zoom in, continues talking with conviction, 5 seconds

Scene 3: Quick cut to lifestyle shot of woman sleeping peacefully, soft morning light, gentle camera movement, 4 seconds

Scene 4: Back to talking head, woman smiles and points down (to link), text overlay with CTA, 3 seconds
```

---

## Універсальні правила промт-інжинірингу

### 1. Конкретність

| Погано | Добре |
|-------|--------|
| A sad woman | A 35-year-old woman with dark circles under her eyes, sitting alone on the edge of her bed at 3am |
| Nice lighting | Warm golden hour light streaming through a window, soft shadows |
| Beautiful background | Cozy bedroom with white linen, potted plants, morning light |

### 2. Мова промта - завжди англійська
Навіть якщо цільова аудиторія україномовна, промти для AI пишуться англійською. Текст українською додається поверх у дизайні.

### 3. Порядок елементів (від важливого до деталей)
1. Суб'єкт (хто/що)
2. Дія (що робить)
3. Оточення (де)
4. Стиль (як виглядає)
5. Технічні деталі (камера, світло)
6. Параметри (--ar, --v)

### 4. Консистентність серії
Для A/B варіацій використовуй **загальну базу промта** і міняй лише тестований елемент:

```
БАЗА: A 35-year-old woman, documentary photography, Canon R5, muted tones --v 6.1 --style raw

Варіація A: [БАЗА] + sitting alone on bed at 3am, phone glow --ar 1:1
Варіація B: [БАЗА] + close-up of hands clutching phone anxiously --ar 1:1
Варіація C: [БАЗА] + standing by window looking out at dark city --ar 1:1
```

### 5. Текст на зображенні
- **Midjourney:** Погано генерує текст. Не включай текст у промт - додавай у дизайні.
- **DALL-E:** Уміє генерувати текст. Вказуй у лапках: `text reading "Your headline here"`
- **Nano Banana Pro:** Середньо. Краще додавати текст окремо.

### 6. Таблиця відповідності: кут → інструмент

| Кут | Найкращий інструмент | Чому |
|------|-------------------|--------|
| Pain-agitate (статика) | Midjourney | Реалізм, емоція, деталізація |
| Text-heavy | DALL-E | Генерація тексту на зображенні |
| Before/After | Midjourney | Контроль над композицією |
| Social proof / UGC (статика) | Nano Banana Pro | Швидкий, комерційний стиль |
| Product-hero | Nano Banana Pro | Заточений під продуктові візуали |
| UGC відео | Higgsfield | Спеціалізація на вертикальному UGC |
| Кінематографічне відео | Runway/Sora | Якість, контроль камери |
| TikTok нативне | Higgsfield | UGC-стиль, вертикальний формат |
| YouTube pre-roll | Runway/Sora | Горизонтальний, кінематографічний |
