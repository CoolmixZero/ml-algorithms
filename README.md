# ML Algorithms

| Algorithm | How to solve | Equations to remember | Dataset |
|:---------:|--------------|:---------------------:|---------|
| HGS | 1. Посчитать дефолтный $HSET$ для всех атрибутов и посчитать его $SCORE$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/1bea9db2-7ca6-4dda-b3d9-ee84e3f0fc90) <br /> 2. Сделать $SPEC$ set, в котором будут возможные вариации решения алгоритма ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/4091af2d-73b9-4c1b-a35f-5b205fa6e4ff) <br /> 3. Посчитать $SCORE$ всех $O_{n}$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/09e4d28d-f2cb-4991-92d8-cb0ee8003bc7) <br /> 4. Выбрать тот, который больше $SCORE(HSET)$ и если их больше одного, не забыть учитывать: $BS - Beam Size$ - для следующего HSET. ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/933c15d7-b93a-4d48-8759-2a673abf0535) <br /> 5. Алгоритм заканчивается, когда $SCORE(O_{n}) = 1$| $SCORE = \frac{P_{c}+N_{ne}}{P + N}\$ <br /> $P_{c}$ - количество **позитивных покрытых** примеров <br /> $N_{ne}$ - количество **негативных непокрытых** примеров| <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/f358bacd-684f-4dbe-acd6-7ef613e90668"  width="1500" > |
| NCD Etalony |  | |
