# Станція

## Підключення

```мавка
взяти "станція/0.1.0"
```

## Структура

```мавка
структура Станція
  дії словник = ()
  
  покласти(д Дія) ніщо
  запустити(порт число = 8080, зворот Дія або пусто = пусто) ніщо
кінець
```

## Використання

```мавка
взяти "станція/0.2.0"

дія отримати_користувачів()
  [(імʼя="Давид")]
кінець

ск = станція.Станція()

ск.покласти(отримати_користувачів)

ск.запустити(8080, (): друк("Станцію запущено!"))
```
