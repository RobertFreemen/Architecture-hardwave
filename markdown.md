markdown

# Вариант 4
## Задание 1
$(X>4)$ v $\overline{(X>1)}$ v $(X>4)$ при $X = 4$

**Решение:**
Подставим значение $X = 4$:
- $(4>4)$ v $\overline{(4>1)}$ v $(4>4)$
- $(4>4)$ $\rightarrow$ Ложь (0)
- $(4>1)$ $\rightarrow$ Истина (1)
- $\overline{\text{Истина}}$ $\rightarrow$ Ложь (0)
- $(4 > 4)$ $\rightarrow$ Ложь (0)
- $\text{Ложь}$ $\lor$ $\text{Ложь}$ $\lor$ $\text{Ложь}$
- Итоговый результат: Ложь (0)

**Ответ:** Выражение ложно (0).

---

## Задание 2

**Условие:**
Если прямая параллельна каждой из двух пересекающихся плоскостей, то она параллельна и линии их пересечения.

Простые высказывания:
* $A$ = Прямая параллельна первой плоскости
* $B$ = Прямая параллельна второй плоскости
* $C$ = Прямая параллельна линии пересечения плоскостей

Логическая формула:
$(A \wedge B) \rightarrow C$

**Ответ:** $(A \wedge B) \rightarrow C$

---

## Задание 3

**Исходное логическое выражение:**

$$ \overline{(\overline{X} \wedge (Y \vee Z))} \vee ((\overline{X} \rightarrow \overline{\overline{Y}}) \vee Z) $$

---

### 1. Преобразование левой части выражения
  $$ \overline{\overline{X} \wedge (Y \vee Z)} $$

  $$ \overline{\overline{X}} \vee \overline{(Y \vee Z)} $$

  $$ X \vee \overline{(Y \vee Z)} $$
 
  $$ X \vee (\overline{Y} \wedge \overline{Z}) $$

  $$ (X \vee \overline{Y}) \wedge (X \vee \overline{Z}) $$

### 2. Преобразование правой части выражения
Упростим вторую часть выражения, используя правила раскрытия импликации ($A \rightarrow B \equiv \overline{A} \vee B$) и снятие двойного отрицания ($\overline{\overline{Y}} \equiv Y$):

  $$ (\overline{X} \rightarrow \overline{\overline{Y}}) \vee Z $$

  $$ (\overline{X} \rightarrow Y) \vee Z $$

  $$ (\overline{\overline{X}} \vee Y) \vee Z $$

  $$ X \vee Y \vee Z $$

### 3. Финальный результат
Соединяем упрощенную левую и правую части через внешнее **ИЛИ ($\vee$)**:
$$ F = X \vee \overline{(Y \vee Z)} \vee X \vee Y \vee Z $$
$$ F = X \vee (Y \vee Z) \vee \overline{(Y \vee Z)} $$

По закону исключенного третьего выражение $(Y \vee Z) \vee \overline{(Y \vee Z)} \equiv 1$. Следовательно:
$$ F = X \vee 1 \equiv 1 $$

**Ответ:** $F = 1$


### Таблица истинности



| X | Y | Z | F |
| :---: | :---: | :---: | :---: |
| 0 | 0 | 0 | **0** |
| 0 | 0 | 1 | **1** |
| 0 | 1 | 0 | **1** |
| 0 | 1 | 1 | **1** |
| 1 | 0 | 0 | **1** |
| 1 | 0 | 1 | **1** |
| 1 | 1 | 0 | **1** |
| 1 | 1 | 1 | **1** |

- [Схема задания 3](https://www.falstad.com/s.py?s=n2qntH)
- [Taблица Excel](/excel/Таблица.xlsx)

---

## Задание 4

**Исходное логическое выражение:**

$$ \overline{(\overline{A} \wedge B)} \wedge \overline{(B \vee A)} $$


### 1. Преобразование первой части выражения по закону де Моргана:

$$ \overline{\overline{A} \wedge B} = \overline{\overline{A}} \vee \overline{B} = A \vee \overline{B} $$

### 2. Преобразование второй части выражения по закону де Моргана:

$$ \overline{B \vee A} = \overline{B} \wedge \overline{A} = \overline{A} \wedge \overline{B} $$

### 3. Финальный результат

$$ (A \vee \overline{B}) \wedge (\overline{A} \wedge \overline{B}) $$

$$ (A \wedge \overline{A} \wedge \overline{B}) \vee (\overline{B} \wedge \overline{A} \wedge \overline{B}) $$

Упрощаем полученные слагаемые:
* В первой скобке элемент $A \wedge \overline{A}$ равен $0$:

$$ 0 \wedge \overline{B} = 0 $$

* Во второй скобке повторяющийся элемент $\overline{B} \wedge \overline{B}$ равен просто $\overline{B}$:

$$ \overline{B} \wedge \overline{A} = \overline{A} \wedge \overline{B} $$

$$ 0 \vee (\overline{A} \wedge \overline{B}) = \overline{A} \wedge \overline{B} $$

**Ответ:** $\overline{A} \wedge \overline{B}$

---

### Таблица истинности

| A | B | F |
|:-:|:-:|:-:|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

- [Таблица Excel](/excel/Таблица%20задание%204.xlsx) 

---

## Задание 5

**Исходное логическое выражение:**

$$ ((\overline{X} \leftrightarrow \overline{Y}) \rightarrow (\overline{Y} \rightarrow \overline{X})) \lor (X \land \overline{Y}) $$

---

## Решение по методике преподавателя

Выполним упрощение логического выражения, используя главное правило раскрытия импликации с доски:
$$ A \rightarrow B \equiv \overline{A} \lor B $$

### 1. Предварительное раскрытие базовых импликаций:
 
  $$ \overline{X} \rightarrow \overline{Y} \equiv X \lor \overline{Y} $$

  $$ Y \rightarrow X \equiv \overline{Y} \lor X $$

  $$ X \rightarrow \overline{Y} \equiv \overline{X} \lor \overline{Y} $$

### 2. Преобразование левой части выражения:

$$ X \lor \overline{Y} \lor \overline{X} \lor \overline{Y} $$

### 3. Упрощение по закону исключенного третьего:
Группируем элементы $X$ и $\overline{X}$:
$$ (X \lor \overline{X}) \lor \overline{Y} $$

По закону исключенного третьего пара $X \lor \overline{X}$ всегда дает единицу ($1$):
$$ X \lor \overline{X} = 1 $$

Получаем выражение:
$$ 1 \lor \overline{Y} $$

$$ 1 \lor \overline{Y} = 1 $$

### 4. Финальный результат:

$$ 1 \lor (X \land \overline{Y}) = 1 $$

**Ответ:** $F = 1$

---

### Таблица истинности

| X | Y | F |
| :-: | :-: | :-: |
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |
