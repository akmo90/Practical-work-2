# Практическая работа №2  
## Параллельная реализация простых алгоритмов сортировки с использованием OpenMP

---

### Задание

#### 1. Последовательная реализация
Реализованы функции сортировки пузырьком, выбором и вставкой
без использования OpenMP.
<p align="center">
  <img src="schemes/схема1.png" style="width: %; height: auto;">
</p>
---

#### 2. Параллельная реализация с использованием OpenMP
Реализованы параллельные версии алгоритмов сортировки с использованием директив
OpenMP. Параллелизация выполнена преимущественно по внешним циклам.

Тестирование производительности проводилось на массивах размером:
- 1 000 элементов
- 10 000 элементов
- 100 000 элементов


<p align="center">
  <img src="schemes/схема2.png" style="width: %; height: auto;">
</p>
---

#### 3. Сравнение производительности
Для измерения времени выполнения последовательных и параллельных реализаций
использовалась библиотека `<chrono>`.  
На основе полученных результатов проведено сравнение производительности и
сформулированы выводы.

---
### Результаты компиляции
```bash
Array's size: 1000
Bubble Sort (seq): 3 ms
Bubble Sort (OMP): 52 ms
Selection Sort (seq): 0 ms
Selection Sort (OMP): 53 ms
Insertion Sort (seq): 0 ms
Insertion Sort (OMP): 0 ms

Array's size: 10000
Bubble Sort (seq): 307 ms
Bubble Sort (OMP): 546 ms
Selection Sort (seq): 96 ms
Selection Sort (OMP): 521 ms
Insertion Sort (seq): 67 ms
Insertion Sort (OMP): 66 ms
```

### Пример компиляции
```bash
g++ -fopenmp main.cpp -o main
./main.exe
```