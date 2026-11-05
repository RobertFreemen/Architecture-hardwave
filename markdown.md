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

### 3. Объединение и минимизация
Соединяем упрощенную левую и правую части через внешнее **ИЛИ ($\vee$)**:
$$ F = X \vee \overline{(Y \vee Z)} \vee X \vee Y \vee Z $$
$$ F = X \vee (Y \vee Z) \vee \overline{(Y \vee Z)} $$

По закону исключенного третьего выражение $(Y \vee Z) \vee \overline{(Y \vee Z)} \equiv 1$. Следовательно:
$$ F = X \vee 1 \equiv 1 $$

**Ответ:** ы($F = 1$).


### Таблица истинности (скрипт расчета)



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

**Ответ:** $X \vee Y \vee Z$
