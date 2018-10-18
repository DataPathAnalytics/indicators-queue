###############################################################
Доступ до API черги процедур, що перевірені ризик індикаторами.
###############################################################

**********
Суть черги
**********

З метою контролю за здійсненням процедур державних закупівель у законі України “Про публічні закупівлі” введене поняття “автоматичного індикатора ризику”. За допомогою цих індикаторів перевіряються усі державні закупівлі, що регулюються законом “Про публічні закупівлі” на предмет відповідності до норм та принципів цього закону а також інструкцій та розпоряджень державних органів, що регулюють державні закупівлі. В процесі перевірки ризик індикаторами кожна перевірена процедура закупівлі займає своє місце у списку перевірених процедур. Цей впорядкований список ми будемо називати *чергою*. Даний АРІ слугує для передавання черги процедур, після їх перевірки ризик індикаторами, до органів державного контролю для подальшої перевірки.

************
Описання API
************

В результаті роботи алгоритму  генерується список процедур, що розбитий на сторінки та поділений на колонки за ступенем ризику, процедури, на які потрібно звернути увагу у першу чергу, маркуються червоним кольором (поле ``topRisk = TRUE``).   Згенерований список видається у вигляді JSON структури по протоколу HTTP.

***************
Доступ до черги
***************

Доступ до черги надається за `посиланням <http://195.201.111.52:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%BC.%20%D0%9A%D0%B8%D1%97%D0%B2>`_

****************************************
Можливі помилки при з'єднанні та їх коди
****************************************

**404 - Incorrect link was entered** -  Перевірте посилання, за яким намагаєтесь отримати доступ

**500 - Server connection error**.


*************************
Запити на отримання черги
*************************

`Доступ до черги процедур з низьким ступенем ризику. <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/low?limit=100&page=0&region=%D0%BC.%20%D0%9A%D0%B8%D1%97%D0%B2>`_

`Доступ до черги процедур з середнім ступенем ризику. <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/medium?limit=100&page=0&region=%D0%BC.%20%D0%9A%D0%B8%D1%97%D0%B2>`_ 

`Доступ до черги процедур з високим ступенем ризику. <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/high?limit=100&page=0&region=%D0%BC.%20%D0%9A%D0%B8%D1%97%D0%B2>`_

`Доступ до загальної черги процедур. <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%BC.%20%D0%9A%D0%B8%D1%97%D0%B2>`_


****************************
Доступ до черги по областях.
****************************
Для того, щоб дістатися до черги визначеного регіону, потрібно у запиті в параметр "регіон" вставити одне з нижчеперерахованих значень.

`Запорізька область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%97%D0%B0%D0%BF%D0%BE%D1%80%D1%96%D0%B7%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`M. Київ. <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%BC.%20%D0%9A%D0%B8%D1%97%D0%B2>`_

`Черкаська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A7%D0%B5%D1%80%D0%BA%D0%B0%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Івано-Франківська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%86%D0%B2%D0%B0%D0%BD%D0%BE-%D0%A4%D1%80%D0%B0%D0%BD%D0%BA%D1%96%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Миколаївська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%9C%D0%B8%D0%BA%D0%BE%D0%BB%D0%B0%D1%97%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Чернігівська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A7%D0%B5%D1%80%D0%BD%D1%96%D0%B3%D1%96%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Харківська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A5%D0%B0%D1%80%D0%BA%D1%96%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Житомирська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%96%D0%B8%D1%82%D0%BE%D0%BC%D0%B8%D1%80%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Вінницька область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%92%D1%96%D0%BD%D0%BD%D0%B8%D1%86%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Полтавська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%9F%D0%BE%D0%BB%D1%82%D0%B0%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Волинська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%92%D0%BE%D0%BB%D0%B8%D0%BD%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Львівська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%9B%D1%8C%D0%B2%D1%96%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Дніпропетровська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%94%D0%BD%D1%96%D0%BF%D1%80%D0%BE%D0%BF%D0%B5%D1%82%D1%80%D0%BE%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Хмельницька область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A5%D0%BC%D0%B5%D0%BB%D1%8C%D0%BD%D0%B8%D1%86%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Одеська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%9E%D0%B4%D0%B5%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Київська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%9A%D0%B8%D1%97%D0%B2%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Херсонська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A5%D0%B5%D1%80%D1%81%D0%BE%D0%BD%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Рівненська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A0%D1%96%D0%B2%D0%BD%D0%B5%D0%BD%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Закарпатська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%97%D0%B0%D0%BA%D0%B0%D1%80%D0%BF%D0%B0%D1%82%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Донецька область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%94%D0%BE%D0%BD%D0%B5%D1%86%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Чернівецька область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A7%D0%B5%D1%80%D0%BD%D1%96%D0%B2%D0%B5%D1%86%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Луганська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%9B%D1%83%D0%B3%D0%B0%D0%BD%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Сумська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A1%D1%83%D0%BC%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Кіровоградська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%9A%D1%96%D1%80%D0%BE%D0%B2%D0%BE%D0%B3%D1%80%D0%B0%D0%B4%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_

`Тернопільська область <http://95.216.36.61:8026/api/v0.1/region-indicators-queue/?limit=100&page=0&region=%D0%A2%D0%B5%D1%80%D0%BD%D0%BE%D0%BF%D1%96%D0%BB%D1%8C%D1%81%D1%8C%D0%BA%D0%B0%20%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D1%8C>`_


******************************************
Структура згенерованої відповіді на запит.
******************************************

Блок інформації про сторінку
============================

.. code ::  


    Pagination:
          {
            nextPage:
            
 		    {
                      Path: string

                      Url: string

                    }

            previousPage:
            
                    {
                      Path: string

                      Url: string

                    }

            totalPages:  integer

            totalElements:  integer

          }
          
Де: 

-  ``nextPage`` - адреса наступної сторінки;

-  ``previousPage`` - адреса попередньої сторінки;

-  ``totalPages`` - загальна кількість сторінок;

-  ``totalElements`` - загальна кількість процедур у черзі.


Блок інформації про чергу.
==========================

.. code ::  

    queueInfo:
    
 	    {
                queueId:  integer
                
                impactCategory:  string
            
            
            tenderScoreRange:
            
                            {
                                Max: number
                                
                                Min:  number (double)
                                
                             }
                             
            numberOfTopRiskedTenders:  integer
             
            topRiskPercentage:  number (double)
            
            expectedValueImportanceCoefficient:  number (double)
            
            tenderScoreImportanceCoefficient:  number (double)
            
	    dateCreated:  string (date-time)
    }


Де:

-  ``queueId`` - автоматично згенерований номер перерахунку черги.

-  ``impactCategory`` - категорія ризиковості процедур черги. 

-  ``tenderScoreRange`` - порогові значення сили ризику процедур в даній категорії. 

-  ``numberOfTopRiskedTenders`` - кількість процедур, що маркуються пріоритетними через великий параметр матеріальності їх  замовника. 

-  ``topRiskPercentage`` - відсоток процедур, що будуть маркуватися як пріорітетні.

-  ``expectedValueImportanceCoefficient`` - значення коефіцієнту при очікуваній вартості процедури для визначення критерію матеріальності.

-  ``tenderScoreImportanceCoefficient`` - значення коефіцієнту при силі ризику процедури для визначення критерію матеріальності.

-  ``dateCreated`` - дата створення даного перерахунку черги.


Блок інформації про процедуру.
==============================

.. code ::

    data:
    [
        {   
            tenderOuterId:  string
            
            tenderId:  string
            
            expectedValue:  number (double)
            
            materialityScore:   number (double)
            
            tenderScore:  number (double)
            
            procuringEntityId:  integer (int64)
            
            topRisk: boolean
            
            Region:  string
            
            impactCategory:  string
	 }
    ]

Де:

-  ``tenderOuterId`` - ідентифікатор процедури з АРІ Прозорро.

-  ``tenderId`` - ідентифікатор процедури, що є зручним для людини.

-  ``expectedValue`` - очікувана вартість процедури.

-  ``materialityScore`` - параметр матеріальності процедури.

-  ``tenderScore`` - сила ризику процедури.

-  ``procuringEntityId`` - ідентифікатор замовника процедури.

-  ``topRisk`` - логічна змінна, що позначає, чи треба маркувати процедуру як пріоритетну.

-  ``Region`` - регіон проведення процедури.

-  ``impactCategory`` - категорія ризиковості процедур, до якої відноситься дана процедура.


