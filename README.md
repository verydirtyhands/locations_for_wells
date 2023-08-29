# Выбор локации для скважины

## Описание проекта

Проект направлен на разработку оптимальной стратегии выбора местоположения для бурения новой нефтяной скважины с целью максимизации добычи и прибыли. Для достижения этой цели предлагается комплексный анализ характеристик скважин в трёх различных регионах, создание предсказательной модели для оценки потенциала скважин, выбор наиболее перспективных скважин и анализ рисков с применением метода Bootstrap.

## Инструменты:

`Python==3.9.16`
`Pandas==1.5.3`
`sklearn==1.2.2`
`seaborn==0.12.2`
`matplotlib==3.6.3`
`numpy==1.23.5`
`xgboost==1.7.5`
`pandas_profiling==3.6.6`

## Описание данных:

### место хранения:

Данные геологоразведки трёх регионов находятся в файлах: 
- geo_data_0.csv 
- geo_data_1.csv 
- geo_data_2.csv 

### описание признаков:

- id — уникальный идентификатор скважины;
- f0, f1, f2 — три признака точек (анонимизированные данных);
- product — объём запасов в скважине (тыс. баррелей).

## Краткое описание проведённой работы:
<i> 
Проанализированы зависимости между анонимизированными данными и объёмом запасов в скважине. Построены модели на основе XGBRegressor, LinearRegression, DecisionTreeRegressor, GaussianProcessRegressor ,также были подобраны параметры для XGBRegressor. Bootstrap + проведён расчёт доверительного интервала </i>

## Выводы
<i>В ходе экспериментов с различными моделями наиболее оптимальной была признана модель XGBRegressor. Несмотря на длительное время работы, она продемонстрировала наилучшие результаты с RMSE в размере 37. Однако стоит отметить, что погрешность во втором регионе значительно меньше, что делает его предсказания более точными.

Результаты анализа позволяют с уверенностью заявить, что все регионы являются прибыльными с вероятностью более 90%. Наиболее перспективный оказался второй регион, в котором наблюдается наименьшая погрешность предсказаний. Это говорит о том, что предсказания для данного региона являются наиболее достоверными.

Кроме того, второй регион также обладает наименьшим риском. В сочетании с высокой точностью предсказаний, это делает второй регион наиболее привлекательным вариантом для разработки.</i>

## Рекомендации
<i>Исходя из проведенного анализа и экспериментов с моделями, рекомендуется выбрать второй регион для разработки новой нефтяной скважины. Этот выбор обоснован наименьшей погрешностью предсказаний, что подтверждает их достоверность, а также низким уровнем риска. Таким образом, второй регион обладает наиболее перспективной комбинацией точности и надежности, делая его оптимальным выбором для дальнейшей добычи нефти.
</i>

---

#### Если проект не открывается или вы хотите посмотреть со всеми интерактивными ячейками(plotly,ydata-profiling), его можно открыть по ссылке: <a href='https://nbviewer.org/github/verydirtyhands/locations_for_wells/blob/main/p7f.ipynb'>Выбор локации для скважины</a>
