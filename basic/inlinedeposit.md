---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Сдача ресурсов   
layout: default
nav_order: 3
parent: Базовый функционал
has_toc: false
---
Требования: 
{: .d-inline}

Персональный сток 
{: .label .label-blue }

## Простой режим 

Казна работает в инлайн режиме, что позволяет быстро и непринужденно сдавать ресурсы в гильд-сток. 

Чтобы сдать ресурсы, надо в чате CW вызвать Казну напечатав `@CW_Kazna_bot`. После этого появится инлайн подсказка с функциями. Для сдачи ресурсов используются ключи: 
- r - (*resources*) ресурсы 
- h - (*herbs*) травы 
- k - (*kraft*) куски и рецепты крафта 
- p - (*potions*) зелья алхимиков 
- o - (*other*) другое (корм, свитки)

![inline_menu]

По умолчанию выбирается ключ **r** для ресурсов. 

Выбрав необходимый ключ (читай "раздел"), появится контекстное меню в котором можно найти ресурс для сдачи в гильдию, и нажать на него. Казна сформирует команду и моментально вышлет его в ЧВ. 

Поздравляю, вы сдали ресурс в гильдию не заморачиваясь на том, чтобы помнить его номер и всего в два клика. 

Вызов меню:

![inline_simple_deposit]

Результат:

![inline_simple_depositf]

## Ограничение ресурсов на сдачу 

Если вы не хотите всё сдавать, то максимальное количество ресурсов можно ограничить введя число после кода. Например: `r 50` - даст знать Казне, что надо ограничить максимум сдачи 50 единицами ресурса. 

![inline_simple_depositl]

[inline_menu]: images/inline_menu.png
[inline_simple_deposit]: images/inline_simple_deposit.png
[inline_simple_depositf]: images/inline_simple_deposit_f.png
[inline_simple_depositl]: images/inline_simple_deposit_limit.png



