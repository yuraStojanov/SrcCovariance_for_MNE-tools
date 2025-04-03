Модификация библиотеки MNE python для использования ковариационной матрицы источников в расчетах
## Установка
заменить файл:*расположение оболочки python*\Lib\site-packages\mne\minimum_norm
## Использование 

source_std  = ...#ваша ков. матрица источников

inverse_operator = mne.minimum_norm.make_inverse_operator(
    info=evoked.info, forward=forward, noise_cov=noise_cov, loose=0.0, source_std = source_std, depth=None
)

