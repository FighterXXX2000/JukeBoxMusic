# Soviet Jukebox
### Как добавить песню в джукбокс:
+ Заливам файл в папку files. Песня должна быть в формате mp3. Так же поддерживаются и другие форматы, включая видеофайлы, но какие точно я не помню. Помню, что ogg, вроде как, работать не хочет.
+ Добавляем запись о файле в playlist.json:

<pre>
1."Oddity.mp3":{
2.    "album":"Space",
3.    "orig_filename":"Oddity.mp3",
4.    "playlists":[
        "bar"
        ],
5.    "playtime_seconds":"326",
6.    "title":"Space Oddity",
7.	  "artist":"Chris Headfield"
  },</pre>

1. - Это название вашего файла. Если файл был залит куда-то в новую папку внутри папки files, то эта строка так же должна содержать этот путь. Например, "songs_from_space/space_oddity.mp3". Важнейшая переменная.
2. - Название альбома. Отображается в интерфейсе джукбокса и выводится в чат при старте песни. Не особо важно, можно не заполнять.
3. - Уже не нужная переменная, оставшаяся от старого формата, лучше вообще не использовать и удалить их все из файла плейлиста.
4. - Список плейлистов, в которые входит песня. Например: "playlists":["bar","jazz"],
Полный список текущих плейлистов можно найти в файле code/modules/media/jukebox.dm. На текущий момент есть такие плейлисты: "bar", "jazz", "rock", "muzak", "emagged", "endgame", "clockwork", "vidyaone", "vidyatwo", "vidyathree", "vidyafour".
5. - Длительность композиции в секундах. НЕ в тиках, в тиках оно само посчитает. Достаточно важная переменная.
6. - Название композиции. Отображается в интерфейсе джукбокса и выводится в чат при старте песни. Достаточно важная переменная.
7. - Исполнитель композиции. Отображается в интерфейсе джукбокса и выводится в чат при старте песни. Достаточно важная переменная.

Порядок переменных можно менять как угодно.