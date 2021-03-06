# Лабораторные работы по курсу Глубокое обучение.
 - Лабораторная работа №1: "Реализация метода обратного распространения ошибки для двуслойной полностью связанной нейронной сети"
 - Лабораторная работа №2: "Разработка полностью связанной нейронной сети"
 - Лабораторная работа №3: "Разработка свёрточной нейронной сети"
 - Лабораторная работа №4: "Начальная настройка весов полностью связанных нейронных сетей"
 - Лабораторная работа №5: "Применение переноса обучения глубоких нейронных сетей"
 
 ## Лабораторные 2-5
  Для разработки были выбраны следующие средства Python + MXNet, решалась задача бинарной классификации "Еда - не еда"
 
 ## Средства разработки
  Для запуска и разработки требуется Python, pip, для запуска на gpu - CUDA
Установка необходимых библиотек с помощью pip
<pre><code>pip install mxnet
pip install opencv-python
</code></pre>
Для GPU ставим
<pre><code>pip install mxnet-cuXX
</code></pre>
где ХХ - версия CUDA, у нас использовалась 8.0
## Данные
  Для выполнения лабораторной работы был выбран набор данных для решения задачи бинарной классификации: «еда» - «не еда». Были использованы картинки из набора данных https://www.kaggle.com/dansbecker/food-101/data в качестве «еды» и картинки из наборов данных https://www.kaggle.com/c/dogs-vs-cats/data и http://host.robots.ox.ac.uk/pascal/VOC/voc2012/index.html в качестве «не еды». Итоговый набор данных состоит из 143125 изображений. С помощью скрипта  im2rec.py, который входит в библиотеку MXNet, изображения были сконвертированы в формат .rec, который обрабатывается выбранной библиотекой, также картинки масштабировались до размера 128×128, и выборка разбивалась на тренировочную и тестовую в соотношении 60:40. Так же в нашем случае для более трудоемкой по памяти задачи с применением стека автокодировщиков в 4 лабораторной мы уменьшили размер изображений до 40×40. Все данные  в .rec доступны по ссылкам:
  * 128×128 Train https://yadi.sk/d/xGTDcW4E3SFKsA
  * 128×128 Test https://yadi.sk/d/_03yYTS53SFLDy
  * 40×40 Train https://yadi.sk/d/36QFvQjx3SR3rD
  * 40×40 Test https://yadi.sk/d/dYxt5erw3SR3sG
  
