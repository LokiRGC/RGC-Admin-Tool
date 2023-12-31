# RGC Admin Tool
## Инструменты от RGC

Приложение, разработанное на языке PHP, командой [RGC] RAGNAROK COMMUNITY, содержит в себе инструменты для редактирования конфигов Dayz.

- Авто-обновление программы ✨
- Гибкая настройка конфигов ✨
- Стильный UX дизайн ✨

## Установка

Для работы .jar версии, потребуется [JAVA](https://www.java.com/ru/) 
установите зависимости и запустите приложение

## Плагины

| Плагины | README |
| ------ | ------ |
| HotKey 1.0.0 | Функция горячих клавиш |
| 2D Game | Game2DBundle |
| HTTP Client | HTTP Клиент |
| Jsoup | Парсер HTML (модульный компонент) |
| Mailer | Отправитель писем (модульный компонент) |
| MySQL | MySQL клиент |
| Material UI | Новые Material UI компоненты |
| System Tray | Трей иконка (модульный компонент) |
| ZIP | ZipFileScript (модульный компонент) |
| RichText | UXRichTextArea |
| Updater | AbstractUpdater - Сервис обновлений |
| Windows | Плагин для взаимодействия с Windows |

## Модуль Загрузки
Модуль загрузки приложения, стартовый модуль подгрузки компонентов.



```sh
namespace app\modules;
use bundle\updater\$GitHubUpdater;
use std, gui, framework, app;

class AppModule extends AbstractModule
```
Событие
```sh
function doAction(ScriptEvent $e = null) //Появление модуля
```

## Sound

Поток мультиплеера, в модуле start
```sh
general1 //Все звуки находятся в этом потоке
```

## Mail
Хост
```sh
smtp
```
Ограничение по времени.
```sh
TimeOut - 15000
```
Отправка письма.
```sh
        $this->mail->send([
                          'to' => $this->object->text,
                          'message' => $this->object->text,
                          'subject' => $this->object->text
                          ]);
```

## Сброс настроек
Для удаления всех настроек приложения, удалите следующие файлы в корне программы: 
```sh
./Addition.ini
./RadZone.ini
./Console.ini
./Settings.ini
./Database.ini
```
