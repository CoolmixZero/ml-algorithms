# ML Algorithms

| Algorithm | How to solve | Equations to remember | Dataset |
|:---------:|--------------|:---------------------:|---------|
| HGS | 1. Посчитать дефолтный $HSET$ для всех атрибутов и посчитать его $SCORE$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/1bea9db2-7ca6-4dda-b3d9-ee84e3f0fc90) <br /> 2. Сделать $SPEC$ set, в котором будут возможные вариации решения алгоритма ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/4091af2d-73b9-4c1b-a35f-5b205fa6e4ff) <br /> 3. Посчитать $SCORE$ всех $O_{n}$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/09e4d28d-f2cb-4991-92d8-cb0ee8003bc7) <br /> 4. Выбрать тот, который больше $SCORE(HSET)$ и если их больше одного, не забыть учитывать: $BS - Beam Size$ - для следующего HSET. ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/933c15d7-b93a-4d48-8759-2a673abf0535) <br /> 5. Алгоритм заканчивается, когда $SCORE(O_{n}) = 1$| $SCORE = \frac{P_{c}+N_{ne}}{P + N}\$ <br /> $P_{c}$ - количество **позитивных покрытых** примеров <br /> $N_{ne}$ - количество **негативных непокрытых** примеров| <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/f358bacd-684f-4dbe-acd6-7ef613e90668"  width="1500" > |
| NCD Etalony | 1. Подставим данные в табличку с каждого класса($+$ и $-$ в данном случае), эталон будет то, что повторяется чаще всего ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/a5351605-14d3-4bb4-8ba6-322dad5ccb43) <br /> 2. Далее подставляем наши эталоны к каждому примеру и считаем, сколько элементов не подходит нашему эталону. <br /> 3. В классификации мы смотрим, совпадают ли числа у классов, если нет - заканчиваем решение; если да, то мы берём пример с этой строки и подставим его для расчёта следующего эталона. ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/d884bb98-1410-4d3c-8bd6-98ceef26f0e1) | ... | <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/0a275ddd-2375-4575-8510-08e00a1a0b96"  width="1500" > |
| Naive Bayes | ... | ... | ... |
| SVM | ... | ... | ... |
| AQ11 | ... | ... | ... |
| HCT | ... | ... | ... |
| IWP | ... | ... | ... |
| R1 | ... | ... | ... |
| Decision Tree C.45 | ... | ... | ... |
| Decision Tree ID3 | ... | ... | ... |
| VSS | ... | ... | ... |
