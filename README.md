# ML Algorithms

| Algorithm | How to solve | Equations to remember | Dataset |
|:---------:|--------------|:---------------------:|---------|
| HGS | 1. Посчитать дефолтный $HSET$ для всех атрибутов и посчитать его $SCORE$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/1bea9db2-7ca6-4dda-b3d9-ee84e3f0fc90) <br /> 2. Сделать $SPEC$ set, в котором будут возможные вариации решения алгоритма ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/4091af2d-73b9-4c1b-a35f-5b205fa6e4ff) <br /> 3. Посчитать $SCORE$ всех $O_{n}$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/09e4d28d-f2cb-4991-92d8-cb0ee8003bc7) <br /> 4. Выбрать тот, который больше $SCORE(HSET)$ и если их больше одного, не забыть учитывать: $BS - Beam Size$ - для следующего HSET. ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/933c15d7-b93a-4d48-8759-2a673abf0535) <br /> 5. Алгоритм заканчивается, когда $SCORE(O_{n}) = 1$| $SCORE = \frac{P_{c}+N_{ne}}{P + N}\$ <br /> $P_{c}$ - количество **позитивных покрытых** примеров <br /> $N_{ne}$ - количество **негативных непокрытых** примеров| <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/f358bacd-684f-4dbe-acd6-7ef613e90668"  width="1500" > |
| NCD Etalony | 1. Подставим данные в табличку с каждого класса($Z$ и $CH$ в данном случае), эталон будет то, что повторяется чаще всего ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/285c8d1d-2551-4592-80f4-a761e87e177b) <br /> 2. Далее подставляем наши эталоны к каждому примеру и считаем, сколько элементов не подходит нашему эталону. <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/60413307-7c5d-447e-a6f8-b42f06e67c8a"  height="300" > <br /> 3. В классификации мы смотрим, совпадают ли числа у классов, если нет - заканчиваем решение; если да, то мы берём пример с этой строки и подставим его для расчёта следующего эталона. ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/e38f94da-4f63-4aec-82a5-443b830cebcd)![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/d58aa911-e43d-45d0-9af7-ee2b9fcafdd1) <br /> `4.` Повторяем 2-ой и 3-ий шаги для наших эталонов, после чего смотрим где числа не равны(кроме наших эталонов) => это будут примеры для новых эталонов  ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/c00c171f-deb2-48fc-b503-7ded42a77eae) <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/d19e58ff-7ef9-4287-be54-d27cd7af1b05"  height="300" > <br /> `5.` наверно случайно убираем один из примеров (и повторяем 4-ый и 5-ый шаги до конца) ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/97e0b1a3-b018-44f0-b05a-59ca9b51280c) <br /> `6.` Записать $DISJUNKTS$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/8c3b92a4-3d02-49b1-9e5c-fa1927fc962e)| ... | <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/ade8f7d8-7dc0-4f15-8936-5201222deb4d"  width="1500" > |
| Naive Bayes | 1. Считаем правдоподобности для каждого аттрибута: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/9ddc6712-c975-47b5-bddb-1140e08ab40c) <br /> 2. Считаем каждый пример при помощи формулы Баеса и классифицируем(результаты классификации добавляем справа от нашей таблицы с примерами): ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/196aeb48-c1ad-41da-89d6-11528dacdf67) <br /> 3. TP что правильно +; TN что правильно -; FN что -, но надо +; FP что +, но надо -; ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/d9817fd7-cdcc-4a2f-9172-c1cfe58e106e) <br /> 4. Считаем Acc, Recall, Pres: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/1a6bfd79-88c3-4efb-9d55-aefc55996f6b)![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/e66dc390-e981-436d-ae8f-ad55eb09261d) | $P(C_{k}/T) = \frac{P(C_{k})*Π P(V_{ij}/C_{k})}{∑_{i=1}^{2}[P(C_{ik})*Π P(V_{ij}/C_{ik})]}$ <br /> $Precision = \frac{TP}{TP + FP}$ <br /> $Recall = \frac{TP}{TP + FN}$ <br /> $F1 = 2 * \frac{Precision * Recall}{Precision + Recall}$ <br /> $Accuracy = \frac{TP + TN}{n}$ <br /> n - кол-во всех примеров | <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/67b51766-a127-408d-b53f-046d177c5de8"  width="1500" > |
| SVM | ... | ... | ... |
| AQ11 | 1. Создаём сеты отрицательных(E1) и положительных(E2) примеров: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/5673b6e9-2a98-44ef-9e5c-35cf8a0d06cb) <br /> 2. Исходя из того, какой сет больше, мы начинаем сравнивать элементы одного сета(где больше элементов) с элементами другого сета(где меньше элементов) и в результат записываем данные второго сета, которые отличаются от первого: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/846efa6f-e0dc-45dc-bebe-bcc98f1ea3ba) <br /> 3. Далее мы смотрим что повторяется во всех результатах, если такого элемента нет, смотрим какой аттрибут присутствует во всех результатах и выбираем то, что подходит по логике выражение (оно может можеть = или ≠ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/0615d948-8726-4c7b-b946-534ea7ca2b77))![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/8f6a0a58-73cd-4c05-aabd-bdb7e959a4aa) <br /> 4. Подставляем все результаты (где мы считали $E2$) и создаём ещё одно условие: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/9926d50d-92cb-41f9-8d91-ea92a3c1d413) <br /> 5. Записываем правила(они всегда возвращают минус): ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/d7dcd068-9b22-4961-a508-fc7bd4e71068) | Distributivny Zakon: $(a ˅ b)˄(c ˅ d) = ac˅ad˅bc˅bd$ | <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/ff9e60cb-b3ba-41fd-bbae-2c202c4bf0f6"  width="1500" > |
| CN2 | 1. Считаем по формулам значения для каждого $A$, выбераем лучшие вариатны и учитываем BM : ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/ffbc5557-c9da-4c10-b40b-5b66f970f3d7) | $Signif(общий) = 2*(∑_{+} + ∑_{-})$ <br /> $Signif(∑+) = ∑ +(K_{r} * log_{2}[\frac{K_{r}}{K} × \frac{N}{N_{r}}])$ <br /> $Signif(∑-) = ∑ -(K_{r} * log_{2}[\frac{K_{r}}{K} × \frac{N}{N_{r}}])$ <br /> $N$ - кол-во TP <br/> $R$ - кол-во классов(T) <br/> $N_{r}$ - кол-во TP класса r(+ или - например) <br/> $K$ - кол-во всех "X", которые есть в датасете <br /> $K_{r}$ - кол-во всех "X", которые есть в датасете и которые подходят под r(+ или -) | <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/550b51d3-b513-4be0-a0cb-6046b2cbd05e"  width="1500" > |
| HCT | 1. Записываем координаты положительных и отрицательных точек в сет, записываем аттрибуты($x, y$ например), рандомно создаём первый сет, а пороговое значение(T) равно числу элементов в сете аттрибутов, считаем $SCORE$ для нашего $H$: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/1863aadc-3142-4a43-b424-4ff7cdcd0281) 2. Смотрим, какие операции мы можем использовать(если никакую, то конец алгоритма), в нашем случае только первую, тк мы можем уменьшить T до 1: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/2fc9e311-bcfe-45d5-bb2d-0563be2a4424) <br /> 3. Повторяет 2 шаг, тут мы можем использовать вторую операцию, тк мы можем добавить ещё одно условаие из-за количества аттрибутов: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/eae09e00-97ab-4362-aa02-5d80a3428d11) <br /> 4. Выбираем наибольший $SCORE$ и записываем условие: ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/655ad1d4-5ae8-496e-a8cd-47e98d4c9ce3) | $SCORE(H) = P_{c} + N_{ne}$ <br /> OP1: удалить условие и снизить пороговое значение(T) <br /> OP2: постоянное пороговое значение(T) и добавить условие | <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/64b7b88f-1e24-44a0-9905-062952e98fc6"  width="1500" > |
| IWP | 1. Создаём уравнение $w_1 x_1 + w_2 x_2 = w_0$ , где $x_1$ это x, а $x_2$ это y. [ $w_0, w_1, w_2$ ] - рандомные числа в интервале от <-1, 1> и посчитаем для него $SCORE(H)$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/7f59f0d5-37f4-43ca-b3a8-3cbaeaec7018)![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/b0058f4e-6491-44a9-851e-92e0361a583c) <br /> 2. Создадим таблицу со всеми нашими данными ($x_{0j}$ **всегда -1**)![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/c703d302-7477-4e77-81c5-57db424d6d2c) <br /> 3. Посчитаем $U_{0j}$ и потом рассортируем по модулю в порядке убывания ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/42dbe25e-cc94-49d4-9ff6-47cbdbc006c3)![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/bef4603b-48d7-4a08-ad50-382085a11e5e) <br /> 4. Посчитаем наше $w_{0}^{'}$ , посчитаем $V_{j}$ и посчитаем $SCORE$ для селекции, где мы выбираем $SCORE > SCORE(H)$ ![image](https://github.com/CoolmixZero/ml-algorithms/assets/107999456/db3045fb-c3de-4edd-87a1-5a66e18e3abe) <br /> 5. То, что мы выбрали теперь является $H$ и мы повторяем все действия до того момента, пока не получим $SCORE = 1$| $U_{kj} = \sum_{i≠k}\frac{w_{i}*x_{ij}}{x_{kj}}$ <br /> $V_{j} = ∑_{i=0}^{n} w_{i}*x_{ij}$ <br /> $SCORE(LTU) = \frac{P_{c}+N_{ne}}{P + N}$ <br /> $w_{k}^{'} = \frac{U_{kj}^{'}+U_{kj+1}^{'}}{2}$| <img src="https://github.com/CoolmixZero/ml-algorithms/assets/107999456/64949c58-c26c-43fc-a958-be9b45c8f86e"  width="1500" > |
| R1 | ... | ... | ... |
| Decision Tree C.45 | ... | ... | ... |
| Decision Tree ID3 | ... | ... | ... |
| VSS | ... | ... | ... |
