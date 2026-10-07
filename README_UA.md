# Evolutionarium V2 Illustrated — GDevelop Native Sprites

У цьому проєкті візуальні елементи — **справжні Sprite/Text Objects GDevelop**, а не CSS/HTML-накладка.

## Що є в сцені
- 64 об’єкти Cell (Hidden/Open) — створюються нативно і перемикають спрайти.
- Piece — одна GDevelop Sprite-група з 11 анімаціями: 5 фішок, Chest/Bomb/Key/Exit, Rocket/Prism.
- Enemy — Spider/Scorpion.
- Фон, рамка поля, HUD-панелі, усі 5 кнопок — окремі GDevelop Sprite Objects.
- Керування, Match-3, Gravity, Reveal, атаки, еволюція, relic choices, Elite та Alpha Scorpion — JavaScript Event керує нативними об’єктами.

## Відкрити ЛОКАЛЬНО
1. Розпакуй ZIP, щоб `game.json` лежав поруч із папкою `assets/`.
2. Відкрий проєкт в GDevelop Desktop (Open local project) або імпортуй через підтримуваний спосіб роботи із файлами.
3. Preview.

## Відкрити ЧЕРЕЗ БРАУЗЕР (твій GitHub)
1. Відкрий репозиторій: https://github.com/mickalaykorolyov-bit/Evolutionarium
2. Завантаж у корінь репозиторію **папку `assets/`** і файл **`game_web.json`** з цього архіву. Важливо зберегти структуру `assets/evo_....png`.
3. Перевір, що відкривається, наприклад: https://raw.githubusercontent.com/mickalaykorolyov-bit/Evolutionarium/main/assets/evo_board_frame.png
4. Встав у браузер:
   https://editor.gdevelop.io/?project=https%3A%2F%2Fraw.githubusercontent.com%2Fmickalaykorolyov-bit%2FEvolutionarium%2Fmain%2Fgame_web.json
5. Preview/Play. Після імпорту можна редагувати Sprite Objects у Scene Editor.

## Управління
- Обери фішку, потім сусідню — Match-3.
- Red damage, Purple +Reveal; Scout за 3 Reveal.
- Reveal знайде Key/Exit та прихованих ворогів.
- Після Key + Exit: Continue Room -> реліквія -> Elite -> Boss.
- DNA 5 сумарних матчів -> вибір еволюції (Venom / Silk / Arcane).
- New Run, Sound ON/OFF, How To Play працюють через GDevelop mouse/touch input.

## Важливі обмеження цієї alpha-збірки
- Логіка ще об'єднана в одному JavaScript Event; для повністю no-code редагування її треба розбити на External Events.
- Нативні об'єкти можна редагувати в Scene Editor. Зараз початкові координати HUD та сітки також фіксовані в JS, тому перенесення HUD мишкою вимагатиме оновлення констант у Event.
- Для браузерного запуску **всі PNG повинні бути завантажені в GitHub** за URL-адресами, зазначеними в `game_web.json`.
- **Повноцінний запуск у GDevelop Editor у середовищі створення не перевірявся** (редактор/движок не встановлений). Перевірена структура файлів, JS-синтаксис, JSON-схеми та PNG.
