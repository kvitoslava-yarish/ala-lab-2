# Теоретичні запитання
### 1. Що таке власне значення і власний вектор матриці? Як вони обчислюються? 
Власний вектор - це вектор, який зберігає свій напрямок після проходження лінійного перетворення. Власне значення - це скалярне значення, на яке власний вектор множився під час лінійного перетворення.

![equation](https://latex.codecogs.com/svg.image?\phi\mathbf{x}=\lambda\mathbf{x})

Для обчислання власного числа треба розв'язати характеристичне рівняння:

![equation](https://latex.codecogs.com/svg.image?\det(A-\lambda&space;I)=0\;)

Потім для кожного власного числа знайти власні вектори:

![equation](https://latex.codecogs.com/svg.image?(A-\lambda&space;I)\mathbf{x}=0\;)

### 2. Які властивості мають власні вектори симетричних матриць? 
1. Всі власні значення симетричної матриці є дійсними числами.
2. Власні вектори, що відповідають різним власним значенням, є ортогональними.
3. Будь-яка симетрична матриця може бути діагоналізована
   
### 3. Які можуть бути недоліки використання PCA, і які стратегії можуть використовуватися для подолання цих недоліків? 

1. Інформація (наприклад певній аутлаєри) можуть бути втрачені через зменшення розмірності даних.
   
- Застосування коректної нормалізації або стандартизації даних перед PCA для зменшення чутливості до великих значень або викидів у вхідних даних.
- Використання більшої кількості компонент для зменшення розміроності даних.

2. Розмір матриці коваріативності (наприклад розмір вхідних даних становить M x N, а кількість n. То розмір матриці коваріативності становитиме MN x MN)

- використання підвидів PCA, в яких врахований цей аспект ( рандомізованого PCA (RPCA), інкрементального PCA (IPCA)б згорткового PCA (CPCA))

### 4. Які переваги має діагоналізація матриці в криптографії? Як вона застосовується для шифрування та дешифрування повідомлень? 
1. Простота обчислень det, inversed
2. Менше займає місця ( по-суті треба зберігати лише головну діагональ)
---
1. **Симетричне шифрування:**
В симетричному шифруванні одна і та ж діагональна матриця використовується для шифрування та дешифрування. Ключом є сама діагональна матриця (D):

   **Шифрування** 
   
   C=D⋅M
   
   **Дешифрування**
   
   M=D−1⋅C

2. **Асиметричне шифрування:**

В асиметричному шифруванні, як в RSA, діагональна матриця може використовуватися як частина публічного. А оберенна відповідно виступати в ролі приватного ключа
   
