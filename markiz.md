markiz

# Вариант 4
## Задание 1

$$ f(x, y, z) = \Big(\big(((x \mid y) \downarrow z) \mid y\big) \downarrow z\Big) $$

#### 1. Аналитическое преобразование (по правилу де Моргана с доски)

1. Применим закон де Моргана к первой скобке (как показал преподаватель):
   $$ x' \cdot y' \cdot z' = \overline{x \vee y \vee z} $$

2. Подставим обратно в исходную функцию:
   $$ f(x, y, z) = \overline{(x \vee y \vee z)} \oplus (x \cdot y \cdot z) $$

3. Раскроем сложение по модулю 2 ($A \oplus B = (A \cdot B') \vee (A' \cdot B)$):
   $$ f(x, y, z) = \big(\overline{(x \vee y \vee z)} \cdot (x \cdot y \cdot z)'\big) \vee \big((x \vee y \vee z) \cdot (x \cdot y \cdot z)\big) $$

4. Упростим оба слагаемых:

   $\overline{(x \vee y \vee z)} \cdot (x' \vee y' \vee z') = x' \cdot y' \cdot z'$ 

   $(x \vee y \vee z) \cdot (x \cdot y \cdot z) = x \cdot y \cdot z$

**Упрощённый вид (СДНФ):**
$$ f(x, y, z) = (x' \cdot y' \cdot z') \vee (x \cdot y \cdot z) $$



| X | Y | Z | F |
| :---: | :---: | :---: | :---: |
| 0 | 0 | 0 | **0** |
| 0 | 0 | 1 | **0** |
| 0 | 1 | 0 | **0** |
| 0 | 1 | 1 | **0** |
| 1 | 0 | 0 | **0** |
| 1 | 0 | 1 | **0** |
| 1 | 1 | 0 | **1** |
| 1 | 1 | 1 | **0** |

- [Таблица excel](/excel/Таблица%20для%20мк1.xlsx)
