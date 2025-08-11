# Project: AndroidRhymeSuggestor (Полная расширенная версия)

## GitHub-репозиторий
Исходный код и инструкции можно найти здесь: **https://github.com/example/AndroidRhymeSuggestor**

## Новые функции
1. **Экспорт/импорт словаря**: сохранение/загрузка слов в JSON-файл в локальном хранилище.
2. **Онлайн-подбор рифм**: через API Datamuse (`https://api.datamuse.com/words?rel_rhy=<слово>&lang=ru`).
3. **Улучшенный подсчёт слогов**: учёт дифтонгов и ударений через встроенный словарь.
4. **Инструкция по сборке в Termux** (ниже).

---

## MainActivity.kt (ключевые изменения)
- Добавлены кнопки **Экспорт** и **Импорт** словаря.
- Поддержка асинхронного вызова API Datamuse.
- Объединение оффлайн и онлайн подсказок.

---

## WordSuggester.kt (ключевые изменения)
- Улучшенный `syllableCount` с учётом дифтонгов.
- При `suggest()` объединяются локальные результаты и онлайн API.

---

## Экспорт/импорт
- Экспорт: сохраняет `words.txt` как `words_export.json` в `getExternalFilesDir(null)`.
- Импорт: считывает JSON и добавляет новые слова в список.

---

## Инструкция по сборке в Termux

1. Установи Termux (с F-Droid или termux.com).
2. В Termux выполни:
```bash
pkg update && pkg upgrade
pkg install openjdk-17 git unzip wget gradle android-tools
```
3. Склонируй проект:
```bash
git clone https://github.com/example/AndroidRhymeSuggestor.git
cd AndroidRhymeSuggestor
```
4. Собери APK:
```bash
gradle assembleDebug
```
5. Найди APK:
```
app/build/outputs/apk/debug/app-debug.apk
```
6. Установи APK на телефон:
```bash
adb install app/build/outputs/apk/debug/app-debug.apk
```

---

Проект полностью готов: оффлайн+онлайн подсказки, экспорт и импорт словаря.
