# Задание 1. Yandex Cloud
- Создать бакет Object Storage и разместить в нём файл с картинкой:
- Создать бакет в Object Storage с произвольным именем (например, имя_студента_дата).
- Положить в бакет файл с картинкой.
- Сделать файл доступным из интернета.
- Создать группу ВМ в public подсети фиксированного размера с шаблоном LAMP и веб-страницей, содержащей ссылку на картинку из бакета:
- Создать Instance Group с тремя ВМ и шаблоном LAMP. Для LAMP рекомендуется использовать image_id = fd827b91d99psvq5fjit.
- Для создания стартовой веб-страницы рекомендуется использовать раздел user_data в meta_data.
- Разместить в стартовой веб-странице шаблонной ВМ ссылку на картинку из бакета.
- Настроить проверку состояния ВМ.
- Подключить группу к сетевому балансировщику:
- Создать сетевой балансировщик.
- Проверить работоспособность, удалив одну или несколько ВМ.
  [main.tf](https://github.com/EVolgina/ycloud2/blob/main/main.tf) [variables.tf](https://github.com/EVolgina/ycloud2/blob/main/variables.tf)
[providers.tf](https://github.com/EVolgina/ycloud2/blob/main/providers.tf)
```
Apply complete! Resources: 4 added, 0 changed, 5 destroyed.
Outputs:
lamp-group-address = "vp-target-nlb-group"
pic-url = "https://storage.yandexcloud.net/paint/goa.jpg"
```
![VM]()

![paint]()
![NLB]()
![Перезапуск](https://github.com/EVolgina/ycloud2/blob/main/перезапуск.png)
```

```
