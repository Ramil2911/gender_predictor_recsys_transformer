# Решение кейса «Предсказание гендера по данным браузера»
HSE, 2024

## Описание

- Сфера НТИ: None
- Бизнес-задача: Создание системы для предсказания пола пользователя по данным его браузера для рекламной рекомендательной системы.
- Результат работы: модель предсказания пола пользователя с метрикой ROC-AUC = 0.962

## Запуск решения
Решение польностью представлено в ноутбуке hack.ipynb. Запуск занимает ~27 Гб RAM!

## Модель
Модель представляет из себя параллельные блок трансформера и MLP, где первый блок обрабатывает последователности действий пользователя, а второй входные векторы из таблицы векторов. Выходы этих блоков передаются в fc-слой.

## Пайплайн
1. Чтение и объединение входных таблиц.
2. преобразование транзакционных данных 2d-таблицы в 3d-тензор последовательностей действий каждого пользователя отдельно.
3. Искусственное увеличение датасета в 4 раза путем перемешивания действий пользователя и конкатенации со старыми данными.
4. Обучение модели transfomer+mlp


## Команда
- [Рамиль Габдрахманов]((https://t.me/ramil2911)

## Используемый стек и технологии

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
