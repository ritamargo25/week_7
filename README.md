Вопросы. Неделя 7
1. Как сделать так, чтобы при просмотре на телефоне текст стал читаемым, а картинка - большой? 
Для этого в начале файла html, где мы прописывает команды под тегом <meta> мы устанавливаем initial-scale=1. Тогда размер страницы будет равен 100% от области просмотра. И прописываем, что ширина страницы должна быть равна ширине экрана девайса, с которого открывают сайт. 
Выглядет это будет так:

2. В чём разница между отзывчивым и адаптивным веб-дизайном?Responsive дизайн - используется один макет, который открывается на всех устройствах.  Adaptive дизайн - для каждого устройства с разной величиной экрана мы делаем свой макет (компьютер, планшет, смартфон) или используем медиа-условия (как сайт будет выглядеть на том или ином устройстве)

3. Какие величины лучше использовать для шрифтов в гибком дизайне? 
лучше всего использовать em и rem (браузер сам конвертирует ее в пиксели)

4. Какой вид верстки использован на этой картинке? К какой категории шаблонов он относится? 
Использована блочная верстка, сайт состоит из блоков (header, sidebar, main, footer)
Адаптивная, так как подстраивается под размеры экрана устройства

5. Как задать стили для экранов шириной от 800 до 1200 пикселей? 
с помощью медиа запроса @media (min-width: 800px) and (max-width: 1200px)

6. Приведите минимум 2 примера как подключать медиазапросы?
a) в файле html там где мы прикрепляем ссылку на файл css <link rel=‘’ stylesheet’’ media=screen and (color)’’ href=‘’styles.css’’>
b) внутри таблицы стилей css, через правило media: @media (max-width: 800px)

7. Как можно задавать гибкие изображения?
a) c помощью свойства max-width. Задаем процентную величину (на столько % изображение будет увеличиваться максимум до этого процента при изменении размера окна браузера)
b) через тег <picture> в котором мы также указываем свойство max-width и процентную величину

8. Как задать стили только для landscape поворота экрана? И что вообще такое landscape и чем он отличается от portrait?
Landscape - это альбомная ориентация страницы (например экран компьютера либо планшета и смартфона, но в перевернутом виде, где ширина больше высоты). Чтобы ее задать, нужно воспользоваться функцией orientation в медиа запросе: @media (orientation: landscape)
Landscape ориентация отличается от portrait тем, что у нее ширина больше высоты, а у portrait наоборот.

9. Назовите минимум 3 способа как можно тестировать, как выглядит сайт при разных размерах экранов?
а) c помощью Chrome dev tools. В браузере Chrome на странице сайта нажать правой кнопкой мыши и открыть dev tools, нажать на значок устройства (планшет/телефон) и на верхней панели выбрать разные устройства. В разных браузерах это делается по-своему.
b) с помощью сайта http://mattkersley.com/responsive/ (помимо этого сайта существуют разные сервисы по проверке)
c) для браузера Chrome существует расширение Responsive viewer, с помощью которого модно провести проверку

10. Самостоятельно изучите, как можно подключить несколько картинок разных размеров через один тег <img>?
Стандартный тег <img> позволяет добавить только 1 изображение. Но если добавить атрибуты srcset и sizes. С их помощью мы можем добавить 
дополнительные изображения с пометками, чтобы браузер выбрал подходящее (пометки - это разные размеры этого изображения)
e.g: <img srcset=‘’имя_файла.jpg 430w, имя_файла.jpg 520w, имя_файла.jpg 630w’’ sizes=‘’ (max-width: 430px) 280px, (max-width: 520px) 440px’’
где:
srcset - включает название изображения, среди которых браузер выберет нужное и их размеры
430w, 520w, 630w - настоящая ширина изображения
sizes - определяет перечень медиавыражений и указывает предпочтительную ширину изображения, если это медиавыражение истинно.
max-width - это медиаусловие
320px, 480px - это возможное состояние экрана
280px, 440px - ширина места, которое будет занимать изображение, если медиавыражение истинно.
ВАЖНО! для ширины места мы НЕ указываем %, только em, vw или px.
Если одни из изображений мы оставляем без медиа условия, то оно становится изображением по умолчанию и будет актуальным, если ни одно из медиаусловий не будет истинным.


3. Сделать пример из статьи [https://habr.com/ru/company/edison/blog/344878/](https://habr.com/ru/company/edison/blog/344878/)

Отчетность - код и видео работы страницы при изменении размера
ВИДЕО (код в файлах)

https://user-images.githubusercontent.com/110172816/190866500-8f383349-9979-4efd-9937-d46022ec4b89.mov


