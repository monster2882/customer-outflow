# Прогнозирование оттока клиентов от GeekBattle, кейс от Сбера

## Задача

На основе личных параметров клиентов необходимо обучить модель для прогнозирования оттока зарплатного клиента физического лица (ФЛ).

## Метрика

В качестве ключевой метрики оценки модели выбран AUC-ROC.

## Обработка данных

Для улучшения процесса обучения модели мы выполняем следующие шаги:

- **Нормализация данных**: Применяем нормализацию для улучшения процесса обучения.
- **Борьба с несбалансированными классами**: Используем технику подвыборки с помощью `RandomUnderSampler` для уравнивания классов.
- **Коррекция дисбаланса классов**: Вычисляем веса для каждого класса с использованием функции `compute_class_weight` из `sklearn.utils.class_weight`. Эти веса используются при обучении модели для снижения влияния преобладающих классов и улучшения обобщающей способности модели на менее представленных данных.

## Решение

В рамках решения задачи мы использовали алгоритм **CatBoost**, который показывает отличные результаты в задачах классификации и регрессии, особенно при работе с категориальными данными.



