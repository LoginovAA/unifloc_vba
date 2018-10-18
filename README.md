# Сравнение макросов из надстройки UniflocVBA7.3, старых макросов и симулятора PipeSim #

### Описание и скриншоты ###

Сравнение проводилось с помощью построения КРД для различных случаев и параметров

Для построение КРД по макросам использовались следующие входные данные:
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA.PNG)


Также возможность макросов предусматривает:

1.Выбор PVT корреляций для расчета:
- на основе корелляции Стендинга
- на основе корелляции Маккейна
- упрощенные зависимости

2.Выбор гидравлической корреляции:
- корелляция Беггса и Брилла (BeggsBriilCor) 
- корелляция Ансари (AnsariCor)
- UnifiedCor
- корелляция Грея (Gray)
- корелляция Хадегорна и Брауна (HagedornBrown)
- корелляция Сахарова и Мохова (SakharovMokhov)

Для построение КРД в PipeSim задавались следующими параметрами:

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/Capture1.PNG)

Для лучшей совместимости задавались газосодержанием при давлении насыщения,
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/Capture2.PNG)

Устьевой и пластовой температурой, длиной и диаметром НКТ
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/Capture3.PNG)

Для линейного распределения температуры увеличили U-value multiplier до 30
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/Capture4.PNG)

Как и в макросах используем корреляцию Ансари
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/Capture5.PNG)

Задаемся устьевым давлением и дебитом, а также строим кривые для различных ГФ
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/Capture6.PNG)

В результате получаем точки построения КРД и их графики

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%91%D0%B5%D0%B7%D1%8B%D0%BC%D1%8F%D0%BD%D0%BD%D1%8B%D0%B9.png)
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%91%D0%B5%D0%B7%D1%8B%D0%BC%D1%8F%D0%BD%D0%BD%D1%8B%D0%B92.png)


### Результаты ###
Результаты показали, что макросы хорошо сходятся с симулятором PipeSim в широком диапазоне значений дебитов и ГФ и при различных значениях плотностей, диаметров, глубин и температур
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/1.png)
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/3.png)
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/4.png)
 
 
 Последние изменения в макросах и файл сравнения были сделаны 18.10.2018
 
 Киян Артем
 
 mega.kiyan@mail.ru

