# Сравнение составляющих градиента давления, скоростей жидкости и газа и holdup фактора Pipesim и макросов #

### Описание и скриншоты ###

Сравнение проводилось с помощью построения КРД, гидравлического градиента давления, градиента давления на трение, скорости жидкости в стволе скажины, скорости газа в стволе скажины, объемного содержания жидкости в многофазном потоке

Для построение КРД по макросам использовались следующие входные данные:

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/%D0%94%D0%B0%D0%BD%D0%BD%D1%8B%D0%B5.PNG)


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

Задаемся устьевым давлением и дебитом, а также ГФ
![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/j.PNG)

В результате получаем точки построения составляющих градиента и их графики


### Результаты ###
Результаты показали, что макросы хорошо сходятся с симулятором PipeSim в широком диапазоне значений дебитов и ГФ и при различных значениях плотностей, диаметров, глубин и температур. Относительная погрешность составляет не больше 5 %

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/pnew.png) 

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/T.png) 

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/ggnew.png) 

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/fg.png) 

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/ag.png) 

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/vsg.png) 

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/vsl.png) 

![Image alt](https://github.com/khabibullinra/unifloc_vba/blob/artem/%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5/%D0%A1%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%20%D0%B3%D1%80%D0%B0%D0%B4%D0%B8%D0%B5%D0%BD%D1%82%D0%B0/lhu.png) 
 
 
 ### Возможные причины расхождения ###
 1. Макросы не учитывают градиент давления на трение.
 2. Макросы для расчета Z фактора, в отличии от Pipesim, используют формулы Дранчука
 3. В макросах температура не расчитывается, а задается. В данном случае линейно, поэтому и пришлось подгонять температуру в Pipesim с помощью U-фактора
 
 Последние изменения в макросах и файл сравнения были сделаны 29.11.2018
 
 Киян Артем
 
 mega.kiyan@mail.ru

