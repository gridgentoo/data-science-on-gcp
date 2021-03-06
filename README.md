Оригинальный репозиторий.  
https://github.com/GoogleCloudPlatform/data-science-on-gcp.  

Agile Architecture для аналитики и искусственного интеллекта в облаке Google.  
https://medium.com/google-cloud/an-agile-architecture-for-analytics-and-ai-on-google-cloud-6415e692591f.  

Vertex AI от Google - вобрала в себя все облачные инструменты Google для подготовки наборов данных и обучения ML моделей.  
По замыслу разработчиков Google, команды смогут полностью перенести все ML процессы на Vertex AI: дата-инженеры ищут данные в Google BigQuery, аннотаторы размечают данные с помощью встроенных инструментов, дата-сайентисты настраивают алгоритмы обучения в AutoML и автоматически подбирают оптимальные гиперпараметры. Обученную и протестированную ML модель можно подключить к рабочему приложению в пару кликов — либо загрузить на специально подготовленный сервер в Google Cloud, либо экспортировать в один из популярных форматов.  

![Image alt](https://habrastorage.org/webt/hy/if/nw/hyifnwdmv9usazdat8l3yo9mtqu.png)

Несмотря на всеобъемлемость платформы, разработчики предусмотрели возможность замены любой ее части на самописные решения. Например в этом туториале.  
https://codelabs.developers.google.com/vertex_custom_training_prediction#0.  

показывается как написать свой алгоритм обучения модели, запаковать его в Docker контейнер и встроить его в процесс обучения модели.  
Использование Docker контейнеров позволяет писать код на любом языке программирования и использовать любые библиотеки.  


Как развернуть модель тензорного потока [TensorFlow Model] в Vertex AI.  
https://towardsdatascience.com/how-to-deploy-a-tensorflow-model-to-vertex-ai-87d9ae1df56

Фрагменты кода взяты из этой записной книжки на GitHub.  
https://github.com/GoogleCloudPlatform/data-science-on-gcp/blob/edition2/09_vertexai/flights_model_tf2.ipynb

Разработка и развертывание модели машинного обучения на Vertex AI с использованием Python.  
https://towardsdatascience.com/developing-and-deploying-a-machine-learning-model-on-vertex-ai-using-python-865b535814f8.  

Как построить конвейер MLOps для настройки гиперпараметров в Vertex AI.  
https://towardsdatascience.com/how-to-build-an-mlops-pipeline-for-hyperparameter-tuning-in-vertex-ai-45cc2faf4ff5.  

# data-science-on-gcp

Source code accompanying book:

<table>
<tr>
  <td>
  <img src="https://images-na.ssl-images-amazon.com/images/I/51dgw%2BCYSOL._SX379_BO1,204,203,200_.jpg" height="100"/>
  </td>
  <td>
  Data Science on the Google Cloud Platform, 2nd Edition <br/>
  Valliappa Lakshmanan <br/>
  O'Reilly, Jan 2022
  </td>
  <td>
  Branch <a href="https://github.com/GoogleCloudPlatform/data-science-on-gcp/tree/edition2">edition2</a> [being built]
  </td>
</tr>
<tr>
  <td>
  <img src="https://images-na.ssl-images-amazon.com/images/I/51dgw%2BCYSOL._SX379_BO1,204,203,200_.jpg" height="100"/>
  </td>
  <td>
  Data Science on the Google Cloud Platform <br/>
  Valliappa Lakshmanan <br/>
  O'Reilly, Jan 2017
  </td>
  <td>
  Branch <a href="https://github.com/GoogleCloudPlatform/data-science-on-gcp/tree/edition1_tf2">edition1_tf2</a> (also: main)
  </td>
</table>

### Try out the code on Google Cloud Platform
<a href="https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/GoogleCloudPlatform/data-science-on-gcp&page=editor&open_in_editor=README.md"> <img alt="Open in Cloud Shell" src ="http://gstatic.com/cloudssh/images/open-btn.png"></a>

The code on Qwiklabs (see below) is **continually tested**, and this repo is kept up-to-date.
The code should work as-is for you, however, there are three very common problems that readers report:
* <i>Ch 2: Download data fails.</i> The Bureau of Transportation website to download the airline dataset periodically goes down or changes availability due to government furloughs and the like.
Please use the instructions in 02_ingest/README.md to copy the data from my bucket. The rest of the chapters work off the data in the
bucket, and will be fine.
* <i>Ch 3: Permission errors.</i> These typically occur because we expect that you will copy the airline data to your bucket. You don't have write access to gs://cloud-training-demos-ml/. The instructions will tell you to change the bucket name to one that you own. Please do that.
* <i>Ch 4, 10: Dataflow doesn't do anything.</i>. The real-time simulation requires that you simultaneously run simulate.py and the Dataflow pipeline. If the Dataflow pipeline is not progressing, make sure that the simulate program is still running.

If the code doesn't work for you, I recommend that you try the corresponding Qwiklab lab to see if there is some step that you missed.
If you still have problems, please leave feedback in Qwiklabs, or file an issue in this repo.

### Try out the code on Qwiklabs

- [Data Science on the Google Cloud Platform Quest](https://google.qwiklabs.com/quests/43)
- [Data Science on Google Cloud Platform: Machine Learning Quest](https://google.qwiklabs.com/quests/50)



### Purchase book
[Read on-line or download PDF of book](http://shop.oreilly.com/product/0636920057628.do)

[Buy on Amazon.com](https://www.amazon.com/Data-Science-Google-Cloud-Platform/dp/1491974567)

### Updates to book
I updated the book in Nov 2019 with TensorFlow 2.0, Cloud Functions, and BigQuery ML.
