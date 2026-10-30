# interface-skills-yarzz

Скиллы для Claude Code и других агентов: как строить интерфейсы, которые читаются с одного взгляда, и как адаптировать плотные кабинеты под телефон.

## Скиллы

- [**scannable-ui**](skills/scannable-ui/SKILL.md) — сканируемый интерфейс: **края** вместо пустоты, **различение** вместо «воздуха», **визуальное вместо текста**, **акцент как разница** с соседями, **меньше вложенных карточек**; плюс **мобильная адаптация** кабинетов — нижнее меню-остров, таблицы без горизонтальной прокрутки, окна-шторки.
  - [edges-and-density.md](skills/scannable-ui/edges-and-density.md) — рецепты краёв, выравнивания и плотности.
  - [mobile.md](skills/scannable-ui/mobile.md) — мобильные правила с подводными камнями и проверками.

Хорошо работает вместе с набором [`jakubkrehel/skills`](https://github.com/jakubkrehel/skills) (`interfaces`): там — доступность, типографика, цвет, тексты и анимация.

## Установка

Claude Code, как плагин:

```text
/plugin marketplace add Yaroslaz/interface-skills-yarzz
/plugin install yarzz-interfaces@interface-skills-yarzz
```

Или скопируйте папку скилла к себе:

```bash
git clone https://github.com/Yaroslaz/interface-skills-yarzz
cp -r interface-skills-yarzz/skills/scannable-ui ~/.claude/skills/
```

## Как расширять

- Новый скилл — новая папка `skills/<имя>/` с `SKILL.md` (front matter `name` и `description`) и подробностями в соседних `.md`.
- В `SKILL.md` — правила, которые применяются всегда, и таблица «Перед тем как закончить». Длинные рецепты — в отдельных файлах со ссылками из `SKILL.md`.
- Каждое правило — проверяемое: что сделать, на каком значении, как увидеть нарушение.
- Источник — в разделе «Источники».

## Источники

- Kole Jain — [«The secret behind weirdly perfect UI designs»](https://www.youtube.com/watch?v=neE6wOuBIP8).
- Мобильная адаптация кабинета преподавателя TestSpace.
