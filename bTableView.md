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

clean up cellForRowat IndexPath
w zaleznosci od itemType sekcji odpal odpowiednia metode do stworzenia celki

Zadanie 6
-----------

numbersOfRows bazujac na ilosc elementow w kazdej sekcji
nubers of sections bazujac na ilosci naszych sekcji

task DidSelecRowAtIndexPath
zrefaktoruj tworzenie nowego kontolera to osobnej metody przyjmujacej jako parametr przekazywany obiekt album
oraz dla PLayer przyjmujacy track
did selecet - w zaleznosci od typu obiektu itemType kliknietej celki pushnij odpowiednij kontroler
.Artist - pokaz fatal error

Zadanie 7
-----------

titleForHeaderInSection
zwroc title dla danego obiektu sections
height for row
zwroc cellHeight