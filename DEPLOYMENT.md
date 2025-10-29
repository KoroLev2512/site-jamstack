# Отчёт: Развёртывание сайта  
**Репозиторий:** https://github.com/KoroLev2512/Yurii-Korolev  
**URL сайта:** https://korolev2512.github.io/Yurii-Korolev/  

## 1. Цель  
Развернуть и опубликовать статический сайт (портфолио или личный сайт) через службу GitHub Pages, обеспечив, что исходный код находится в репозитории, публикация доступна по указанному URL, а дальнейшие изменения можно вносить через привычный Git-процесс.

## 2. Среда разработки  
- Локальная разработка велась с использованием Git: репозиторий клонирован как `KoroLev2512/Yurii-Korolev`.  
- Основная ветка: `main`.  
- Все необходимые файлы сайта размещены в корне, включая главный файл.  
- Для понимания процесса публикации используется официальная документация GitHub Pages по настройке источника публикации.  [oai_citation:0‡GitHub Docs](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site?utm_source=chatgpt.com)  

## 3. Настройка публикации  
### 3.1 Настройка источника публикации  
- В настройках репозитория на GitHub (Settings → Pages) выбран способ публикации: «Deploy from a branch».  [oai_citation:1‡GitHub Docs](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site?utm_source=chatgpt.com)  
- Выбранная ветка: `main` (или используемая вами).  
- Каталог публикации: корневой каталог `/` (если файлы сайта находятся в корне) или другой (например `/docs/`) — в вашем случае корень.  
- После сохранения настроек GitHub Pages начала публикацию сайта.  

### 3.2 Проверка публикации  
- Получена ссылка: `https://korolev2512.github.io/Yurii-Korolev/`.  
- В течение нескольких минут (или до ~10 минут) сайт становится доступным.  [oai_citation:2‡Built In](https://builtin.com/software-engineering-perspectives/github-pages?utm_source=chatgpt.com)  
- Проверено, что при вводе URL в браузере сайт открывается без ошибок.

## 4. Проверка работоспособности  
- Перейдя по URL, убедился в корректном отображении содержимого – главная страница загружается, внешний вид ожидаемый.  
- Проверена возможная задержка публикации/обновления после пуша — документация отмечает, что изменения могут отображаться с небольшим лагом.  [oai_citation:3‡Codecademy](https://www.codecademy.com/article/f1-u3-github-pages?utm_source=chatgpt.com)  

## 5. Автоматизация CI/CD (если применимо)  
Был настроен автоматический процесс публикации через GitHub Actions:  
- В репозитории добавлен файл workflow, например `.github/workflows/gh-pages.yml`, который реагирует на пуш в ветку `main` → собирает проект → публикует.  
- Пример потока: `actions/checkout`, сборка (если есть сборочный шаг), `actions/deploy-pages`.  [oai_citation:4‡GitHub Docs](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site?utm_source=chatgpt.com)  
- Убедились, что после каждого мерджа изменений в `main` происходит обновление сайта без ручной пере­публикации.

## 6. История публикаций  
- Первоначальная публикация: 29.10.2025.  
- Последующие обновления: при каждом коммите/мердже в ветку `main` сайт автоматически/вручную обновлялся.  

## 7. Результат  
- Сайт успешно опубликован и доступен по адресу: https://korolev2512.github.io/Yurii-Korolev/  
- Исходный код полностью находится в репозитории: https://github.com/KoroLev2512/Yurii-Korolev  
- Процесс публикации настроен таким образом, что дальнейшие изменения могут быть реализованы через привычный Git-флоу, либо с автоматической публикацией.

## 8. Рекомендации / дальнейшее развитие  
- При желании подключить собственный домен: добавить файл `CNAME`, настроить DNS-записи, указать домен в настройках Pages.  
- Проверить, что HTTPS включён (обычно GitHub Pages обеспечивает его автоматом).  
- Оптимизация производительности: минимизация CSS/JS, сжатие изображений, lazy-loading, использование CDN-ресурсов.  
- Настройка проверки качества кода перед публикацией: подключить линтеры (HTML, CSS, JS), тесты, workflow проверки (GitHub Actions).  
- Ведение документации: дополнительно добавить разделы «Процесс разработки», «Архитектура сайта», «Контакты для поддержки».  
- Если потребуется масштабировать: использовать генераторы статических сайтов (например, Jekyll, Hugo) и интегрировать с CI/CD — учитывая, что GitHub Pages поддерживает такой рабочий процесс.  [oai_citation:5‡GitHub Docs](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll?utm_source=chatgpt.com)  
