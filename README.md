# Станція

Пак для віддаленого виконання дій Мавки.

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
взяти "станція/0.1.0"

користувачі = [(імʼя="Давид")]

дія отримати_користувачів()
  вернути користувачі
кінець

дія додати_користувача(імʼя)
  користувачі.додати((імʼя=імʼя))
  вернути користувачі
кінець

ск = станція.Станція()

ск.покласти(отримати_користувачів)
ск.покласти(додати_користувача)

ск.запустити(8080, (): друк("Станцію запущено на http://localhost:8080!"))
```
