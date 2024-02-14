<p align="center"><img src="https://raw.githubusercontent.com/Stirling-Tools/Stirling-PDF/main/docs/stirling.png" width="80" ><br><h1 align="center">Stirling-PDF</h1>
</p>

[![Docker Pulls](https://img.shields.io/docker/pulls/frooodle/s-pdf)](https://hub.docker.com/r/frooodle/s-pdf)
[![Discord](https://img.shields.io/discord/1068636748814483718?label=Discord)](https://discord.gg/Cn8pWhQRxZ)
[![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/frooodle/s-pdf/latest)](https://github.com/Stirling-Tools/Stirling-PDF/)
[![GitHub Repo stars](https://img.shields.io/github/stars/stirling-tools/stirling-pdf?style=social)](https://github.com/Stirling-Tools/stirling-pdf)
[![Paypal Donate](https://img.shields.io/badge/Paypal%20Donate-yellow?style=flat&logo=paypal)](https://www.paypal.com/paypalme/froodleplex)
[![Github Sponser](https://img.shields.io/badge/Github%20Sponsor-yellow?style=flat&logo=github)](https://github.com/sponsors/Frooodle)

[![Deploy to DO](https://www.deploytodo.com/do-btn-blue.svg)](https://cloud.digitalocean.com/apps/new?repo=https://github.com/Stirling-Tools/Stirling-PDF/tree/digitalOcean&refcode=c3210994b1af)

Это мощный инструмент для манипулирования PDF-файлами, работающий на основе веб-технологий и запускаемый локально с использованием Docker. Он позволяет выполнять различные операции с PDF-файлами, такие как разделение, слияние, конвертация, переупорядочивание, добавление изображений, поворот, сжатие и многое другое. Это приложение с веб-интерфейсом, запускаемое локально, начало свое существование как приложение, созданное исключительно с помощью ChatGPT, и развилось до включения широкого спектра функций для обработки всех ваших PDF-файлов.

Stirling PDF не осуществляет исходящих вызовов для сохранения или отслеживания записей.

Все файлы и PDF-файлы либо существуют исключительно на клиентской стороне, находятся в памяти сервера только во время выполнения задачи, либо временно находятся в файле исключительно для выполнения задачи. Любой файл, загруженный пользователем, будет удален с сервера к тому времени.

![stirling-home](images/stirling-home.png)

## Особенности
- Поддержка темного режима.
- Пользовательские параметры загрузки (см. [здесь](https://github.com/Stirling-Tools/Stirling-PDF/blob/main/images/settings.png) для примера)
- Параллельная обработка файлов и загрузки
- API для интеграции с внешними скриптами
- Опциональная поддержка входа и аутентификации (см. [здесь](https://github.com/Stirling-Tools/Stirling-PDF/tree/main#login-authentication) для документации)


## **Особенности PDF**

### **Операции с страницами**
- Просмотр и изменение PDF-файлов - Просмотр многостраничных PDF-файлов с настраиваемой сортировкой и поиском. Плюс функции редактирования на странице, такие как аннотирование, рисование и добавление текста и изображений. (Используется PDF.js с Joxit и Liberation.Liberation шрифтами)
- Полностью интерактивный графический интерфейс для слияния/разделения/поворота/перемещения PDF-файлов и их страниц.
- Объединение нескольких PDF-файлов в один результирующий файл.
- Разделение PDF-файлов на несколько файлов по указанным номерам страниц или извлечение всех страниц в отдельные файлы.
- Переупорядочивание страниц PDF в разном порядке.
- Поворот PDF-файлов на 90-градусов.
- Удаление страниц.
- Макет нескольких страниц (форматирование PDF в многостраничный формат).
- Изменение размера содержимого страницы на установленный %.
- Регулировка контраста.
- Обрезка PDF.
- Автоматическое разделение PDF (с помощью физических разделителей страниц).
- Извлечение страниц(ы).
- Конвертация PDF в одностраничный файл.

### **Операции конвертации**
- Конвертация PDF в изображения и обратно.
- Конвертация любого общего файла в PDF (с использованием LibreOffice).
- Конвертация PDF в Word/Powerpoint/другие форматы (с использованием LibreOffice).
- Конвертация HTML в PDF.
- URL в PDF.
- Markdown в PDF.

### **Безопасность и разрешения**
- Добавление и удаление паролей.
- Изменение/установка разрешений PDF.
- Добавление водяных знаков.
- Подтверждение/подпись PDF.
- Санитария PDF.
- Автоудаление текста.

### **Прочие операции**
- Добавление/генерация/написание подписей.
- Восстановление PDF-файлов.
- Обнаружение и удаление пустых страниц.
- Сравнение 2 PDF-файлов и отображение различий в тексте.
- Добавление изображений в PDF-файлы.
- Сжатие PDF для уменьшения их размера (с использованием OCRMyPDF).
- Извлечение изображений из PDF.
- Извлечение изображений из сканов.
- Добавление номеров страниц.
- Автоматическое переименование файла путем обнаружения текста заголовка PDF.
- OCR на PDF (с использованием OCRMyPDF).
- Преобразование в PDF/A (с использованием OCRMyPDF).
- Редактирование метаданных.
- Выпрямление PDF-файлов.
- Получение всей информации о PDF для просмотра или экспорта в формате JSON.


Для обзора задач и используемых технологий каждой из них, пожалуйста, ознакомьтесь с [Endpoint-groups.md](https://github.com/Stirling-Tools/Stirling-PDF/blob/main/Endpoint-groups.md)
Демонстрация приложения доступна [здесь](https://stirlingpdf.io). имя пользователя: demo, пароль: demo

## Используемые технологии
- Spring Boot + Thymeleaf
- [PDFBox](https://github.com/apache/pdfbox/tree/trunk)
- [LibreOffice](https://www.libreoffice.org/discover/libreoffice/) для расширенных конвертаций
- [OcrMyPdf](https://github.com/ocrmypdf/OCRmyPDF)
- HTML, CSS, JavaScript
- Docker
- [PDF.js](https://github.com/mozilla/pdf.js)
- [PDF-LIB.js](https://github.com/Hopding/pdf-lib)

## Как использовать

### Локально
Пожалуйста, ознакомьтесь с https://github.com/Stirling-Tools/Stirling-PDF/blob/main/LocalRunGuide.md

### Docker / Podman
https://hub.docker.com/r/frooodle/s-pdf

Stirling PDF имеет 3 различных версии: полную, Lite и Ultra-Lite. В зависимости от используемых функций вам может потребоваться более компактный образ для экономии места.
Чтобы узнать, что предлагают различные версии, ознакомьтесь с нашим [соответствием версий](https://github.com/Stirling-Tools/Stirling-PDF/blob/main/Version-groups.md)
Для тех, кто не обращает внимание на оптимизацию места, просто используйте тег "latest".
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/frooodle/s-pdf/latest?label=Stirling-PDF%20Full)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/frooodle/s-pdf/latest-lite?label=Stirling-PDF%20Lite)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/frooodle/s-pdf/latest-ultra-lite?label=Stirling-PDF%20Ultra-Lite)

Запуск Docker
```bash
docker run -d \
  -p 8080:8080 \
  -v /location/of/trainingData:/usr/share/tessdata \
  -v /location/of/extraConfigs:/configs \
  -v /location/of/logs:/logs \
  -e DOCKER_ENABLE_SECURITY=false \
  --name stirling-pdf \
  frooodle/s-pdf:latest


  Также можно добавить следующее для настройки, но это не обязательно

  -v /location/of/customFiles:/customFiles \
```
Docker Compose (docker-compose.yml)
```yaml
version: '3.3'
services:
  stirling-pdf:
    image: frooodle/s-pdf:latest
    ports:
      - '8080:8080'
    volumes:
      - /location/of/trainingData:/usr/share/tessdata #Required for extra OCR languages
      - /location/of/extraConfigs:/configs
#      - /location/of/customFiles:/customFiles/
#      - /location/of/logs:/logs/
    environment:
      - DOCKER_ENABLE_SECURITY=false
```

Примечание: Podman совместим с Docker через интерфейс командной строки (CLI), поэтому просто замените "docker" на "podman".

## Включить функцию распознавания текста / сжатия
Пожалуйста, ознакомьтесь с https://github.com/Stirling-Tools/Stirling-PDF/blob/main/HowToUseOCR.md

## Поддерживаемые языки

Stirling PDF в настоящее время поддерживает 26 языков!
- Английский (English) (en_GB)
- Английский (США) (en_US)
- Арабский (العربية) (ar_AR)
- Немецкий (Deutsch) (de_DE)
- Французский (Français) (fr_FR)
- Испанский (Español) (es_ES)
- Упрощенный китайский (简体中文) (zh_CN)
- Традиционный китайский (繁體中文) (zh_TW)
- Каталанский (Català) (ca_CA)
- Итальянский (Italiano) (it_IT)
- Шведский (Svenska) (sv_SE)
- Польский (Polski) (pl_PL)
- Румынский (Română) (ro_RO)
- Корейский (한국어) (ko_KR)
- Португальский (Бразилия) (Português) (pt_BR)
- Русский (Русский) (ru_RU)
- Баскский (Euskara) (eu_ES)
- Японский (日本語) (ja_JP)
- Голландский (Nederlands) (nl_NL)
- Греческий (el_GR)
- Турецкий (Türkçe) (tr_TR)
- Индонезийский (Bahasa Indonesia) (id_ID)
- Хинди (हिंदी) (hi_IN)
- Венгерский (Magyar) (hu_HU)
- Болгарский (Български) (bg_BG)
- Сербский (латиница) (Srpski) (sr-Latn-RS)

## Содействие (создание проблем, переводы, исправление ошибок и т. д.)

Пожалуйста, ознакомьтесь с нашим [Руководством по содействию](CONTRIBUTING.md)!

## Настройка
Stirling PDF позволяет легко настраивать приложение.
Включает в себя такие вещи, как
- Настраиваемое название приложения
- Настраиваемые слоганы, значки, изображения, а также пользовательский HTML (через переопределение файлов)

Для этого есть два варианта, либо использовать сгенерированный файл настроек ``settings.yml``
Этот файл находится в каталоге ``/configs`` и использует стандартный формат YAML

Также поддерживаются переменные среды и они переопределяют файл настроек.
Например, в файле settings.yml у вас есть
```yaml
system:
  defaultLocale: 'en-US'
```

Чтобы сделать это с помощью переменной среды, у вас должно быть ``SYSTEM_DEFAULTLOCALE``

Текущий список параметров:
```yaml
security:
  enableLogin: false # установите значение 'true' для включения входа
  csrfDisabled: true

system:
  defaultLocale: 'en-US' # Установите язык по умолчанию (например, 'de-DE', 'fr-FR', и т. д.)
  googlevisibility: false # 'true', чтобы разрешить видимость Google (через robots.txt), 'false', чтобы запретить
  customStaticFilePath: '/customFiles/static/' # Путь к каталогу для пользовательских статических файлов

#ui:
#  appName: exampleAppName # Видимое название приложения
#  homeDescription: I am a description # Краткое описание или слоган, отображаемый на домашней странице.
#  appNameNavbar: navbarName # Название, отображаемое на панели навигации

endpoints:
  toRemove: [] # Список конечных точек для отключения (например, ['img-to-pdf', 'remove-pages'])
  groupsToRemove: [] # Список групп для отключения (например, ['LibreOffice'])

metrics:
  enabled: true # 'true' для включения конечных точек API Info (см. http://localhost:8080/swagger-ui/index.html#/API, чтобы узнать больше), 'false' для отключения
```
### Дополнительные примечания
- Эндпоинты. В настоящее время эндпоинты ENDPOINTS_TO_REMOVE и GROUPS_TO_REMOVE могут включать списки эндпоинтов и групп через запятую, чтобы отключить, как пример, ENDPOINTS_TO_REMOVE=img-to-pdf,remove-pages отключит и img-to-pdf, и remove pages, GROUPS_TO_REMOVE=LibreOffice отключит все, что использует LibreOffice. Вы можете увидеть список всех эндпоинтов и групп [здесь](https://github.com/Stirling-Tools/Stirling-PDF/blob/main/Endpoint-groups.md)
- customStaticFilePath. Настройка статических файлов, таких как логотип приложения, путем размещения файлов в каталоге /customFiles/static/. Пример настройки логотипа приложения - размещение /customFiles/static/favicon.svg для замены текущего SVG. Это можно использовать для изменения любых изображений/иконок/css/шрифтов/js и т. д. в Stirling-PDF

### Параметры только для среды выполнения
- ``SYSTEM_ROOTURIPATH`` т. е. установите ``/pdf-app`` для установки корневого URI приложения на ``localhost:8080/pdf-app``
- ``SYSTEM_CONNECTIONTIMEOUTMINUTES`` для установки пользовательских значений времени ожидания подключения
- ``DOCKER_ENABLE_SECURITY`` чтобы сообщить Docker о загрузке файлов безопасности (необходимо указать true для аутентификации входа)

## API
Для тех, кто хочет использовать бэкэнд-API Stirling-PDF для связи со своими собственными сценариями для редактирования PDF-файлов, можно просмотреть всю существующую документацию по API [здесь](https://app.swaggerhub.com/apis-docs/Stirling-Tools/Stirling-PDF/) или перейти по адресу /swagger-ui/index.html вашего экземпляра stirling-pdf для документации вашей версии (или перейти по кнопке API в настройках Stirling-PDF)

## Аутентификация входа
![stirling-login](images/login-light.png)
### Предварительные требования:
- Пользователь должен иметь папку ./configs внутри Docker, чтобы она сохранялась во время обновлений.
- Пользователи Docker должны загрузить версию безопасности jar, установив ``DOCKER_ENABLE_SECURITY`` в ``true`` в переменных среды.
- Затем либо включите вход через файл settings.yml, либо установите ``SECURITY_ENABLE_LOGIN`` в ``true``
- Теперь начальный пользователь будет сгенерирован с именем пользователя ``admin`` и паролем ``stirling``. При входе в систему вас попросят сменить пароль на новый. Вы также можете использовать переменные среды ``SECURITY_INITIALLOGIN_USERNAME`` и ``SECURITY_INITIALLOGIN_PASSWORD``, чтобы немедленно установить свой собственный пароль (рекомендуется удалить их после создания пользователя).

После выполнения вышеуказанного, при перезапуске будет показан новый stirling-pdf-DB.mv.db, если все сработало.

При входе в Stirling PDF вы будете перенаправлены на страницу /login для входа с этими учетными данными по умолчанию. После входа все должно функционировать как обычно.

Чтобы получить доступ к настройкам учетной записи, перейдите в "Настройки учетной записи" в меню настроек (в правом верхнем углу навигационной панели). Это меню настройки учетной записи также содержит ваш ключ API.

Чтобы добавить новых пользователей, перейдите внизу в "Настройки администратора", здесь вы можете добавлять новых пользователей. Упоминаемые в этом различные роли предназначены для ограничения скорости. Это работа в процессе, которая будет расширяться в будущем.

Для использования API вы должны предоставить заголовок с 'X-API-Key' и связанный с ним ключ API для этого пользователя.

## Часто задаваемые вопросы

### Вопрос 1: Какие планируемые функции?
- Полоса прогресса/отслеживание
- Полностью настраиваемые логические конвейеры для объединения нескольких операций вместе.
- Поддержка папок с автоматическим сканированием для выполнения операций
- Сокрытие текста (через пользовательский интерфейс, а не только автоматический способ)
- Добавление форм
- Поддержка макета с несколькими страницами (сшивание страниц PDF вместе) поддержка x строк y столбцов и настраиваемый размер страницы
- Заполнение форм вручную и автоматически

### Вопрос 2: Почему мое приложение загружает файлы .htm?
Это часто вызванная проблема вашей конфигурацией NGINX. Размер загружаемого файла по умолчанию для NGINX составляет 1 МБ, вам нужно добавить следующее в ваш файл sites-available Nginx. ``client_max_body_size SIZE;`` Где "SIZE" - это, например, 50M для файлов размером 50 МБ.

### Вопрос 3: Почему загрузка прерывается?
У NGINX по умолчанию есть значения времени ожидания, поэтому, если вы запускаете Stirling-PDF за NGINX, вам может потребоваться установить значение времени ожидания, такое как добавление конфигурации ``proxy_read_timeout 3600;``
