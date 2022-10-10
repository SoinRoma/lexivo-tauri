<h1 align="center">Lexivo - Tauri</h1>

### Новый проект

Для создания приложения на основе Tauri используется команда:

```
npx create-tauri-app
```

### Дополнительные программы

Также для первого запуска может потребуется установить [Rust](https://www.rust-lang.org/) и другие программы.
Подробная инструкция [тут](https://tauri.app/v1/guides/getting-started/prerequisites)

## Настройка обновлений

Для настройки и получения обновления для вашего приложения понядобится сгенирировать публичный и приватный ключ

```
tauri signer generate -w ~/.tauri/myapp.key
```

В корне проекта появится папка ~ , где будут лежать ключи. 
Образец находится в файле example.env

+ Публичный ключ должен находить в tauri.conf.json\tauri\updater\pubkey
+ Приватный ключ (с паролём или без) должен лижать в переменных средах вашего компьютера
Подробнее об этом [тут](https://github.com/tauri-apps/tauri/discussions/4451). А как правильно добавить ключ в 
переменные среды [тут](https://phoenixnap.com/kb/windows-set-environment-variable). После этого потребуется перезапуск 
компьютера.
  

Полная инструкция здесь [тут](https://tauri.app/v1/guides/distribution/updater/)


## Запуск приложения

1 - Установка всех пакетов и зависимостей
```
npm install
```

2 - Запуск приложения в режиме разработчика
```
npm run tauri dev
```

3 - Сборка пакета
```
npm run tauri build
```