# neuro_data_lyashevskaya

**task 1**

Возьмите тот же датасет, что был у вас в дз1, отфильтруйте и разбейте на части так, что:
- тренировочный датасет содержит 2500 строк, валидационный 100 строк
- все строчки тренировочного и валидационного датасета содержат от 512 до 1024 токенов (получаемых t5-long токенизатором)

Обучите модель longt5-base для задачи суммаризации:
- loss должен сойтись (не NaN и не сверхбольшое число, обычный убывающий loss) 
Постройте график loss.

Предскажите ответ модели:
- на валидационном датасете 
Выведите результаты для первых/любых трех строк валидационного датасета 
Оцените качество работы.

Опишите текстом, какие параметры скорости обучения, количества эпох, batch size, effective batch size использует обученная модель, как вел себя loss во время обучения. Если loss сошелся не не с первого запуска, прокомментируйте ход ваших рассуждений, какие действия вы предприняли в этом случае.

**task 2**

Обучите long-t5-tglobal-base для задачи суммаризации, инференс делаем в конце для обученной модели
Датасет - по вашему выбору, но другой (не тот, который использовался в ДЗ1)
Отфильтруйте данные, чтобы в каждой строке было не менее 1024 токена и чтобы объем обучающих данных был не менее 10 тыс. таких строк (работа с датасетом - макс. 2 балла)
Сделайте анализ релевантных для задачи распределений в датасете (например, минимальное, максимальное, среднее значение, стандартное отклонение или постройте гистограмму) и напишите вывод (1-2 предложения) (описательные статистики - макс. 2 балла) 
Сделайте подбор параметров 
- learning rate
- efficient batch size
- batch size
- epoch number
и напишите вывод текстом, на каком значении и почему вы остановились (подбор параметров - макс. 3 балла)
