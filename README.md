# EE232-Project

EE232 Project : Publication in China

In this project, we first analyzed the trend of **the total population**, **male and female population**, **urban and rural population** since the founding of the People's Republic of China. The we analyzed the population flow and the variation trend in recent years from the aspects of **economy**, **education**, **population structure** and so on. In addition, we manage to predict the total population of China in the next 50 years by the LSTM network.

## Analysis of population data in recent years

We have counted China's population data from 1949 to 2020. From the whole picture we can see very clearly that the following major historical events had made an impact on population trend, such as **Three years of natural disasters(三年自然灾害)**, the **reform and opening-up(改革开放)** policy and **Family planning(计划生育)**.

![image](https://user-images.githubusercontent.com/50920785/147948533-16c7b03b-53b0-4659-8a40-bb6709c76b44.png)

## The population in each province

After an overall analysis of population changes, we further refined the scale and conducted an analysis on the population data of all the provinces in the past two decades.

![image](https://user-images.githubusercontent.com/50920785/147948773-392b8311-6275-4097-981c-d69ac19cc995.png)

It can be seen from the results that Guangdong, Shandong and Henan provinces have become the three most populous provinces since 2000. From the perspective of time axis, the overall population concentration shows an eastward shift. Among guangdong, Zhejiang, Hebei, Jiangsu and other provinces, the growth rate is particularly prominent. This phenomenon is inseparable from the economic development and economic structure of those regions. After investigation, we found that these coastal areas are mostly handicraft and manufacturing areas, many migrants come to seek better jobs.

## The flow of migrants

To be specific, the migration of migrants across provinces is relatively rare. What is more common is the migration of migrants within the province (for example, there is a large migration of migrants from the surrounding cities of Guangdong Province to Guangzhou). The migration of migrants across provinces is also concentrated in the surrounding provinces, and there is rarely a large-scale influx of migrants over long distances.

Furthermore, although the GDP of Beijing, Shanghai and Zhejiang develops faster, the migrant population is far less than that of Guangdong province. (These provinces and cities are small, expensive and expensive. At the same time, these regional jobs often require education.)

There are also some very interesting phenomena: such as the floating population in Beijing is far less than that in Hebei Province as many people working in Beijing choose to live in Langfang. And the largest inflow to Shanghai comes from Suzhou (Shanghai's back garden).

![image](https://user-images.githubusercontent.com/50920785/147949017-852fa3a0-e185-466f-b80d-e5c9da0ee91f.png)

## Population forecast

If we want to directly analyze the sequence data based on the time axis, the first solution that comes to our minds is to use RNN, LSTM and other similar sequence data models. Here is a brief introduction to the RNN model: In order to reserve the features of one sequence input for the learning of the next sequence input, RNN uses a circular structure to process the sequence data by reserving the features of the last input and adding them to the next data input. However, the LSTM model improved from RNN uses many logic gates to screen some features that should be saved after each input, so that the whole model has long term memory effect.

![image](https://user-images.githubusercontent.com/50920785/147949293-ccd7faa5-2634-4ab5-adab-fb5288f0a31e.png)

It can be seen that by using simple LSTM model to fit one-dimensional population data, we can get an acceptable result:

![image](https://user-images.githubusercontent.com/50920785/147949350-8c37fd26-e8dc-4e2f-bf55-1e771658b214.png)

The final prediction results:

![image](https://user-images.githubusercontent.com/50920785/147949391-f5af1b10-94c6-40d8-98dd-d055a67cf5df.png)

## At the end of the project

For a natural phenomenon, we often expect to find the "pattern" behind the phenomenon, but for a complete society, we often cannot predict the results of social effects precisely. Social policies, the different desires and interests of each individual, and the suspicion of each other affect one's judgment. In this case, there may not even be a "pattern". But just because in such a complex space without patterns, the role of "people" can be brought into full play, and they can influence the whole system by themselves, so as to find a solution to win the game together.

It is because of this social attribute that we can achieve faiths like "human rights are created equal" and "never give up" between people. 

> As Marx Engels said: human nature is the unity of natural and social attributes.

## Acknowledgements

Many thanks to Mr. Jin yaohui and the teaching assistants for their efforts to this course, as well as  all the students who provided us help during this project.







> Data sources of this project: [National Bureau of Statistics of China](http://www.stats.gov.cn/)

