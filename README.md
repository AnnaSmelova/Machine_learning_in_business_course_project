# Курс Машинное обучение в бизнесе

## Итоговый проект

#### Стек:

ML: sklearn, pandas, numpy
API: flask

#### Данные: с kaggle - https://www.kaggle.com/rashikrahmanpritom/heart-attack-analysis-prediction-dataset

#### Задача: предсказать предрасположен ли человек к сердечному приступу или нет. Бинарная классификация.

#### Целевая переменная: output

#### Используемые признаки:

* age - возраст (int64)
* sex - пол (int64)
* cp - тип боли в груди (int64)
* exng - стенокардия, вызванная физической нагрузкой (int64)
* trtbps - артериальное давление в состоянии покоя (в мм рт. ст.) (int64)
* thalachh - достигнутая максимальная частота пульса (int64)

#### Модель: catboost

#### Клонируем репозиторий и создаем образ
'''
$ git clone https://github.com/AnnaSmelova/Machine_learning_in_business_course_project.git
$ cd Machine_learning_in_business_course_project
$ docker build -t flask_app:v0.1 flask_app/
'''

#### Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)
Предобученная модель лежит в Machine_learning_in_business_course_project/prepare_and_check_model/models/
'''
$ docker run -d -p 8180:8180 -p 8181:8181 -v <your_local_path_to_pretrained_models>:/app/app/models flask_app:v0
'''

#### Переходим на localhost:8181

Geek University: факультет Искусственного интеллекта
