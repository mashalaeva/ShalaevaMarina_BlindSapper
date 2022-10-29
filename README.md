# Тестовое задание Defold Junior Игра  «Слепой сапер»

## Шалаева Марина

В ходе выполнения работы возникла следующая проблема: таймер, по истечении времени работы которого должны были меняться цвета мин (кругов) с синего и красного на серый, работал некорректно. Эмпирически было выведено, что таймер начинал работу раньше, чем команда ```msg.post(...)``` присылала уведомление о запуске какого-либо события в другой скрипт, независимо от расположения строчек кода друг относительно друга. Решением данной проблемы в моем случае стало добавление дополнительной кнопки. После этого для старта игры стало необходимо сделать следующее:

* Нажать на кнопку «Spawn», которая разместит красные и синие круги на поле. После нажатия на кнопку «Spawn» ее текст изменится на «Respawn», а также станет доступна кнопка «Start»;
* Нажать на кнопку «Start». После нажатия на кнопку она вновь скроется, а цвета кругов изменятся на серый. Только после этого можно будет начать саму игру;
* В случае проигрыша / выигрыша / желания начать игру сначала, следует нажать на кнопку «Respawn» и вновь действовать в соотвествии с пунктами этого списка.

Также возник следующий вопрос: как обозначить игроку его победу в случае, если он откроет все 50 кругов одного цвета. Было принято решение сразу после 50-ого набранного балла заканчивать игру и выводить фразу «You win! Your score is 50» вместо фразы «Game is over! Your score is ...». После этого можно начать игру заново.
