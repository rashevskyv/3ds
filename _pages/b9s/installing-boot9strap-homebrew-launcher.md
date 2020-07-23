---
title: Установка boot9strap (Homebrew Launcher)
lang: ru
permalink: installing-boot9strap-homebrew-launcher.html
author_profile: true
---
{% include toc title="Разделы" %}

{% include /inc/emunand_note.txt %}

Убедитесь, что на устройстве включена беспроводная связь и есть стабильное подключение к интернету. safehax требует интернет для работы.

## Инструкция

### Часть I - Запуск и применение эксплойтов

1. Выберите **udsploit** в списке Homebrew
  + Вам может потребоваться пролистать список ВНИЗ, чтобы увидеть нужный пункт
1. После завершения нажмите {% include inc/btn.txt btn="START" %} для выхода из **udsploit**
  + Может потребоваться несколько попыток
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова
1. Выберите **safehax** в списке Homebrew
  + Вам может потребоваться пролистать список ВНИЗ, чтобы увидеть нужный пункт
  + Если появляется ошибка "PM INIT FAILED", убедитесь, что используете **safehax** со включенным WiFi
  + Если "PM INIT FAILED" *всё ещё* появляется, попробуйте использовать [safehax версии r19](https://github.com/TiniVi/safehax/releases/tag/r19){:target="_blank"}
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова
1. Если эксплойт сработал, запустится SafeB9SInstaller

### Часть II - Установка boot9strap

{% include /inc/install_b9s.txt %}

___

## **Следующий шаг:** [Завершение установки](finalizing-setup)
{: .notice--success}

