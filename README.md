# Scorpion ZS-256 Turbo+

## Российский клон компьютера ZX Spectrum с улучшениями.

Компьютер разрабатывался и выпускался, под руководством Сергея Зонова, санкт-петербургской фирмой Scorpion с 1996 по 1998г.
Данная версия схемы, отревершена по файлам molodcov_alex, а затем и по плате Павла Рябцова известной как "Black Edition".
Изначально это была схема, которая упоминается как схема Черного кота. В создании схемы, большую помощь оказали труды savelij из темы про скорпиона 1024.

## Особенности:
- Z80B CPU, режим Turbo 7MHz, данный вариант хорошо работает с КМОП процессорами Z84C0020PEC.
- 256k DRAM, хорошо работают только импортные микросхемы типа 41256.
- Теневой Сервис-Монитор
- Музыкальный сопроцессор AY-3-8912.
- 2 Слота расширения ZX Bus.
- Контроллер дисковода Floppy-дисков с ФАПЧ.
- Старые микросхемы 565РТ5 заменены более доступными GAL16V8, GAL22V10.
- PROF ROM.
- Интерфейс Centronics для принтера.
- Интерфейс RS-232, но никто не проверял, работает ли?

[Принципиальная схема](Export/Schematic_Scorpion-256-Turbo_v16.2.4.pdf)

[Монтажная схема](Export/PCB_SILK_TOP_BW_v16.2.4.pdf)

Печатная плата и герберы, получены, как побочный продукт при реверсе схемы и отличаются и от платы molodcov_alex и от платы Павла. Мной плата не заказывалась, но многие уже собирали её. Некоторые трассы укаорочены, уменьшено число изгибов проводников, уменьшено число проводников между ножками процессора с 3-х до 2-х.
На плате нет краевых разъемов.

[Тема на форуме, по данному варианту компьютера](https://zx-pk.ru/threads/9195-scorpion-zs-256-turbo-restored)

[Чат ZS Scorpion  в Telegram](https://t.me/zs_scorpion)

## Изменения
- В версии схемы v16.2, исправлено подключение GAL ФАПЧ контроллера дисковода. Несоответствие было обнаружено при сборке платы пользователем форума tigr101274. Исправлена печатная плата в соответствии со схемой, на печатной плате значительно расширены проводники питания за счет полигонов.
- В версии v16.2.1 исправлена ошибка, замеченая azx987sa, с сигналом строба интерфейса принтера.
- В версии v16.2.2 добавлен резистор R76, как в Scorpion ZS 1024 Turbo+ от savelij, для лучшего качества звука с AY. Убраны лишние дорожки и переходные отверстия, замеченные пользователем ponchick.
- В версии v16.2.3 изменена схема формирования сигнала DSR, по варианту, предложенному Jeckas Nameless. Изменены футпринты для транзисторов КТ315/КТ361 и некоторых конденсаторов. Перенесен диод VD2 для более удобного монтажа.
- В версии v16.2.4 подвинуты некоторые элементы для удобства сборки. На разъем XP3 выведен сигнал SYNC и добавлен разъем X16 - выход частоты 14МГц. Заменен футпринт для AY (DD51) на нормальный, под панельку. Добавлена пара конденсаторов по питанию, в районе чипов памяти. Перенумерованы диоды, для соответствия оригиналу.