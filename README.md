# Face Emotion Recognition Model

Реализация скрипта для определения эмоции на кадрах с вебкамеры

Для запуска скрипта необходимо убедится что установлены библиотеки

    TensorFlow
    Scipy
    NumPy
    MediaPipe
    OpenCV

Так же для работы с вебкамерой необходимо установить v4l-utils

    sudo apt install v4l-utils

Команда для проверки доступных вебкамер

    v4l2-ctl --list-devices

Модель имеет два варианта определения эмоции

    Классификация
    Valence-arousal регрессия

При запуске модель запрашивает вариант определния эмоции

    class - для определения моции путем классификации изображений
    va - для определения координат эмоции

Модель определяет 9 эмоции

    anger
    contempt
    disgust
    fear
    happy
    neutral
    sad
    surprise
    uncertain