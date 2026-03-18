---
description: Установка операционной системы Butter (ОС) на SD-карту для Raspberry Pi
---

# Установка Butter

Вам понадобится:

* Настольный компьютер
* Подключение к интернету
* Butter Box

{% stepper %}
{% step %}
### Скачайте Butter OS для Raspberry Pi&#x20;

Убедитесь, что размер файла совпадает с размером, указанным на сайте. Иногда браузеры не завершают загрузку, что может привести к повреждению файла.

{% embed url="https://www.dropbox.com/scl/fo/helpqh3q2oj7ti2ia038m/h?dl=0.&rlkey=cswt4w4zksiuj3eb1oca48yw0" %}

{% hint style="info" %}
Всегда выбирайте последнюю версию файла.&#x20;
{% endhint %}
{% endstep %}

{% step %}
### Вставьте карту micro SD в компьютер

Чтобы вставить карту micro SD в компьютер, вам может понадобиться адаптер:

<div align="center"><figure><img src="../../.gitbook/assets/image.png" alt="" width="375"><figcaption><p>Пример адаптера (USB-C к Micro SD)</p></figcaption></figure></div>

{% hint style="info" %}
Подключать коробку к компьютеру не нужно.
{% endhint %}
{% endstep %}

{% step %}
### Запустите Raspberry Pi Imager&#x20;

После того как вы вставили карту micro SD в компьютер с подключением к интернету, запустите Raspberry Pi Imager на настольном компьютере. Программа проведёт вас через шаги установки операционной системы Butter на карту micro SD.&#x20;

Если у вас нет Raspberry Pi Imager, вы можете скачать его здесь: [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)
{% endstep %}

{% step %}
### Выберите устройство > **Raspberry Pi Zero 2 W**

После запуска Raspberry Pi Imager вам будет предложено выбрать устройство Raspberry Pi.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 9.56.27 AM.png" alt=""><figcaption><p>Выберите Raspberry Pi Zero 2 W (или другое устройство, если у вас не стандартная коробка от Butter HQ)</p></figcaption></figure>
{% endstep %}

{% step %}
### Выберите операционную систему > Использовать пользовательскую

* На вкладке ОС выберите **Использовать пользовательскую** и загрузите пользовательский файл Butter OS .img. Убедитесь, что вы **распаковали файл** перед использованием.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 9.57.31 AM.png" alt=""><figcaption><p>Выберите «Использовать пользовательскую». Вы загрузите пользовательский файл .img, который скачали с Dropbox.</p></figcaption></figure>
{% endstep %}

{% step %}
### Выберите хранилище > Выберите карту Micro SD

* На вкладке **Хранилище** выберите **карту Micro SD.**

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 1.27.37 PM.png" alt=""><figcaption><p>Выберите карту Micro SD.</p></figcaption></figure>

После всех выборов ваш экран будет выглядеть примерно так:

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 1.27.43 PM.png" alt=""><figcaption><p>Финальный экран после выбора.</p></figcaption></figure>

Вам может быть показано сообщение _«Это действие удалит все данные с выбранного внешнего хранилища»_ и _«Хотите ли вы применить настройки»_, нажмите _«нет, очистить настройки»_.

После этого выберите _«записать»_ и начните процесс записи на карту Micro SD.
{% endstep %}

{% step %}
### Извлеките из компьютера и вставьте карту Micro SD в Raspberry Pi (Butter Box)

По завершении извлеките карту Micro SD. Вставьте карту Micro SD в Raspberry Pi (Butter Box), который не подключён к питанию.&#x20;
{% endstep %}

{% step %}
### Перейдите к быстрому старту

Подключите Raspberry Pi (Butter Box) к питанию. Подождите несколько мгновений и подключитесь к порталу Butter Box. Перейдите в раздел [Быстрый старт](../../quick-start.md) для получения дополнительной информации.
{% endstep %}
{% endstepper %}

**Если вы собираете расширенную коробку, перейдите к следующему разделу: Расширение вашей коробки.**

{% content-ref url="extend-your-box.md" %}
[extend-your-box.md](extend-your-box.md)
{% endcontent-ref %}



### Устранение неполадок

Если вы видите ошибку, указывающую, что входной файл не является допустимым образом диска, проверьте скачанный файл.

Убедитесь, что размер файла совпадает с размером, указанным на сайте. Иногда браузеры не завершают загрузку, что может привести к повреждению файла.

Также убедитесь, что вы **распаковали файл** перед использованием.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 1.28.37 PM.png" alt=""><figcaption></figcaption></figure>
