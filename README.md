# Проект аннотации городских птиц

## Проектирование аннотационной схемы (ЛР2)

### Аннотационная схема
Схема описана в `annotation_schema.md`, папка `data/Lr2/`

### Модальности и форматы
- Текст — CoNLL-U, папка `data/Lr2/text`
- Изображения — CVAT JSON/XML, папка `data//Lr2/images`
- Аудио — TextGrid, папка `data//Lr2/audio`

### Верификация
Перекрёстная проверка, kappa ≥ 0.8, IoU ≥ 0.75, проверка каждого 5-го файла.

## Разметка текстовых данных (ЛР №3)

### Способ разметки
Инструмент INCEpTION не устанавливался. Разметка выполнена вручную
в формате CoNLL-U, полностью совместимом с экспортом INCEpTION.

### Уровни разметки
- Документ (`# doc_id`, `# species`)
- Параграф (`# paragraph = p1, p2, ...`)
- Токен (столбец FORM)
- Часть речи (столбец UPOS)
- Именованная сущность (MISC: `NER=B-...`, `NER=I-...`)

### Типы именованных сущностей
- SPECIES — вид птицы
- LOCATION — место
- DATE_TIME — дата/время
- BEHAVIOR — поведение
- COLOR — цвет оперения
- SOUND — тип звука

### Файлы разметки
- `data/Lr3/annotated/sparrow.conllu`
- `data/Lr3/annotated/pigeon.conllu`
- `data/Lr3/annotated/tit.conllu`
- `data/Lr3/annotated/magpie.conllu`

### Изменения в аннотационной схеме
Добавлены теги `SOUND_TYPE` (SONG, CALL, TRILL) и `BODY_PART`, папка `data/Lr3/`

## Разметка изображений (ЛР №5)

### Способ разметки
Инструмент CVAT не устанавливался. Разметка выполнена вручную
в формате CVAT JSON, полностью совместимом с экспортом CVAT.

### Классы объектов
- SPARROW — домовый воробей
- PIGEON — сизый голубь
- TIT — большая синица
- MAGPIE — сорока

### Классы деталей
- BEAK — клюв
- TAIL — хвост
- WING — крыло
- PLUMAGE — оперение
- LEG — лапа

### Атрибуты
- pose, occlusion, plumage_color, age_sex, confidence

### Формат хранения
CVAT JSON: `data/Lr5/images/annotated/*.json`

### Файлы разметки
- `data/Lr5/images/annotated/sparrow_01.json`
- `data/Lr5/images/annotated/pigeon_01.json`
- `data/Lr5/images/annotated/tit_01.json`
- `data/Lr5/images/annotated/magpie_01.json`

## Источники изображений

- sparrow_01.jpg — Wikimedia Commons, File:House Sparrow (Passer domesticus), Mirpur.jpg, CC BY-SA
- pigeon_01.jpg — Wikimedia Commons, File:Pigeon portrait 4861.jpg, CC BY-SA
- tit_01.jpg — Wikimedia Commons, File:Velika senica (Parus major) Great Tit.jpg, CC BY-SA
- magpie_01.jpg — Wikimedia Commons, File:Eurasian magpie Gennevilliers 02.jpg, CC BY-SA
