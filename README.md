# MNIST_Image_Clustering_KMeans_t-SNE
MNIST_Image_Clustering_KMeans_t-SNE_3.4.1

# Проект: Кластеризация изображений MNIST с использованием KMeans и t-SNE

## Описание проекта
В данном проекте проводится кластеризация изображений рукописных цифр из набора данных MNIST с использованием алгоритма KMeans. Также применяется метод понижения размерности t-SNE для визуализации данных и улучшения качества кластеризации. Проект включает в себя следующие этапы:
1. Загрузка и предварительная обработка данных.
2. Кластеризация данных с помощью KMeans.
3. Визуализация центроидов кластеров.
4. Оценка качества кластеризации с использованием метрик точности.
5. Понижение размерности данных с помощью t-SNE и повторная кластеризация.

## Используемые библиотеки и методы
- **Библиотеки:**
  - `keras.datasets` для загрузки набора данных MNIST.
  - `matplotlib.pyplot` для визуализации данных.
  - `sklearn.model_selection.train_test_split` для разделения данных на обучающую и тестовую выборки.
  - `sklearn.cluster.KMeans` для кластеризации данных.
  - `scipy.stats.mode` для определения моды в кластерах.
  - `sklearn.metrics.accuracy_score` и `confusion_matrix` для оценки качества модели.
  - `sklearn.manifold.TSNE` для понижения размерности данных.
  - `seaborn` и `mpl_toolkits.mplot3d` для визуализации данных в 3D.

- **Методы и алгоритмы:**
  - Алгоритм KMeans для кластеризации данных.
  - Метод t-SNE для понижения размерности данных.
  - Метрика точности (accuracy) для оценки качества кластеризации.
  - Визуализация данных с помощью scatterplot и heatmap.

## Краткое описание проекта
1. **Загрузка данных:** Используется набор данных MNIST, содержащий изображения рукописных цифр размером 28x28 пикселей.
2. **Предварительная обработка:** Данные разделяются на обучающую и тестовую выборки, а затем "распрямляются" для использования в алгоритме KMeans.
3. **Кластеризация:** Применяется алгоритм KMeans для кластеризации данных на 10 кластеров (по количеству цифр).
4. **Визуализация центроидов:** Центроиды кластеров визуализируются в виде изображений, чтобы понять, какие цифры были выделены.
5. **Оценка качества:** Оценивается точность кластеризации с использованием метрик accuracy и confusion matrix.
6. **Понижение размерности:** Данные преобразуются с помощью t-SNE для понижения размерности до 2D и 3D, что позволяет улучшить визуализацию и качество кластеризации.
7. **Повторная кластеризация:** После понижения размерности данные снова кластеризуются, и оценивается точность модели.

## Итоги
- **Точность модели:** На тестовых данных точность модели составила около 59.3%, что указывает на умеренную эффективность кластеризации.
- **Визуализация:** Визуализация центроидов кластеров показала, что алгоритм KMeans смог выделить основные черты цифр, хотя некоторые цифры были перепутаны.
- **Оптимальное количество кластеров:** График каменистой осыпи показал, что оптимальное количество кластеров для данного набора данных находится в диапазоне от 7 до 16.
- **Понижение размерности:** Применение t-SNE позволило улучшить визуализацию данных и повысить точность кластеризации до 82.3% на обучающих данных.

## Про t-SNE
Проблема, однако, известна. t-SNE — метод, который не дает правила получения проекций многомерного пространства на, например, двумерное. Тем самым, при появлении новых данных, проекции придется искать заново.
В то же время, еще раз хочется подчеркнуть, как обучение без учителя позволило построить классификатор, который, как будто бы, является результатом решения задачи обучения с учителем.

## Заключение
Проект демонстрирует применение методов кластеризации и понижения размерности для анализа и визуализации данных. Несмотря на умеренную точность, методы показали свою эффективность в выделении основных черт данных и могут быть использованы для дальнейшего анализа и улучшения моделей.
