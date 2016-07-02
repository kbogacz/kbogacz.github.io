---
layout: page
title: TableView
permalink: /tableView/
---


Zadanie 1
----------

Przenieś metody delegatów ```UITableViewDataSource``` oraz  ```UITableViewDelegate``` do ```Extension``` klasy

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

W przypadku pomyślnego ptrzymania obiektu przypisz go do ```section.typedItems = tracks``` oraz ustaw ```section.expanded = false```

Odwiez tabele w clouserze  ```clearAllNotice(closure: () ->())```

Zadanie 4
-----------

Stwórz metodę zwracającą komorkę typu  ```AlbumTrackTableViewCell``` przy użyciu ```tableView.dequeReusableCell(indexPath:indexPath)```. Pamiętaj by w metodzie dodać paramter ```indexPath```.

Skonfiguruj celkę obiektem  z tabeli ```typedItems``` odpowiedniej sekcji.

Powtórz powyższe czynności  dla ```SearchResultTableViewCell```

Zadanie 5
-----------

Korzystając z utworzonych w poprzednim zadaniu funkcji 
uzupełnij metodę 

 ```func tableView(tableView: UITableView, cellForRowAtIndexPath indexPath: NSIndexPath) -> UITableViewCell ```

tak, by w  zaleznosci od typu obiektu sekcji zwracała odpowiedni typ komórki.


Zadanie 6
-----------
Bazujac na ustawieniach poszczególnych sekcji w  naszesz tablicy o nazwie ```sections``` skonfiguruj poniższe metody:

 ```numberOfSectionsInTableView(tableView: UITableView) -> Int```
 
``` tableView(tableView: UITableView, titleForHeaderInSection section: Int) -> String?```
 
  ```tableView(tableView: UITableView, heightForRowAtIndexPath indexPath: NSIndexPath) -> CGFloat```
  
  ```tableView(tableView: UITableView, numberOfRowsInSection section: Int) -> Int ```
 

Zadanie 7
-----------

Zrefaktoruj tworzenie nowego kontolera do osobnej metody przyjmujacej jako parametr przekazywany obiekt  ```album```
dla  ```AlbumViewController``` oraz  ```track``` dla ```PlayerViewController```

 ```tableView(tableView: UITableView, didSelectRowAtIndexPath indexPath: NSIndexPath)  ```

W zależności od typu obiektu klikniętej komórki wywołaj odpowiednią metodę tworzącą kontroler następnego widoku.

Dla .Artist - pokaż fatal error

Zadanie 8
-----------

