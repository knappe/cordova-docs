* * *

license: Licensed to the Apache Software Foundation (ASF) under one or more contributor license agreements. See the NOTICE file distributed with this work for additional information regarding copyright ownership. The ASF licenses this file to you under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0
    
         Unless required by applicable law or agreed to in writing,
         software distributed under the License is distributed on an
         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
         KIND, either express or implied.  See the License for the
         specific language governing permissions and limitations
    

## under the License.

# Конфигурация iOS

Файл `config.xml` управляет основные параметрами приложения, которые применяются к каждому приложению и экземпляру CordovaWebView. Этот раздел описывает настройки, которые применяются только к платформе iOS. Смотрите раздел "Файл config.xml" для получения информации о глобальных параметрах конфигурации.

*   `EnableViewportScale` (логическое значение, по умолчанию `false`): Установите `true` чтобы разрешить тегу meta viewport либо отключить или ограничить диапазон масштабирования экрана пользователем, который включен по умолчанию.
    
        <preference name="EnableViewportScale" value="true"/>
        
    
    Установите viewport следующим образом в HTML, чтобы отключить масштабирование и гибко подстраивать содержимое в WebView во время отрисовывания:
    
        < мета имя = «просмотра» содержание =' ширина = устройства ширина, первоначальный масштаб = 1, пользователь масштабируемых = no' / >
        

*   `MediaPlaybackRequiresUserAction` (логическое значение, по умолчанию `false` ): Установите `true` чтобы запретить автоматическое воспроизведение HTML5 видео или аудио с использованием атрибуте `autoplay` или через JavaScript.
    
        <preference name="MediaPlaybackRequiresUserAction" value="true"/>
        

*   `AllowInlineMediaPlayback` (логическое значение, по умолчанию `false` ): Установите `true` чтобы разрешить воспроизведение мультимедиа HTML5 появляться *встроено* в пределах экрана, с помощью стандартных элементов управления браузера, а не элементы управления платформы. Чтобы это работало, добавьте атрибут `webkit-playsinline` к любому элементу `<video>`.
    
        <preference name="AllowInlineMediaPlayback" value="true"/>
        

*   `BackupWebStorage` (строка, либо `none`, `local`, или значение по умолчанию `cloud`): Установите `cloud` чтобы разрешить сохранение веб-данных при резервном копировании через iCloud. Установите `local` для того чтобы разрешить только в локальных резервных копия при синхронизации через iTunes. Установите `none` чтобы предотвратить создание резервных копий веб-данных.
    
        <preference name="BackupWebStorage" value="local"/>
        

*   `TopActivityIndicator` (строка, по умолчанию `gray` ): контролирует появление небольшого вращающийся значка в строке состояния, указывающее значительную активность процессора. Допустимыми значениями являются `whiteLarge`, `white`, и `gray`.
    
        <preference name="TopActivityIndicator" value="white"/>
        

*   `KeyboardDisplayRequiresUserAction` (логическое значение, по умолчанию `true`): Установите `false` чтобы разрешить клавиатуре появляются при вызове `focus()` на формах ввода.
    
        <preference name="KeyboardDisplayRequiresUserAction" value="false"/>
        

*   `SuppressesIncrementalRendering` (логическое значение, по умолчанию `false` ): Установите `true` чтобы ожидать, пока все содержимое будет получено до того, как оно будет отображаться на экране.
    
        <preference name="SuppressesIncrementalRendering" value="true"/>
        

*   `GapBetweenPages`(float, значение по умолчанию `` ): размер разрыва, в точках, между страницами.
    
        <preference name="GapBetweenPages" value="0"/>
        

*   `PageLength` (float, значение по умолчанию ``): размер каждой страницы, в точках, в направление протяженности страницы. Когда PaginationMode — справа налево или слева направо, это свойство представляет ширину каждой страницы. Когда PaginationMode сверху вниз или снизу вверх, это свойство представляет высоту каждой страницы. Значение по умолчанию равно 0, что означает, что макет использует размер viewport-а, чтобы определить размеры страницы.
    
        <preference name="PageLength" value="0"/>
        

*   `PaginationBreakingMode` (строки, по умолчанию `page`): допустимые значения `page` и `column`. Порядок, в котором происходит разрыв столбца или страницы. Это свойство определяет, будут ли определенные CSS свойства относительно разрыва столбца и страницы применяться или игнорироваться. Когда это свойство имеет значение `column`, содержимое страницы обрабатывает CSS свойства, относящиеся к разрыву колонки в месте разрыва страницы.
    
        <preference name="PaginationBreakingMode" value="page"/>
        

*   `PaginationMode` (строка, по умолчанию `unpaginated`): допустимые значения `unpaginated`, `leftToRight`, `topToBottom`, `bottomToTop`, и `rightToLeft`. Это свойство определяет является ли содержимое в WebView разбитым на страницы, которые заполняют один экран одновременно, или как представлены один длинный прокручиваемый список. Если установить paginated, это свойство переключает страничный макет содержимого, заставляя WebView использовать значения использования значения PageLength и GapBetweenPages для перерисовки его содержимого.
    
        <preference name="PaginationMode" value="unpaginated"/>
        

*   `UIWebViewDecelerationSpeed` (строка, по умолчанию `normal` ): допустимые значения `normal`, `fast`. Это свойство контролирует скорость замедления импульса прокрутки. `normal` это скорость по умолчанию для большиства приложений платформы, и `fast` является значением по умолчанию для Mobile Safari.
    
        <preference name="UIWebViewDecelerationSpeed" value="fast" />