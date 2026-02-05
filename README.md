# Как скачать и установить Microsoft Office (Word, Excel, PowerPoint и др.) в 2026 году

## Описание

В этом руководстве вы узнаете, как скачать официальный комплект Microsoft Office с сайта Microsoft, а также как его установить на ваш компьютер. Все ссылки ведут на официальный сайт, что гарантирует безопасность и отсутствие вирусов.

## Шаг 1. Скачивание установщика

Перейдите по ссылке на официальный сайт Microsoft и скачайте Office Deployment Tool:

[Download Office Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117)

## Шаг 2. Распаковка файлов

Запустите скачанный файл, примите лицензионное соглашение и выберите папку для распаковки файлов.

## Шаг 3. Открытие PowerShell от имени администратора

Откройте Windows PowerShell с правами администратора одним из способов:
- Win + X → «Терминал Windows (Admin)»
- Shift + ПКМ на рабочем столе → «Открыть окно PowerShell здесь»
- Поиск «PowerShell» → ПКМ → «Запуск от имени администратора»

## Шаг 4. Переход в папку с файлами

Перейдите в папку, куда распаковали файлы, командой:
```powershell
cd C:\Users\<ваш_пользователь>\Downloads\Office
```

## Шаг 5. Установка Office

Выполните две команды по очереди:
```powershell
reg add "HKCU\Software\Microsoft\Office\16.0\Common\ExperimentConfigs\Ecs" /v "CountryCode" /t REG_SZ /d "std::wstring|US" /f
.\setup.exe /configure .\configuration-Office365-x64.xml
```

После этого начнётся установка Microsoft Office.

Активация Office через PowerShell

<img width="806" height="1165" alt="image" src="https://github.com/user-attachments/assets/d2958170-1e11-4c59-aa9e-b2df252677d8" />

