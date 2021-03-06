---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Авторизация  
layout: default
nav_order: 2
parent: Базовый функционал
---

{:toc }

Удобство работы с ботом открывается при предоставлении боту доступа к: 
- Гильд-стоку 
- Персональному стоку 
- Профилю 
- Обмундированию 

В этом случае вы и ваш ГМ получают максимальный профит от бота, удобства управление гильдией и скоростью принятия решений. 

## Назначение авторизаций 

### 📦 Гильд-сток 

Гильд-сток сообщение от ЧВ содержит информацию о гильдии (замок, тэг, эмоджи и так далее, кроме состава гильдии), размер склада, вещи. 

Доступ к гильд-стоку позволяет боту определить вашу гильдию и объединить вас с согильдийцами использующими уже Казну. Вам становятся доступны основные полезные свойства бота для группового взаимодействия. См. Продвинутый функционал и Гильд чаты. 

### 🕋 Персональный сток 

Данный тип сообщений от ЧВ содержит информацию о вашем личном складе. Дав доступ к этому разделу, вы сможете использовать инлайн функционал бота для закидывания в гильдию трав, ресурсов, крафта и других вещей. 

ГМ сможет лишний раз вас не дергать прося показать что есть в стоке или кидая клич на гильдию, есть ли у кого-то Silver Alloy, например. 

### 👤 Профиль 

В профиле ЧВ указывается информация о вашем персонаже: жизни, стамина, опыт, золото, имя и так далее. 

Доступ к профилю позволяет целенаправленно пинговать членов гильдии на бои с мобами, показывать ситуацию с опытом и так далее. Доступ к профилю позволяет так же определить вашу гильдию. 

### 🎽 Обмундирование 

В этом сообщение ЧВ рассказывает о экипировке персонажа, его качестве и состоянии. 

Доступ к этому разделу позволяет Казне уведомлять вас о сломанных вещах, о вещах, которые можно улучшить. ГМ может просматривать экипировку у всей гильдии и планировать дальнейшие обновления. 

## Базовая авторизация 

Базовая авторизация дает доступ к апи от вашего имени. С практической точки зрения пользы от этого мало, но это позволяет поддержать проект мешками с золотом. Впрочем, это необходимый шаг для того, чтобы дать доступ к другим правам. 

![auth_none]

Начинается все с кнопки авторизации. Нажав на нее, вы должны увидеть сообщение примерно следующего содержания:

![auth_basic]

После этого в CW вам должно прийти сообщение о том, что бот хочет получить доступ к вашим данным. Обязательно дождитесь сообщения в CW, прежде чем жать на кнопку авторизации еще раз. 

![auth_forward]

Необходимо форвардить всё сообщение, чтобы бот распознал код. После форварда вы увидите в боте что код принят, а так же ссылки и кнопки для авторизации доступа к дополнительной информации. 

![auth_gbasic]

Далее вы можете воспользоваться ссылками, кнопками или же зайти в меню настроек ⚙️ и там дать\забрать желаемые права. 

Не надо жать на все ссылки сразу. ЧВ сгенерирует код на каждую ссылку, но примет только последнюю и даст права боту только на последний запрошенный раздел информации.
{: .label .label-red }

## Авторизация доступа к гильд-стоку 

Доступ к гильд-стоку дает вам возможность: 
- Просматривать вещи в гильд-стоке по категориям 
- Видеть вес вещей в определенной категории (с разбивкой по весам)
- Создание уведомлений на приход\уход ресурсов из гильд-стока 

Для того, чтобы дать доступ к гильд-стоку необходимо пройти в настроки бота (⚙️). Там будут отображены все текущие права доступа. Например: 

![auth_mgbasic]

На изображении выше видно, что никаких прав кроме базовых боту не выдано. Для авторизации доступа к гильд-стоку необходимо выполнить команду `/auth_guildstock`. Это запустит процесс авторизации. Т.е. СW пришлет вам сообщение с кодом, а вы его должны зафорвардить Казне. 

![auth_gscode]

Обратите внимание, что CW под кодом пишет для чего этот код. 

![auth_gsg]

И результат форварда сообщения с кодом в Казну показан выше. 

Теперь в меню настроек (⚙️) будет отображена новая информация по правам. Так же вместо кнопки авторизации в основном меню будет кнопка обновления. 

![auth_gsmenu]

## Авторизация доступа к персональному стоку 

Авторизация доступа ко всем остальным разделам осуществляется так же, как и к гильд-стоку. 

## Статус авторизаций для членов гильдии 

Проверить свою принадлежность к гильдии и статус авторизаций может любой пользователь бота. Для этого необходимо ввести команду `/guild`. Казна в ответ покажет состав с правами и ролями. 

Например, в сообщении ниже видно, что 3 члена гильдии дали полный доступ, а четвертый только к персональному стоку и профилю. 

![guild_roster]

В сообщении используется позиционная запись: 

гильд-сток | сток | профиль | экипировка | роль | имя




[auth_none]: images/auth_none.png
[auth_basic]: images/auth_basic.png
[auth_forward]: images/auth_forward.png
[auth_gbasic]: images/auth_granted_basic.png
[auth_mgbasic]: images/auth_m_granted_basic.png
[auth_gscode]: images/auth_gstock_code.png
[auth_gsg]: images/auth_gstock_granted.png
[auth_gsmenu]: images/auth_menu_gs.png
[guild_roster]: images/guild_roster.png


