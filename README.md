# Face Emotion Recognition Model

Реализация скрипта для определения эмоции на кадрах с вебкамеры

Для запуска скрипта необходимо убедится что установлены библиотеки

    TensorFlow
    Scipy
    NumPy
    MediaPipe
    OpenCV
    MatPlotLib

Так же для работы с вебкамерой необходимо установить v4l-utils

    sudo apt install v4l-utils

Команда для проверки доступных вебкамер

    v4l2-ctl --list-devices

Предобученные веса для модели должны быть в формате .h5 и находиться рядом со скриптом в папке /weights

    /weights/model_class_weights.h5
    /weights/model_va_weights.h5

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

Модель имеет два варианта определения эмоции

    Классификация
    Valence-arousal регрессия

При запуске модель запрашивает вариант определния эмоции

    class - для определения моции путем классификации изображений
    va - для определения координат эмоции

Для обучения весов va модели, использовался finetuning модели классификации