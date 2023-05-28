# Содержание
1. [Диаграммы использования](#1) <br>
	1.1. [Описание актёров](#1.1) <br> 
	1.2. [Варианты использования (сценарии)](#1.2) <br>
		1.2.1 [Открыть справку](#1.2.1) <br>
      			1.2.1.1 [Поток событий](#1.2.1.1) <br>
		1.2.2 [Настройки](#1.2.2) <br>
      			1.2.2.1 [Поток событий](#1.2.2.1) <br>
		1.2.3 [Начать тренировку](#1.2.3) <br>
      			1.2.3.1 [Поток событий](#1.2.3.1) <br>
 # 1. Диаграммы использования <a name = "1"></a>
 ![UseCase](https://github.com/AnastasiaKviatsinskaya/tritpo/blob/master/Diagrams/Use%20case/Use%20Case%20Diagram.png)
 ## 1.1 Описание актёров <a name = "1.1"></a>
 
Класс пользователя     | Описание
:----------------------|:-------------------------------------------------------
Artist  | Пользователь, который учится печатать десятипальцевым методом

## 1.2 Варианты использования <a name = "1.2"></a>

### 1.2.1 Открыть справку <a name = "1.2.1"></a>
**Описание.** Вариант использования "Открыть справку" дает пользователю возможность прочитать справочную информацию о приложении
**Основной поток:**
1. Приложение отображает пользователю окно со справочной информацией. 
2. Вариант использования завершается.

### 1.2.2 Настройки <a name = "1.2.2"></a>
**Описание.** Вариант использования "Настройки" дает пользователю возможность настроить интерфейс и тренировку на свое усмотрение

#### 1.2.2.1 Поток событий <a name = "1.2.2.1"></a>
**Основной поток:**
1. Приложение отображает пользователю окно настроек. 
2. Пользователь выставляет значения на свое усмотрение.
3. При нажатии на кнопку "Сохранить" выставленные значение сохраняются.
4. Обновляется окно настроек.
5. Вариант использования завершается.

### 1.2.3 Начать тренировку <a name = "1.2.3"></a>
**Описание.** Вариант использования "Начать тренировку" дает пользователю возможность начать обучение десятипальцевому методу печати

#### 1.2.3.1 Поток событий <a name = "1.2.3.1"></a>
**Основной поток:**
1. Приложение отображает пользователю окно для тренировки.
2. Пользователь может выбрать уровень (текст) тренировки перед ее началом.
3. При нажатии на кнопку старт тренировка начинается и на экране появляется текст.
4. При тренировку на скорость выполняется альтернативный поток А1.
5. При обучающей тренировке выполняется альтернативный поток А2.
6. Вариант использования завершается.

**Альтернативный поток А1:**
1. Запускается таймер.
2. При вводе последнего символа тренировочного текста подсчитывается скорость набора текста.
3. Возврат к п.6 основного потока.

**Альтернативный поток А2:**
1. Подсчет ошибок, совершенных пользователем при наборе тренировочного текста.
2. При вводе последнего символа тренировочного текста подсчитывается правильность набора текста.
3. Если правильность выше 80% происходит переход на новый уровень.
4. Возврат к п.5 основного потока.


