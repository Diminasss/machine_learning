# Лабораторная работа №6 — перенос обучения на Fruits 360

[Вернуться к общему README](../README.md) · [Открыть блокнот](Lab6.ipynb)

## Цель работы

Сравнить MobileNetV2, InceptionV3 и DenseNet121 при классификации выбранных классов Fruits 360.

Каждая архитектура исследуется в двух режимах: с полностью замороженной предобученной базой и с дообучением последних 20 слоёв. Качество оценивается по accuracy, precision, recall, F1-score и матрице ошибок.

## Модели с замороженной базой

### MobileNetV2

![Матрица ошибок MobileNetV2](diagrams/mobilenetv2-frozen-confusion.png)

![Графики обучения MobileNetV2](diagrams/mobilenetv2-frozen-history.png)

### InceptionV3

![Матрица ошибок InceptionV3](diagrams/inceptionv3-frozen-confusion.png)

![Графики обучения InceptionV3](diagrams/inceptionv3-frozen-history.png)

### DenseNet121

![Матрица ошибок DenseNet121](diagrams/densenet121-frozen-confusion.png)

![Графики обучения DenseNet121](diagrams/densenet121-frozen-history.png)

## Модели после частичного дообучения

### MobileNetV2

![Матрица ошибок дообученной MobileNetV2](diagrams/mobilenetv2-finetuned-confusion.png)

![Графики дообучения MobileNetV2](diagrams/mobilenetv2-finetuned-history.png)

### InceptionV3

![Матрица ошибок дообученной InceptionV3](diagrams/inceptionv3-finetuned-confusion.png)

![Графики дообучения InceptionV3](diagrams/inceptionv3-finetuned-history.png)

### DenseNet121

![Матрица ошибок дообученной DenseNet121](diagrams/densenet121-finetuned-confusion.png)

![Графики дообучения DenseNet121](diagrams/densenet121-finetuned-history.png)

## Запуск

Блокнот подготовлен для Google Colab и загружает Fruits 360 через Kaggle API. Потребуются `tensorflow`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn` и `kaggle`.

Перед запуском добавьте свой `kaggle.json`, проверьте путь к распакованному набору данных и создайте каталог `diagrams/` для сохраняемых графиков. Не публикуйте `kaggle.json`, поскольку он содержит данные доступа к Kaggle.
