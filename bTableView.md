---
layout: page
title: TableView
permalink: /tableView/
---


Zadanie 1
----------

Przenieś metody delegatów ```UITableViewDataSource``` oraz  ```UITableViewDelegate``` do ```Extension``` klasy ```ArtistViewController```

Zadanie 2
-----------

Stwórz dwa obiekty typu ```SpotifyItemSection``` dla obiektów typu ```Album``` i ```Track``` z parametrami

Album

* ```title: "Albums"```
* ```limit: 4```
* ```cellHeight: 60```

Tracks

* ```title: "Tracks"```
* ```limit: 8```
* ```cellHeight: 45```
                                                                                                  
Stwórz tablicę o nazwie ```sections``` z nowopowstałymi obiektami. 


Zadanie 3
-----------

Musimy zaktualizować funkcje  ```getTopTracks()``` oraz  ```getAlbums()```. 
Dodaj do nich parametr ```section``` typu  ```SpotifyItemSection``` o odpowiednim typie obiektu - ```Track``` lub ```Album```.

W przypadku pomyślnego otrzymania obiektu przypisz go do ```section.typedItems = tracks``` oraz ustaw ```section.expanded = false```

Odśwież tabelę w clousure  ```clearAllNotice(closure: () ->())```

Zadanie 4
-----------

Stwórz metodę zwracającą komorkę typu  ```AlbumTrackTableViewCell``` przy użyciu ```tableView.dequeReusableCell(indexPath:indexPath)```. Pamiętaj by w metodzie dodać paramter ```indexPath```.

Skonfiguruj komórkę obiektem  z tabeli ```typedItems``` odpowiedniej sekcji.

Powtórz powyższe czynności  dla  komórki typu ```SearchResultTableViewCell```

Zadanie 5
-----------

Korzystając z utworzonych w poprzednim zadaniu funkcji 
uzupełnij metodę 

 ```func tableView(tableView: UITableView, cellForRowAtIndexPath indexPath: NSIndexPath) -> UITableViewCell ```

tak, by w  zależności od typu obiektu sekcji zwracała odpowiedni typ komórki.


Zadanie 6
-----------
Bazując na ustawieniach poszczególnych sekcji  naszej tablicy o nazwie ```sections``` skonfiguruj poniższe metody:

 ```numberOfSectionsInTableView(tableView: UITableView) -> Int```
 
``` tableView(tableView: UITableView, titleForHeaderInSection section: Int) -> String?```
 
  ```tableView(tableView: UITableView, heightForRowAtIndexPath indexPath: NSIndexPath) -> CGFloat```
  
  ```tableView(tableView: UITableView, numberOfRowsInSection section: Int) -> Int ```
 

Zadanie 7
-----------
 
Przenieś tworzenie nowych  kontrolerów do osobnych metod przyjmujących jako parametr przekazywany obiekt  ```album```
dla  ```AlbumViewController``` oraz  ```track``` dla ```PlayerViewController```

W metodzie
```tableView(tableView: UITableView, didSelectRowAtIndexPath indexPath: NSIndexPath)  ```
 
w zależności od typu obiektu klikniętej komórki wywołaj odpowiednią  funkcję tworzącą kontroler następnego widoku.

Dla .Artist - pokaż fatal error

Zadanie 8
-----------
Nadpisz metodę
 ```tableView(tableView: UITableView, viewForFooterInSection section: Int) -> UIView?```
 
Jeżeli paramter sekcji ```hasMore``` jest prawdziwy stwórz przy pomocy metody ```tableView.dequeueReusableHeaderFooterView()``` obiekt typu  ```MoreResultsFooterView?```.

Stwórz metodę ```reloadSection(section: Int)``` która przeładowuje naszą wskazaną sekcję w naszej tabeli z efektem .Fade.

W nowostworzonym obiekcie przypisz do tapAction .....
JAK TO OPISAC 
ustaw na aktualnej sekcji ```expanded = true``` oraz wywołaj utworzoną metodę ```reloadSection(section: Int)```

W funkcji  zwróć odpowiednią wartość wysokości stopki ```tableView(tableView: UITableView, heightForFooterInSection section: Int) -> CGFloat ```

Jeśli parametr sekcji ```hasMore``` posiada wartość ```true``` ustaw wysokość Footera na ```45.0```. W przeciwnym przypadku niech funkcja zwróci ```CGFloat.min```


