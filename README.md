# Колесо фортуны

Одностраничное приложение (HTML/JS/SVG, без внешних зависимостей). Названия сегментов и настройки хранятся в `localStorage` браузера каждого пользователя — на сервер уходит только код.

## Публикация на внутреннем GitLab Pages

1. Создай в `gitlab.corp.mail.ru` пустой проект (без README).
2. Привяжи remote и запушь ветку `master`:
   ```bash
   cd ~/wheel-of-fortune
   git remote add origin git@gitlab.corp.mail.ru:<group>/<project>.git
   git push -u origin master
   ```
3. Дождись первого пайплайна — там отработает job `pages`.
4. Адрес сайта появится в проекте: **Settings → Pages** (покажет URL вида `https://<namespace>.pages.<host>/<project>/`).

> Если Pages в вашем инстансе не настроен — попроси админа включить его (нужен `pages_external_url` и wildcard-DNS `*.pages.<host>`).

## Локальный просмотр

```bash
cd ~/wheel-of-fortune
python3 -m http.server 8000
# → http://localhost:8000
```
