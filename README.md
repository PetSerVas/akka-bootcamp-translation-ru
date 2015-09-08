# Тренировочный центр Akka.NET

![Akka.NET logo](images/akka_net_logo.png)

Добро пожаловать в тренировочный центр [Akka.NET](http://getakka.net/ "Akka.NET - Distributed actor model in C# and F#")!  Это бесплатный курс, созданный для вас ребятами из [Petabridge](http://petabridge.com/ "Petabridge - Akka.NET Training, Consulting, and Support") и переведенный мну.

[![Можно присоединиться к англоязычному чату здесь https://gitter.im/petabridge/akka-bootcamp](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/petabridge/akka-bootcamp?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

В трех блоках мы научим вас создавать полезныу полнофункциональные программы, используя возможности акторов Akka.NET, и другие не менее увлекательные вещи из арсенала Akka.NET.

Мы начнем с создания простых акторов, и будем улучшать программу до полноценного приложения.

Этот курс никак не ограничен по времени, вы сами выбираете, с какой скоростью хотите проходить обучение.
Также можно подписаться на [ежедневную рассылку уроков](http://learnakka.net/ "Learn Akka.NET with Akka.NET Bootcamp").


> Замечание:  Поддержка F# все еще в процессе ( более подробно смотрите на [FSharp branch](https://github.com/petabridge/akka-bootcamp/tree/FSharp)). Мы с удовольствием примем пулл-риквесты  для F#. Не стесняйтесь их отсылать.

## Чему вы научитесь?
В тренировочном центре Akka.NET вы научитесь использовать акторов Akka.NET для построения реактивных, параллельных приложений.

Вы узнаете как можно создавать приложения, которые казались вам очень сложными (если не невозможными) до изучения Akka.NET. Вы уйдуте от сюда с уверенностью, что вы можете решать более и более сложные проблемы, чем все те, с которыми вы встречались ранее.

### Блок 1
В первом блоке мы изучим основы работы акторов и всей системы Akka.NET в целом.

В состав *NIX  входит встроенная команда `tail`, которая позволяет отслеживать изменения в файле (например наблюдать за постоянно растущим  файлом логов). Мы создадим аналог команды `tail` для Windows и одновременно получим практические навыки работы с акирпами.


В блоке №1 вы изучите:

1. Как создавать вашу собственную систему акторов(`ActorSystem`) и акторов;
2. Как посылать сообщения акторам, и как обрабатывать разные типы сообщений;
3. Как использовать `Props` и `IActorRef`-ы  для построения систем с низкой связностью.
4. Как использовать пути к акторам, из адреса и `ActorSelection` для отправки сообщений другим акторам.
5. Как создавать дочерних акторов и иерархии акторов. Как контролировать дочерних акторов при помощи `SupervisionStrategy`.
6. Как контролировать действия происходящие при запуске, остановке, и перезапуске актора.

**[Начать изучение блока №1](src/Unit-1)**.

### Блок №2
Во втором блоке мы погрузимся в коцепции, которые позволят вам создавть более сложные приложения, чем то, которое было в первом блоке.

В блоке №2 вы узнаете:

1. Как использовать [конфигурацию HOCON](http://getakka.net/wiki/Configuration "Akka.NET HOCON Configurations") для конфигурации ваших акторов при помощи App.config и Web.config;
1. Как сконфигурировать диспетчера акторов [Dispatcher](http://getakka.net/wiki/Dispatchers) таким образом, чтобы акторы выполнялись в потоке Windows Forms UI. Таким образом акторы смогут производить действия над контролами, без необходимости смены контекстов;
1. Как обрабатывать сложные типы сообщений при помощи сопоставления с образцом в `ReceiveActor`;
1. Как исопльзовать планировщик (`Scheduler`) для периодической отправки сообщений;
1. Как использовать паттерн [Publish-subscribe (pub-sub)](http://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern) между акторами;
1. Как и зачем менять поведение актора во время выполнения программы; и
2. Как сохранять сообщения в стек(`Stash`) актора для последующей обработки.

**[Приступить к изучению блока №2](src/Unit-2)**.

### Блок № 3 
Третий блок позволит узнать как использовать [Octokit](http://octokit.github.io/) с максимальной параллелизацией и масштабируемостью для того, чтобы доставать данные из репозиториев Github!

В блоке № 3 вы изучите:

1. Как выполнять асинхронную работу внутри акторов при помощи `PipeTo`;
2. Как пользоваться `Ask` для блокирующего ожидания ответа от другого актора ;
2. Как использовать `ReceiveTimeout` для контроля таймаутов ответа от других акторов;
4. Как использовать роутер `Group` для разделения работы между вашими акторами;
5. Как исользовать роутеры `Pool` для автоматического масштабирования пула акторов; и
6. Как использовать HOCON для конфигурации роутеров.

**[Начать блок №3](src/Unit-3)**.

## Вводная

Вот как устроен тренировочный центр Akka.NET!

### Используйте Github, чтобы упростить себе жизнь

Этот Github репозиторий содержит проекты файлов для Visual Studio, а также другие ресурсы необходимые для работы.

Таким образом, если вы хотите заниматься, мы рекомендуем следующее:

1. Если у вас ее еще нету, заведите учетную запись на [Github](https://github.com/).
2. [Форкните этот репозиторий](https://github.com/petabridge/akka-bootcamp/fork) и склонируйте ваш форк на локальную машину.
3. На протяжении работы с проектом, держите окно браузера открытым, чтобы видеть [Akka.NET Bootcamp ReadMes](https://github.com/petabridge/akka-bootcamp/). Таким образом вы сможете читать документацию одновременно с работой в студии.

### Структура тренировочного центра

Тренировочный центр Akka.NET состоит из 3-х блоков:

* **Блок 1 - Начало работы с Akka.NET**
* **Блок 2 - Akka.NET для середнячков**
* **Блок 3 - Продвинутые техники Akka.NET**

Каждый блок имеет следующую структуру ( для примера возьмем **Блок 1**) :

````
src\Unit1\README.MD - оглавление и инструкции по выполнению модуля
src\Unit1\DoThis\ - содержит .SLN и файлы проектов, которые вам понадобятся в этом блоке
-- урок  1
src\Unit1\Lesson1\README.MD - README описывающий урок
src\Unit1\Lesson1\DoThis\ - C# классы, изображения, текстовые файлы, и другое барахло необходимое для выполнения первого урока
src\Unit1\Lesson1\Completed\ - Застряли на выполнении урока? В этой папке вы найдете "эталонное" решение для задачи.
-- и т.д. для остальных уроков в блоке
````

Начанайте выполнение заданий с первого урока в каждом блоке, и следуйте по ссылкам внутри README файлов на Github. Мы стартуем с **[Блока 1, урока 1](src/Unit-1/lesson1)**.

### Структура урока
Каждый урок содержит README файл со следующей информацией:

1. Концепции и инструменты Akka.NET, которые вы будете применять на этом уроке. Плюс ссылки на дополнительную информацию и примеры
2. Пошаговые инструкции по изменению .NET проекта внутри папки `Unit-[Num]/DoThis/`. 
3. Если вы застряли на выполнении задания, каждый урок содержит свою папку  `/Completed/`, с готовым к выполенению кодом задания.  Можете сравнить его со своей реализацией и таким образом найти несоответствия.

#### Когда вы выполняете задания...

Несколько вещей, на которые стоит обраттиь внимание при выполнении пошаговых инструкций:

1. **Don't just copy and paste the code shown in the lesson's README**. You'll retain and learn all of the built-in Akka.NET functions if you type out the code as it's shown. [Kinesthetic learning](http://en.wikipedia.org/wiki/Kinesthetic_learning) FTW!
2. **You might be required to fill in some blanks during individual lessons.** Part of helping you learn Akka.NET involves leaving some parts of the exercise up to you - if you ever feel lost, always check the contents of the `/Completed` folder for that lesson.
3. **Don't be afraid to ask questions**. You can [reach the Petabridge and Akka.NET teams in our Gitter chat](https://gitter.im/petabridge/akka-bootcamp) here.


## Docs
We will provide explanations of all key concepts throughout each lesson, but of course, you should bookmark (and feel free to use!) the [Akka.NET docs](http://getakka.net/).

## Tools / prerequisites
This course expects the following:

- You have some programming experience and familiarity with C#
- A Github account and basic knowledge of Git.
- You are using a version of Visual Studio ([it's free now!](http://www.visualstudio.com/))
  - We haven't had a chance to test these in Xamarin / on Mono yet, but that will be coming soon. If you try them there, please let us know how it goes! We are planning on having everything on all platforms ASAP.


## Enough talk, let's go!
[Let's begin!](src/Unit-1/lesson1)

## About Petabridge
![Petabridge logo](images/petabridge_logo.png)

[Petabridge](http://petabridge.com/) is a company dedicated to making it easier for .NET developers to build distributed applications.

**[Petabridge also offers Akka.NET consulting and training](http://petabridge.com/ "Petabridge Akka.NET consulting and training")** - so please [sign up for our mailing list](http://petabridge.com/)!

---
Copyright 2015 Petabridge, LLC
