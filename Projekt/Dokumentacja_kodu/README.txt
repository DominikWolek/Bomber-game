BOMBERMAN
---------
Projekt zosta� wykonany w silniku Godot. Jest to silnik na licencji MIT do tworzenia gier
2D oraz 3D. Gry oparte na silniku mog� by� tworzone w C++, my jednak zdecydowali�my si�
napisa� gr� w skryptowym j�zyku godota - GDScript. U�ywa on sk�adni podobnej do Pythona.
Wi�kszo�� z nas nie mia�a styczno�ci z tym j�zykiem oraz musia�a nauczy� si� sposobu w
jaki silnik dzia�a od zera.
Godot wspiera platformy Windows oraz X11 (Linux).
Wszystkie tilesety oraz animacje s� oparte na licencji CC0. Dwie mapy zosta�y wykonane
przez Filipa Sow�. Wygl�d bomby jest wzorowany na zagranicznym kanale YouTube'owym:
https://www.youtube.com/user/CommentisAnonymous. Uzyskali�my zgod� od tw�rcy na umieszczenie
tego wygl�du w naszym projekcie.
---------
Wymagania systemowe: 
Windows 7 lub nowszy, macOS 10.10 lub nowszy, Linux (64-bit lub 32-bit x86)
Hardware wspomagaj�cy OpenGL 3.3 Core Profile
---------
Godot opiera si� na idei scen oraz w�z��w. Jest ona najlepiej opisana na stronie Godota
docs.godotengine.org. Oto kr�tki opis zar�wno w�z��w, jak i scen:

W�z�y s� fundamentalnym elementem tworzenia gry. W�ze� mo�e wykonywa� r�ne 
wyspecjalizowane funkcje. Jednak dany w�ze� zawsze posiada nast�puj�ce atrybuty:
- Ma nazw�.
- Posiada w�a�ciwo�ci kt�re mo�na edytowa�.
- Mo�e wywo�ywa� zwrot co ka�d� klatk�.
- Mo�e by� rozbudowywany (aby mie� wi�cej funkcji).
- Mo�e by� dodany do innego w�z�a jako dziecko.
W�z�y mog� mie� inne w�z�y jako dzieci. W�z�y u�o�one w ten spos�b staj� si� drzewem.

Scena sk�ada si� z grupy w�z��w zorganizowanych hierarchicznie (w spos�b drzewiasty). 
Co wi�cej, scena:
- zawsze ma jeden w�ze� g��wny.
- mo�e zosta� zapisana na dysku i wczytana z powrotem.
- mo�e by� instancjonowana.
Uruchomienie gry oznacza uruchomienie sceny. Projekt mo�e zawiera� kilka scen, 
ale aby gra mog�a si� rozpocz��, jedna z nich musi by� wybrana jako scena g��wna.

---------
Spos�b kompilacji oraz instrukcja obs�ugi znajduj� si� w folderze "Dokumentacja projektu".
Ze wzgl�du na ci�ki wyb�r najwa�niejszych metod i zmiennych z naszego projektu komentarze
dotycz�ce funkcji/metod oraz zmiennych znajduj� si� bezpo�rednio w kodzie programu za��czonego
w folderze "Kod".
Kr�tkie przedstawienie najwa�niejszych w�z��w w naszym projekcie:
ConfigurationNode - odpowiedzialny za konfiguracje gry (mapa, dane graczy itp.). Zmiany dokonywane
przez gracza zapisywane s� w pliku config.cfg, oraz dane czytane s� z tego pliku. Wykorzystywany m.in
w scenach CharacterSettings, Sounds, MapScene.
Board - jest w�z�em okre�lanym jako TileMap. Wczytywane s� do niego odpowiednie tekstury. Board z za�o�enia
jest rodzicem Player�w oraz Bot�w. Na tym w�le wykonywane s� operacje zwi�zane m.in z podk�adaniem bomby.
Player - w�ze� b�d�cy graczem. Obs�ugiwane s� w nim operacje zwi�zane ze sterowaniem postaci� oraz akcje
takie jak utrata �ycia, zwi�kszenie �ycia gracza itp.
Bot - dziedziczy po Playerze. Do jego obs�ugi utworzyli�my algorytm, kt�ry odpowiada za odpowiednie
podk�adanie bomb oraz odpowiednie poruszanie si�.

