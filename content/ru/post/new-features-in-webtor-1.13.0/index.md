---
title: "Новые улучшения в Webtor 1.13.0"
date: 2021-12-11T16:38:00+03:00
series: "Что нового"
translationKey: "v1.13.0"
titleEmoji: ":tada:"
aliases:
    - /ru/v1.13.0/
---
Вот список ключевых изменений:

1. **️Исправлены ошибки дозагрузки** - теперь в случае сбоя при загрузке корректно работает возможность дозагрузки, это касается
загрузки как отдельных файлов, так загрузки ZIP-архивом.

2. **Меньше обрывов и сбоев** - ранее при релизах компонентов все загрузки обрывались, теперь они просто приостанавливаются
на время обновления.

3. **Торрент-файлы живут вечно** - ранее торрент-файлы удалялись через определенное время, теперь они сохраняются навсегда, это
позволяет реже обращаться к BitTorrent-сети и улучшает время отклика. (это не касается загружаемого контента!)

4. **Отображение приоритета загрузки** - ранее при отображении прогресса загрузки подсвечивались только загруженные фрагменты,
теперь также подсвечиваются и фрагменты которые загружаются с высоким приоритетом.

5. **Улучшена адаптивность интерфейса** - теперь экранное пространство на мобильных устройствах используется более эффективно.

6. **Drag&drop работает и для субтитиров** - теперь можно просто перекинуть субтитры в окно плеера.

Кроме того теперь у проекта появился свой [Subreddit](https://www.reddit.com/r/webtor/), где мы можем обсуждать доработки и
направления развития проекта.

А для [WordPress](https://wordpress.org/) появился [свой собственный плагин](https://github.com/webtor-io/wordpress-plugin)
для вставки webtor-плеера в любой WordPress-блог.

Спасибо что используете [webtor.io](https://webtor.io/ru/) и [поддержите проект](https://www.patreon.com/bePatron?u=24145874)!