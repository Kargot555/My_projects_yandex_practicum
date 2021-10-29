# Прогнозирование вероятности оттока для фитнесс центров

Заказчик - сеть фитнес-центров "Культурист-датасаентист"

Исходные данные - «Культурист-датасаентист» предоставил сведения в csv-файлах.

Цель исследования:

    научиться прогнозировать вероятность оттока (на уровне следующего месяца) для каждого клиента;
    сформировать типичные портреты клиентов: выделить несколько наиболее ярких групп и охарактеризовать их основные свойства;
    проанализировать основные признаки, наиболее сильно влияющие на отток;
    сформулировать основные выводы и разработать рекомендации по повышению качества работы с клиентами:
        выделить целевые группы клиентов;
        предложить меры по снижению оттока;
        определить другие особенности взаимодействия с клиентами.

## Ход выполнения:

    Открытие данных
    Предобработка данных
        Изучение данных
        Обработка дубликатов
        Обработка пропущенных значений
        Работа с типами данных

Проведите исследовательский анализ данных (EDA):
Постройте модель прогнозирования оттока клиентов:
Сделайте кластеризацию клиентов:
Сформулируйте выводы и сделайте базовые рекомендации по работе с клиентами


Библиотеки

# достаём библиотеки

import matplotlib.pyplot as plt

import pandas as pd

from scipy import stats as st

​

# библиотека сиборн для визуализации на Питоне поверх matplotlib

import seaborn as sns

# Импорт библиотеки высокоуровневых математических функций

import numpy as np

​

from statsmodels.stats.proportion import proportions_ztest

# лаконичный, последовательный, высокоуровневый API для создания фигур

import plotly.express as px

import plotly.graph_objects as go

# уберём warnings

import sys

import warnings

if not sys.warnoptions:

       warnings.simplefilter("ignore")

import datetime as dt

​

# Модуль Re для регулярных выражений в Python

import re

# для построения графика воронки

import plotly.graph_objects as go

from plotly.subplots import make_subplots

# библиотеки для машинного обучения

from sklearn.model_selection import train_test_split

from sklearn.preprocessing import StandardScaler

from sklearn.ensemble import RandomForestClassifier

from sklearn.linear_model import LogisticRegression

from sklearn.metrics import accuracy_score,  precision_score, recall_score

​

# для кластарезации

from scipy.cluster.hierarchy import dendrogram, linkage

from sklearn.cluster import KMeans