# hse_hw1_meth
https://colab.research.google.com/drive/1p6rcIcnGKTRrzXKew7vHRKpLE8CNlCml?usp=sharing

![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2020.34.06.png)
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2020.33.57.png)
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2020.33.46.png)
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2020.33.38.png)
Вывод: Сравнивая данные для SRR3414630_1 полученные в прошлом дз и текущие данные важно отметить различний GC состав - 2 пика ( цитозина больще в РНК, тимина больше в ДНК, содержание остальных сравнимо и их содержание нормальное - около четверти)
### A Число ридов, закартированных на участки 11347700-11367700; 40185800-40195800  
|                    | 11347700-11367700 | 40185800-40195800 |
|--------------------|-------------------|-------------------|
| Epiblast           | 2328              | 1062              |
| 8 cell             | 1090              | 464               |
| ICM                | 1456              | 630               |

### B Дедупликация 
Сколько процентов прочтений дуплицированно в каждом из образцов? 

|                   |           %           |
|-------------------|-----------------------|
| Epiblast          | 2.92                  |
| 8 cell            | 18.31                 |
| ICM               | 9.08                  |
  
Дупликации связаны с метилированием 

### D Отчет и описание M-bias plot  
8 CELL: примерно 40% СPG метилирования
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2019.33.55.png)
EPIBLAST: примерно 80% СPG метилирования
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2019.34.09.png)
ICM: примерно 20% СPG метилирования
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2019.34.20.png)
  
### E Гистограмма распределения метилирования цитозинов по хромосоме
```
df = pd.read_csv("s_icm.deduplicated.bedGraph", delimiter='\t', skiprows=1, header=None)
plt.figure(figsize=[8, 4])
plt.title("icm")
plt.hist(df[3].values, bins=50, color='aqua')
plt.show()
```
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2019.52.04.png)
примерно половина метилирования приходится на 0%
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2019.52.09.png)
примерно большая часть метилирования приходится на 100% (лучше всего)
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/img/Screenshot%202022-02-18%20at%2019.52.13.png)
 примерно половина метилирования приходится на 0%
### А Визуализируйте уровень метилирования и покрытия для каждого образца 
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/Screenshot%202022-02-21%20at%2017.43.05.png)
![](https://github.com/banochkabb/hse_hw1_meth/blob/main/Screenshot%202022-02-21%20at%2017.43.05.png)
