# Тест кейсы для приложения таймера

| ID  | Название теста                        | Предусловия                                                   | Шаги                                                                                                                                                     | Ожидаемый результат                                                                                                                                   |
|-----|---------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Добавление нового таймера             | Приложение открыто                                            | 1. Нажать на кнопку "+". <br> 2. Выбрать время (минуты и секунды) с помощью рулетки. <br> 3. Нажать кнопку "Старт".                                     | Новый таймер добавлен и отображается в списке таймеров. Начинается обратный отсчет времени.                                                            |
| 2   | Отмена добавления таймера             | Приложение открыто                                            | 1. Нажать на кнопку "+". <br> 2. Нажать кнопку "Отменить".                                                                                               | Новый таймер не добавлен.                                                                                                                              |
| 3   | Запуск таймера                        | Существует хотя бы один таймер                                 | 1. Нажать кнопку "Старт" напротив одного из таймеров.                                                                                                    | Таймер начинает обратный отсчет времени.                                                                                                               |
| 4   | Пауза таймера                         | Таймер запущен                                                | 1. Нажать кнопку "Пауза" напротив активного таймера.                                                                                                     | Таймер ставится на паузу, обратный отсчет останавливается.                                                                                             |
| 5   | Сброс таймера                         | Таймер запущен или на паузе                                    | 1. Нажать кнопку "Отмена" напротив активного или паузированного таймера.                                                                                 | Таймер сбрасывается, время возвращается к исходному значению.                                                                                          |
| 6   | Удаление таймера                      | Существует хотя бы один таймер                                 | 1. Нажать кнопку "Править". <br> 2. Нажать кнопку "-" напротив одного из таймеров. <br> 3. Нажать кнопку "Готово".                                       | Таймер удаляется из списка.                                                                                                                            |
| 7   | Запуск всех таймеров                  | Существует хотя бы один таймер                                 | 1. Нажать кнопку "Старт" для всех таймеров.                                                                                                              | Все таймеры начинают обратный отсчет времени.                                                                                                          |
| 8   | Пауза всех таймеров                   | Все таймеры запущены                                          | 1. Нажать кнопку "Пауза" для всех таймеров.                                                                                                              | Все таймеры ставятся на паузу, обратный отсчет останавливается.                                                                                        |
| 9   | Сброс всех таймеров                   | Все таймеры запущены или на паузе                              | 1. Нажать кнопку "Отмена" для всех таймеров.                                                                                                             | Все таймеры сбрасываются, время возвращается к исходному значению.                                                                                     |
| 10  | Отображение всех таймеров             | Существует хотя бы один таймер                                 | 1. Нажать кнопку "Таймеры".                                                                                                                              | Отображается список всех добавленных таймеров.                                                                                                         |
| 11  | Редактирование таймера                | Существует хотя бы один таймер                                 | 1. Нажать кнопку "Править". <br> 2. Выбрать таймер для редактирования. <br> 3. Изменить время с помощью рулетки. <br> 4. Нажать кнопку "Готово".        | Время таймера изменяется, новые значения отображаются в списке таймеров.                                                                               |
| 12  | Корректность обратного отсчета времени| Таймер запущен                                                | 1. Наблюдать за обратным отсчетом времени таймера.                                                                                                       | Таймер показывает корректный обратный отсчет времени, секунды уменьшаются на 1 каждую секунду.                                                         |
| 13  | Добавление нескольких таймеров        | Приложение открыто                                            | 1. Нажать на кнопку "+". <br> 2. Выбрать время (минуты и секунды) с помощью рулетки. <br> 3. Нажать кнопку "Старт". <br> 4. Повторить для нескольких таймеров. | Все добавленные таймеры отображаются в списке и могут быть запущены по отдельности.                                                                    |
| 14  | Пауза отдельного таймера              | Несколько таймеров запущены                                    | 1. Нажать кнопку "Пауза" напротив одного из активных таймеров.                                                                                           | Только выбранный таймер ставится на паузу, остальные продолжают обратный отсчет времени.                                                               |
| 15  | Сброс отдельного таймера              | Несколько таймеров запущены или на паузе                       | 1. Нажать кнопку "Отмена" напротив одного из активных или паузированных таймеров.                                                                        | Только выбранный таймер сбрасывается, время возвращается к исходному значению.                                                                          |

## Использованные техники тест-дизайна

- **Эквивалентное разделение**: Проверка функциональности добавления, удаления и редактирования таймеров.
- **Анализ граничных значений**: Проверка корректности обратного отсчета времени.
- **Попарное тестирование**: Тестирование взаимодействия нескольких таймеров одновременно (добавление, запуск, пауза, сброс).
- **Тестирование состояния**: Проверка поведения таймеров в разных состояниях (запущен, на паузе, сброшен).
- **Тестирование переходов**: Проверка корректности переходов между состояниями таймера (например, запуск -> пауза -> сброс).
