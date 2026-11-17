markiz

# Вариант 4
## Задание 1

$$ f(x, y, z) = \Big(\big(((x \mid y) \downarrow z) \mid y\big) \downarrow z\Big) $$

#### 1. Аналитическое преобразование (по правилу де Моргана с доски)

1. Применим закон де Моргана к первой скобке:

$$ x' \cdot y' \cdot z' = \overline{x \vee y \vee z} $$

2. Подставим обратно в исходную функцию:

$$ f(x, y, z) = \overline{(x \vee y \vee z)} \oplus (x \cdot y \cdot z) $$

3. Раскроем сложение по модулю 2 

( $A \oplus B = (A \cdot B') \vee (A' \cdot B)$ )

$$ f(x, y, z) = \big(\overline{(x \vee y \vee z)} \cdot (x \cdot y \cdot z)'\big) \vee \big((x \vee y \vee z) \cdot (x \cdot y \cdot z)\big) $$

4. Упростим оба слагаемых:

$\overline{(x \vee y \vee z)} \cdot (x' \vee y' \vee z') = x' \cdot y' \cdot z'$ 

$(x \vee y \vee z) \cdot (x \cdot y \cdot z) = x \cdot y \cdot z$

Упрощённый вид (СДНФ):

$$ f(x, y, z) = (x' \cdot y' \cdot z') \vee (x \cdot y \cdot z) $$


#### 2. Таблица истинности

#### Таблица истинности для Задания 1

| X | Y | Z | $X \mid Y$ | $(X \mid Y) \downarrow Z$ | $((X \mid Y) \downarrow Z) \mid Y$ | $F$ |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 0 | 1 | **0** |
| 0 | 0 | 1 | 1 | 0 | 1 | **0** |
| 0 | 1 | 0 | 1 | 0 | 1 | **0** |
| 0 | 1 | 1 | 1 | 0 | 1 | **0** |
| 1 | 0 | 0 | 1 | 0 | 1 | **0** |
| 1 | 0 | 1 | 1 | 0 | 1 | **0** |
| 1 | 1 | 0 | 0 | 1 | 0 | **1** |
| 1 | 1 | 1 | 0 | 0 | 1 | **0** |


- [Таблица excel](/excel/Таблица%20для%20мк1.xlsx)

---

## Задание 2

$$x \rightarrow (y \cdot z) = (x \rightarrow y) \cdot (x \rightarrow z)$$

#### 1. Аналитическое доказательство
Используем формулу замены импликации ($A \rightarrow B = A' \vee B$) и дистрибутивный закон:

1. Раскроем импликацию в левой части:
$$x \rightarrow (y \cdot z) = x' \vee (y \cdot z)$$

2. Применим распределительный закон:
$$x' \vee (y \cdot z) = (x' \vee y) \cdot (x' \vee z)$$

3. Свернем скобки обратно в импликации:
$$(x' \vee y) \cdot (x' \vee z) = (x \rightarrow y) \cdot (x \rightarrow z)$$

Левая часть равна правой, тождество доказано.

#### 2. Таблица истинности

| X | Y | Z | $Y \cdot Z$ | $X \rightarrow (Y \cdot Z)$ | $X \rightarrow Y$ | $X \rightarrow Z$ | $(X \rightarrow Y) \cdot (X \rightarrow Z)$ | F |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | **1** |
| 0 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | **1** |
| 0 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | **1** |
| 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | **1** |
| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | **1** |
| 1 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | **1** |
| 1 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | **1** |
| 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | **1** |

- [Таблица excel](/excel/Таблица%20истинности%20для%20дз2%20задан%202.xlsx)