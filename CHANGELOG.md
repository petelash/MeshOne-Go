# Changelog / Popis promjena

**English** · [Hrvatski](#hrvatski)

All notable user-facing changes to MeshOne Go, newest first.

## 1.2.6

- **Contact circle colour:** long press a contact and choose "Circle colour" to pick one of 16 colours, or go back to automatic.

## 1.2.5

- **Coordinates in messages** (e.g. 45.562095,18.648674) are now links. Tap one to choose where to open it: the app's map, Google Maps, Apple Maps (in the browser) or another app, or copy it.

## 1.2.4

- **Long press for help**: long press a command button (also in the list of all commands) to see what it does, what value it takes and what it shows. The same works for the buttons in contact details and in the message route window (Chat, Log in, Trace, Discover path, Route, Reset path, status, telemetry, contact actions). It replaces the ? icon, which was not visible.
- Fixed the description of the *region load* command.
- **Contact categories** are now ordered *All*, ⭐ (favourites), *Users* (previously *Chat*), then the rest.

## 1.2.3

- **Reply in direct messages**: long press a received message and pick *Reply*; the first few words of that message are quoted above your answer.
- **Message path map**: node and repeater names are shown under their symbols, as on the main map; your own node is the flashing dot.
- **Main map legend**: *My node* now has the same flashing dot as on the map. The dot is now the same size as the other node symbols.

## 1.2.2
- **Automatic adding of contacts** now has a limit on how far away a new contact may be: a slider with − and + buttons, from 0 hops (direct only) to 32, or no limit (the default). It applies to the categories that are switched on. The window is also more compact.
- **Show on top**: long press a contact to keep it at the top of the list, whatever the sort order (*Remove from top* undoes it). The other contacts stay ordered as before.
- TX power: every value can now be picked (some, such as 12, 16 and 18 dBm, were skipped). The same fix applies to the spreading factor and coding rate sliders.

## 1.2.1
- The project has moved to a new GitHub repository, [petelash/MeshOne-Go](https://github.com/petelash/MeshOne-Go). From this version the app checks for updates there. After installing it, tap *Check for updates* once to make sure you have the latest version.

## 1.2.0
- **Contact permissions**: one new screen in Settings → Contacts and privacy replaces the three telemetry rows. For basic telemetry, location and environment you choose *Nobody*, *Selected contacts* or *Everybody*; with *Selected contacts* you pick the contacts one by one, or all favourites or all contacts at once. The same screen controls who may send **remote commands (CLI)** to your node.
- **Command line for companions**: in a direct chat with a companion contact, the ⋮ menu has *Command line*. It works only if that contact allowed remote commands for you; if it does not answer, the app says so.
- **Editable command buttons** in the repeater / room server console: *Edit* opens a list of all remote commands to switch on as buttons, add your own, reorder and restore the defaults. Commands with an argument only fill in the beginning, dangerous ones ask first. Companions have their own button list.
- **Telemetry on the map**: a GPS reading now shows a small map with the position and a *Show on map* button, on a contact and in My telemetry. On the map you can refresh that position, or have it refreshed automatically every few seconds (you choose how often).
- **Trace on map** (⋮ menu on the main screen): tap repeaters on the map in order, reorder them in the list, see the total distance, and run a trace. The path is exactly as you draw it (the same repeater can be picked up to 2 times, for the way back). After the reply every leg shows its SNR, coloured by quality, and the round-trip time is shown; if the path does not complete, the map shows how far the link reaches. A warning appears when two repeaters on the path share the same first key byte.
- A **?** icon next to the Trace / Discover path buttons explains the difference between them.
- **The app is now called MeshOne Go** (it was MeshCore Go), so it is not mistaken for the official MeshCore app. The icon keeps the same design, with the new name and a white “GO” flag.
- On the maps, your node is a circle whose centre flashes red every second, with its name next to it; contact and repeater names are shown on the main map too. A button on both maps takes you to your location (the connected node's position, or the phone's GPS if the node has none).
- *Trace on map* has a **Stop** button, and *Clear* is now *Delete*.
- If the node reports a battery of 0 V or 0 %, the app says the battery is not connected.
- When you have opened a position from telemetry, *Stop following* on the map removes it and returns the map to normal.
- Telemetry readings are labelled without the channel in brackets: *Temperature:*, or *Temperature 1:*, *Temperature 2:* when there are several of a kind.
- The contact list now opens on the *Chat* filter instead of *All*.
- All new texts are translated into all eight languages.

## 1.1.9
- New languages: **Romanian**, **Bulgarian** and **Slovenian**. The language is now chosen from a drop-down list in Settings → Appearance. In these three languages a text that is not translated yet is shown in English.

## 1.1.8
- Small improvements.

## 1.1.7
- Direct messages are retried more before they are marked as failed. With the automatic route and a known path: 3 attempts along the path, then 3 as flood; with no known path: 3 attempts as flood straight away. Always flood sends 3 as flood, and a manual path 3 along it. The "not delivered" mark appears only after the last attempt.

## 1.1.6
- Settings → Notifications: each kind of notification can have its own sound and vibration – private messages, channels, mentions in channels, chat rooms, detected #channels and link to the node dropped. The sound is chosen from the phone's sounds (or none), and the vibration is the phone's own or none; "More in the Android settings" opens the phone's page for that kind of notification, where some phones offer other vibration patterns too. "Same sound and vibration for all" uses one setting for every notification.
- Settings → Contacts: the automatic adding switches for each contact type are now in their own window ("Automatic adding of contacts").
- A sound or vibration set earlier in the Android settings for the old "Messages" notifications is not carried over and has to be chosen again.

## 1.1.5
- Settings → Contacts: automatic adding of new contacts can be turned on or off separately for chat (companion) nodes, repeaters, room servers and sensors (also in Received adverts → automatic adding). Needs node firmware that supports it; with older firmware the single "manual adding" switch stays.
- **Delete contacts** (menu ⋮ → Delete contacts…): delete many contacts from the node at once – by type (chat, repeaters, room servers, sensors), keeping favourites or not, and all of them or only those not heard from in 1 week, 1 month, 3 or 6 months. The list shows which contacts will go and single ones can be left out; you confirm before anything is deleted, and deleting can be stopped. Message history stays on the phone.
- Settings → Appearance → Font opens its own list instead of showing every font on the page, and has eight more fonts built in: Open Sans, Montserrat, Poppins, Inter, Nunito, Raleway, Roboto Slab and Rubik. The phone's own fonts are still there.

## 1.1.4
- WiFi / Tailscale: the app now notices when the link to the node silently drops (no internet, Tailscale path down, node without power). The battery query it already sends every minute doubles as a link check: if the node does not answer twice in a row, the link is treated as lost, just like with Bluetooth – the "link to the node dropped" notification is shown (if turned on) and the app reconnects by itself. When the phone switches networks, the link is checked right away.

## 1.1.3
- Connect → WiFi / Tailscale: a new card, **Use your node from anywhere**, describes the MeshCore Tailscale Companion firmware, which builds the Tailscale VPN into the node itself (no extra computer at home, no port forwarding, no public IP). It has buttons to open the web flasher and to share its link, since the flasher runs on a computer (Chrome or Edge).

## 1.1.2
- **Unread messages**: when you open a chat with unread messages, it opens at the first unread one, marked by a line with "Unread messages". Scroll down to the newer ones yourself; a new message moves the list down only when you are already at the bottom.
- "Proslijedilo repetitora" (repeaters that forwarded your message): the number is red while no repeater has forwarded the message and green from one up.

## 1.1.1
- **Channel order**: hold a channel in the Channels tab and drag it up or down to change the order. Holding without moving still opens the channel menu, which now also has **Restore original order**.
- The order is changed and saved **only in the app**, separately for each node, and stays after reconnecting and restarting the app. Nothing is written to the node: the channels keep their slots on the node, and other apps connected to the same node keep their own order.
- **Bluetooth search** shows two lists: **In range** (nodes found by the scan, strongest signal first, with signal bars and dBm, marked *saved* or *new*) and **Saved – not in range** (paired or saved nodes the scan did not find, greyed out but still tappable). The search starts by itself when the Bluetooth tab opens, and saved Bluetooth nodes are no longer listed twice. The signal shown is smoothed (median of the last readings), so the bars no longer flicker, and Bluetooth nodes paired only in Android can also be removed from the list (with a shortcut to the Bluetooth settings to unpair them).
- Saved nodes (WiFi, Tailscale, USB and Bluetooth) no longer have a delete icon: hold a node to remove it, and the app asks for confirmation first.
- Fixed: removing a node the app was still connecting to did not stop the attempts, and Cancel right after start-up could be undone by the background service starting the connection again.
- Fixed: "Proslijedilo repetitora" (repeaters that forwarded your message) stayed at 0 on a channel that exists in more than one slot with the same key, e.g. a second "Public" used with a scope.
- Croatian and Serbian wording: "heard" (čuti) is replaced everywhere, e.g. "Zadnje detektirani", "Detektirani kanali koje nemaš", "Detektiran je kanal …", "Proslijedilo repetitora: N" and "Tvoj signal kod repetitora".

## 1.1.0
- **Hungarian** language (Settings → Appearance → Language → Magyar).
- **Heard #channels you don't have**: the app recognises traffic on #channels that are not added (a built-in list of common channel, city and region names, your own names and channels mentioned in messages) and notifies once per channel, with **Add** and **Don't notify again** buttons. The same channels are listed at the top of the Channels tab, so you add only the ones you want.
- Settings → Notifications: turn these notifications on or off, add your own channel names to watch, and reset the channels you silenced.
- Settings → About: a **Changelog** link under the app version opens the changes of that version.
- Adding and removing a channel is now instant (the app no longer re-reads every channel slot from the node).
- Icon descriptions read by screen readers now follow the selected language.
- Fixed: the sensor contact type was shown as "Sensor" in Croatian and Serbian.

## 1.0.9
- Neighbour repeaters: signal status for each repeater – quality (excellent / good / weak / very weak) with SNR and RSSI, how well the repeater hears you, distance, and average / lowest / highest SNR.
- Neighbour repeaters: sort by last heard, strongest signal or nearest.
- Neighbour repeaters that are not contacts yet can be added with one tap (or all at once); the app first asks the repeater for its full name.
- A short (1-byte) code is merged with the repeater already identified by a longer code; when it still fits several repeaters, tapping the question mark explains which ones, nearest first.

## 1.0.8
- New **Neighbour repeaters** screen in the ⋮ menu (below Received adverts): the repeaters your node hears directly, with full names when known, SNR, RSSI, when each was last heard and how many packets came through it. The refresh button asks the repeaters in range to answer.

## 1.0.7
- Send advert button: a short press sends a zero-hop advert, a long press sends a flood advert.
- Tailscale → Devices in the tailnet: tap a device to connect to the MeshCore node on it (asks for confirmation first; the TCP port can be changed, default 5000).

## 1.0.6
- The number of new received adverts is shown only next to "Received adverts" in the ⋮ menu, no longer on the menu icon.

## 1.0.5
- Fixed notifications: the background connection service now always starts, so messages and notifications keep arriving after you leave the app.
- A chat left open in the background now notifies about new messages and keeps them unread until you return.
- Settings → Notifications warns when Android has notifications turned off for the app, with a shortcut to turn them on.

## 1.0.4
- Send advert button uses the ((•)) symbol, like the original app.
- Contact search opens from the top bar (magnifier icon) instead of a permanent search field.
- Received adverts moved to the ⋮ menu, with a counter of new nodes.

## 1.0.3
- The connection notification shows the node's battery and, over Bluetooth, the signal strength (over WiFi: LAN or Tailscale) instead of the Bluetooth address.
- The connection notification no longer adds an unread badge to the app icon.

## 1.0.2
- The search field looks like the category buttons below it (same outline and rounded corners, compact height) and has a clear button.

## 1.0.1
- **Discover regions in range** – when choosing a region scope (default or per channel), the app asks the repeaters in direct range which regions they serve and lets you pick one with a tap.

## 1.0.0 – first stable release
- Channel icons as in the original MeshCore app: ((•)) for Public, # for hashtag channels, a lock for private channels.

## 0.9.9
- Links in messages are underlined and open in the browser.
- Settings → Radio → **Path hash size** (1, 2 or 3 bytes per hop, stored on the node).
- Radio settings offer **all 48 regional presets**.
- TX power can no longer be set below 1 dBm.
- Notifications show only the MeshCore Go icon.

## 0.9.8
- Fixed the update check.
- Settings → About → **Licence**: MIT licence and the open-source components used.

## 0.9.6
- **In-app updates**: the app checks for new versions once a day and offers download and install (can be turned off).

## 0.9.5
- Contacts whose name ends with an emoji or flag get that emoji as their icon.
- Long-press a contact → **Contact icon**: automatic, 1 letter, 2 letters or any emoji.

## 0.9.1 – 0.9.4
- Each contact category (All, Chat, Repeaters, Chat rooms, Sensors, Favourites) can be sorted: favourites first, latest activity, A–Z or last heard. Long-press the category to change the order; the order is remembered per category.
- "Favourites first" lists favourites and then everyone else alphabetically.
- Better visibility of switches in the AMOLED theme.

## 0.9.0
- **Region scope**: default scope stored on the node and an individual scope per channel (default, no scope or a chosen region).
- **Notification settings**: direct messages, channels, chat rooms, mentions only, link-lost alert, sound and vibration.
- Per channel notifications: all messages, mentions only or muted. Contacts can be muted. Every message notification has a **Mute** button.
- New languages: **Serbian** and **German** (along with Croatian and English).

## 0.8.7
- **AMOLED theme** with the backgrounds of the original MeshCore app.

## 0.8.6
- The repeater `neighbors` command shows names, time and SNR instead of key prefixes.

## 0.8.5
- When a message arrived over several routes, the map shows **all routes at once in different colours**, with a legend.

## 0.8.3 – 0.8.4
- **Path on map** also for your own direct messages and your own channel messages.

## 0.8.2
- Every sent direct message shows how it went out: direct or flood, and which attempt.

## 0.8.1
- Long-press a contact: add to / remove from favourites, rename, delete.

## 0.7.9 – 0.8.0
- More compact lists (contacts, channels, settings, received adverts).

## 0.7.4 – 0.7.8
- **Received adverts** screen (like Discover in the original app): nodes heard by your node, filters by type, details, one-tap add, automatic adding on/off.
- With manual adding on, new adverts are no longer added to contacts automatically.
- "Heard by repeaters" counter under your channel messages.

## 0.7.1 – 0.7.3
- **Unread** button: shows how many conversations have unread messages and takes you straight to the newest one.
- Message path on the map drawn as a red dashed line with direction arrows.
- Layout fixes for Android 15 (no empty gaps above lists).

## 0.7.0
- Number of repeaters that heard your channel message, with the list of repeaters and their SNR.
- Long-press a message: reply (@mention), copy, path on map, resend, delete.
- **Message path on the map**: the repeaters a message travelled through.
- **DM route control**: automatic, always flood or a manual path through chosen repeaters.

## 0.6.0
- **Remember password** option for repeater and room server login (stored only on the phone).
- Notifications use the app icon.

## 0.5.0
- Official MeshCore node symbols on the map, coloured by how recently the node was heard.

## 0.4.0
- New app icon.
- **English** language (switch in Settings, along with Croatian).
- Author information in Settings → About.

## 0.3.0
- **Automatic connection route**: at home the app connects directly over WiFi, away from home through Tailscale – nothing to switch manually.
- Simple, round node symbols on the map.

## 0.2.0
- The app is now called **MeshCore Go**.
- Connect to nodes **over the local network without Tailscale, over Bluetooth LE and over USB**.
- Separate map symbols for companions, repeaters, room servers and sensors.
- Adjustable **font size** and choice of fonts.
- **Always running in the background**: ignores battery optimisation, keeps the link to the node and **reconnects automatically** (each can be turned on or off).

## 0.1.0 – first version
- Android MeshCore client with **Tailscale built in**: no separate Tailscale app or system VPN is needed. Sign in with a Tailscale auth key or through the browser.
- Connection to a WiFi companion node over TCP, through your tailnet.
- Contacts, channels and direct messages with delivery receipts; room servers.
- Repeater administration: login, status, trace and CLI console.
- Map of nodes.
- Layout and flow like the original MeshCore app (Contacts, Channels, Map, Settings), in its own design.

---

<a id="hrvatski"></a>
# Popis promjena (hrvatski)

Sve važnije promjene u MeshOne Go za korisnike, od najnovije.

## 1.2.6

- **Boja kruga kontakta:** dugim pritiskom na kontakt odaberi "Boja kruga" i uzmi jednu od 16 boja ili vrati automatsku.

## 1.2.5

- **Koordinate u porukama** (npr. 45.562095,18.648674) sada su poveznice. Dodirom biraš gdje ih otvoriti: na karti aplikacije, u Google Maps, Apple Maps (u pregledniku) ili drugoj aplikaciji, ili ih kopiraš.

## 1.2.4

- **Objašnjenje na dugi pritisak**: dugim pritiskom na gumb naredbe (i na popisu svih naredbi) vidiš što radi, koju vrijednost prima i što pokazuje. Isto vrijedi za gumbe u detaljima kontakta i u prozoru za rutu poruka (Chat, Prijava, Trace, Otkrij putanju, Ruta, Reset putanje, status, telemetrija, radnje s kontaktom). To zamjenjuje ikonu ?, koja se nije vidjela.
- Ispravljen opis naredbe *region load*.
- **Kategorije kontakata** sada idu redom *Svi*, ⭐ (favoriti), *Korisnici* (prije *Chat*), pa ostale.

## 1.2.3

- **Odgovor na izravne poruke**: dugim pritiskom na primljenu poruku odaberi *Odgovori*; iznad tvog odgovora citira se nekoliko prvih riječi te poruke.
- **Putanja poruke na karti**: ispod simbola pišu imena nodova i repetitora, kao na glavnoj karti; tvoj node je treptajuća točka.
- **Legenda glavne karte**: *Moj node* sada ima istu treptajuću točku kao na karti. Točka je sada iste veličine kao simboli ostalih nodova.

## 1.2.2
- **Automatsko dodavanje kontakata** sada ima ograničenje koliko novi kontakt smije biti udaljen: klizač s gumbima − i +, od 0 hopova (samo izravni) do 32, ili neograničeno (zadano). Vrijedi za uključene kategorije. Prozor je i zbijeniji.
- **Prikaži na vrhu**: dugim pritiskom na kontakt zadržiš ga na vrhu popisa, bez obzira na redoslijed (*Ukloni s vrha* to poništava). Ostali kontakti redaju se kao dosad.
- TX snaga: sada se mogu odabrati sve vrijednosti (neke, npr. 12, 16 i 18 dBm, preskakale su se). Isto je popravljeno na klizačima za spreading factor i coding rate.

## 1.2.1
- Projekt se preselio u novi GitHub repozitorij, [petelash/MeshOne-Go](https://github.com/petelash/MeshOne-Go). Od ove verzije aplikacija ondje provjerava ažuriranja. Nakon instalacije jednom dodirni *Provjeri za ažuriranja* da potvrdiš da imaš najnoviju verziju.

## 1.2.0
- **Dozvole kontakata**: novi ekran u Postavke → Kontakti i privatnost zamjenjuje tri retka telemetrije. Za osnovnu telemetriju, lokaciju i okolinu biraš *Nikome*, *Odabrani kontakti* ili *Svima*; kod *Odabranih kontakata* biraš kontakte jedan po jedan, ili sve favorite odnosno sve kontakte odjednom. Isti ekran određuje tko smije slati **udaljene naredbe (CLI)** tvom nodeu.
- **Naredbeni redak za companione**: u izravnom razgovoru s companion kontaktom u izborniku ⋮ je *Naredbeni redak*. Radi samo ako je taj kontakt dopustio udaljene naredbe za tebe; ako ne odgovara, aplikacija to kaže.
- **Uredivi gumbi naredbi** u konzoli repeatera / chat sobe: *Uredi* otvara popis svih udaljenih naredbi koje možeš uključiti kao gumbe, dodati vlastite, preslagati i vratiti zadano. Naredbe s argumentom samo upišu početak, a opasne prvo traže potvrdu. Companioni imaju vlastiti popis gumba.
- **Telemetrija na karti**: GPS očitanje sada prikazuje malu kartu s položajem i gumb *Pokaži na karti*, na kontaktu i u Mojoj telemetriji. Na karti možeš osvježiti taj položaj ili ga automatski osvježavati svakih nekoliko sekundi (sam biraš koliko često).
- **Trace preko karte** (izbornik ⋮ na glavnom ekranu): dodiruj repetitore na karti redom, preslaži ih u popisu, vidi ukupnu udaljenost i pokreni trace. Putanja je točno onakva kakvu nacrtaš (isti repetitor možeš odabrati do 2 puta, za povratak). Nakon odgovora svaki dio putanje prikazuje SNR, obojen prema kvaliteti, te vrijeme obilaska; ako putanja ne prođe do kraja, karta pokazuje dokle veza dopire. Upozorenje se pojavi kad dva repetitora na putanji imaju isti prvi bajt ključa.
- Ikona **?** uz gumbe Trace / Otkrij putanju objašnjava razliku među njima.
- **Aplikacija se sada zove MeshOne Go** (prije MeshCore Go), kako se ne bi zamijenila sa službenom aplikacijom MeshCore. Ikona je istog dizajna, s novim nazivom i bijelom zastavicom „GO”.
- Na kartama je tvoj node krug čija sredina svake sekunde zatreperi crveno, s nazivom uz njega; na glavnoj karti vide se i nazivi kontakata i repetitora. Gumb na obje karte vodi te na tvoju lokaciju (položaj spojenog noda ili GPS mobitela ako node nema lokaciju).
- *Trace preko karte* ima gumb **Prekini**, a *Očisti* je sada *Obriši*.
- Ako node javlja bateriju od 0 V ili 0 %, aplikacija piše da baterija nije spojena.
- Kad otvoriš položaj iz telemetrije, *Prestani pratiti* na karti ga uklanja i vraća kartu u normalan prikaz.
- Telemetrija više ne piše kanal u zagradi: *Temperatura:*, odnosno *Temperatura 1:*, *Temperatura 2:* kad ima više istih podataka.
- Popis kontakata sada se otvara na filtru *Chat* umjesto *Svi*.
- Svi novi tekstovi prevedeni su na svih osam jezika.

## 1.1.9
- Novi jezici: **rumunjski**, **bugarski** i **slovenski**. Jezik se sada bira iz padajućeg izbornika u Postavke → Izgled. U ta tri jezika tekst koji još nije preveden prikazuje se na engleskom.

## 1.1.8
- Manja poboljšanja.

## 1.1.7
- Privatne poruke se prije oznake „Nije isporučeno” pokušavaju slati više puta. S automatskom rutom i poznatom putanjom: 3 pokušaja putanjom, pa 3 floodom; ako putanja nije poznata: odmah 3 pokušaja floodom. „Uvijek flood” šalje 3 puta floodom, a ručna putanja 3 puta tom putanjom. Oznaka „Nije isporučeno” pojavi se tek nakon zadnjeg pokušaja.

## 1.1.6
- Postavke → Obavijesti: svaka vrsta obavijesti može imati svoj zvuk i vibraciju – privatne poruke, kanali, spominjanja u kanalima, chat sobe, detektirani #kanali i prekid veze s nodeom. Zvuk se bira među tonovima mobitela (ili bez zvuka), a vibracija je zadana vibracija mobitela ili bez vibracije; „Više u postavkama Androida” otvara Androidovu stranicu za tu vrstu obavijesti, gdje neki mobiteli nude i druge uzorke vibracije. „Isti zvuk i vibracija za sve” koristi jednu postavku za sve obavijesti.
- Postavke → Kontakti: prekidači za automatsko dodavanje po vrstama kontakata sada su u vlastitom prozoru („Automatsko dodavanje kontakata”).
- Zvuk ili vibracija ranije postavljeni u Androidovim postavkama za stare obavijesti „Poruke” ne prenose se i treba ih ponovno odabrati.

## 1.1.5
- Postavke → Kontakti: automatsko dodavanje novih kontakata može se zasebno uključiti ili isključiti za chat (companion) nodeove, repetitore, chat sobe (room servere) i senzore (i u Primljeni adverti → automatsko dodavanje). Potreban je firmware nodea koji to podržava; sa starijim firmwareom ostaje jedan prekidač za ručno dodavanje.
- **Brisanje kontakata** (izbornik ⋮ → Obriši kontakte…): brisanje više kontakata s nodea odjednom – po vrsti (chat, repetitori, chat sobe, senzori), sa ili bez favorita, i svih ili samo onih koji se nisu javili 1 tjedan, 1 mjesec, 3 ili 6 mjeseci. Popis pokazuje koji će kontakti biti obrisani i pojedine možeš izostaviti; prije brisanja traži se potvrda, a brisanje se može prekinuti. Povijest poruka ostaje na mobitelu.
- Postavke → Izgled → Font otvara vlastiti popis umjesto da su svi fontovi na stranici, a ugrađeno je i osam novih fontova: Open Sans, Montserrat, Poppins, Inter, Nunito, Raleway, Roboto Slab i Rubik. Fontovi sustava ostali su.

## 1.1.4
- WiFi / Tailscale: aplikacija sada primijeti kad veza s nodeom tiho padne (nema interneta, prekinut Tailscale put, node bez struje). Upit za bateriju koji ionako šalje svake minute služi i kao provjera veze: ako node dvaput zaredom ne odgovori, veza se smatra prekinutom, kao i kod Bluetootha – prikaže se obavijest o prekidu veze (ako je uključena) i aplikacija se sama ponovno spaja. Kad mobitel promijeni mrežu, veza se provjeri odmah.

## 1.1.3
- Spajanje → WiFi / Tailscale: nova kartica **Koristi svoj node s bilo kojeg mjesta** opisuje firmware MeshCore Tailscale Companion, koji Tailscale VPN ugrađuje u sam node (bez dodatnog računala kod kuće, bez otvaranja portova i bez javne IP adrese). Ima gumbe za otvaranje web flashera i dijeljenje njegovog linka, jer flasher radi na računalu (Chrome ili Edge).

## 1.1.2
- **Nepročitane poruke**: razgovor s nepročitanim porukama otvara se na prvoj nepročitanoj, označenoj crtom s natpisom „Nepročitane poruke”. Prema novijim porukama listaš sam; nova poruka pomiče popis prema dolje samo ako si već na dnu.
- „Proslijedilo repetitora”: broj je crven dok poruku nije proslijedio nijedan repetitor, a zelen od jednog naviše.

## 1.1.1
- **Redoslijed kanala**: drži kanal u kartici Kanali i povuci ga gore ili dolje da promijeniš redoslijed. Držanje bez pomicanja i dalje otvara izbornik kanala, u kojem je sada i **Vrati izvorni redoslijed**.
- Redoslijed se mijenja i sprema **samo u aplikaciji**, posebno za svaki node, i ostaje nakon ponovnog spajanja i ponovnog pokretanja aplikacije. Na node se ništa ne zapisuje: kanali na nodeu ostaju na svojim mjestima, a druge aplikacije spojene na isti node zadržavaju svoj redoslijed.
- **Bluetooth pretraga** prikazuje dva popisa: **U dometu** (nodeovi koje je pretraga pronašla, od najjačeg signala, s crticama signala i dBm, označeni kao *spremljen* ili *novi*) i **Spremljeni – nisu u dometu** (upareni ili spremljeni nodeovi koje pretraga nije pronašla, sivi, ali se i dalje mogu odabrati). Pretraga se pokreće sama kad otvoriš karticu Bluetooth, a spremljeni Bluetooth nodeovi više se ne prikazuju dvaput. Prikazani signal je izglađen (medijan zadnjih očitanja), pa crtice više ne titraju, a i Bluetooth nodeovi upareni samo u Androidu mogu se ukloniti s popisa (uz prečac do postavki Bluetootha za raskidanje uparivanja).
- Spremljeni nodeovi (WiFi, Tailscale, USB i Bluetooth) više nemaju ikonu za brisanje: drži node da ga ukloniš, a aplikacija prije toga traži potvrdu.
- Ispravljeno: brisanje nodea na koji se aplikacija još spajala nije zaustavljalo pokušaje, a „Odustani” odmah nakon pokretanja mogla je poništiti pozadinska usluga ponovnim spajanjem.
- Ispravljeno: „Proslijedilo repetitora” ostajao je na 0 na kanalu koji postoji u više mjesta s istim ključem, npr. drugi „Public” koji se koristi sa scopeom.
- Izraz „čuti” zamijenjen je u cijeloj aplikaciji, npr. „Zadnje detektirani”, „Detektirani kanali koje nemaš”, „Detektiran je kanal …”, „Proslijedilo repetitora: N” i „Tvoj signal kod repetitora” (i na srpskom).

## 1.1.0
- **Mađarski** jezik (Postavke → Izgled → Jezik → Magyar).
- **Čuti #kanali koje nemaš**: aplikacija prepoznaje promet na #kanalima koji nisu dodani (ugrađeni popis čestih kanala, gradova i regija, tvoja imena i kanali spomenuti u porukama) i javlja obavijest jednom po kanalu, s gumbima **Dodaj** i **Ne obavještavaj više**. Isti kanali prikazani su na vrhu kartice Kanali, pa dodaješ samo one koje želiš.
- Postavke → Obavijesti: uključivanje i isključivanje tih obavijesti, vlastita imena kanala za praćenje i reset utišanih kanala.
- Postavke → O aplikaciji: link **Popis promjena** ispod verzije aplikacije otvara promjene te verzije.
- Dodavanje i brisanje kanala sada je trenutno (aplikacija više ne čita ponovno sva mjesta za kanale s nodea).
- Opisi ikona koje čita čitač ekrana sada su na odabranom jeziku.
- Ispravljeno: tip kontakta senzor prikazivao se kao „Sensor” na hrvatskom i srpskom.

## 1.0.9
- Susjedni repetitori: status signala za svaki repetitor – ocjena (odličan / dobar / slab / vrlo slab) uz SNR i RSSI, koliko dobro repetitor čuje tebe, udaljenost te prosječni, najniži i najviši SNR.
- Susjedni repetitori: razvrstavanje po zadnjem čutom, najjačem signalu ili najbližem.
- Susjedni repetitori koji još nisu u kontaktima mogu se dodati jednim dodirom (ili svi odjednom); aplikacija prvo od repetitora dohvati njegov puni naziv.
- Kratki kod (1 bajt) spaja se s repetitorom koji je već prepoznat po duljem kodu; ako i dalje odgovara više repetitora, dodir na upitnik objasni o kojima se radi, najbliži prvi.

## 1.0.8
- Novi ekran **Susjedni repetitori** u izborniku ⋮ (ispod Primljeni adverti): repetitori koje tvoj node čuje izravno, s punim imenima kad su poznata, SNR-om, RSSI-jem, vremenom kad su zadnji put čuti i brojem paketa koji su stigli preko njih. Gumb za osvježavanje pita repetitore u dometu da se jave.

## 1.0.7
- Tipka za slanje adverta: kratki pritisak šalje zero-hop advert, a dugi pritisak flood advert.
- Tailscale → Uređaji u tailnetu: dodirom na uređaj spajaš se na MeshCore node na njemu (prvo traži potvrdu; TCP port se može promijeniti, zadano 5000).

## 1.0.6
- Broj novih primljenih adverta prikazuje se samo uz "Primljeni adverti" u izborniku ⋮, a ne više na ikoni izbornika.

## 1.0.5
- Ispravljene obavijesti: servis za vezu u pozadini sad se uvijek pokreće, pa poruke i obavijesti stižu i nakon izlaska iz aplikacije.
- Razgovor ostavljen otvoren u pozadini sad javlja nove poruke i ostavlja ih nepročitanima dok se ne vratiš.
- Postavke → Obavijesti upozoravaju kad su obavijesti za aplikaciju isključene u Androidu, s prečacem za uključivanje.

## 1.0.4
- Gumb za slanje adverta koristi simbol ((•)), kao u originalnoj aplikaciji.
- Pretraga kontakata otvara se iz gornje trake (ikona povećala) umjesto stalnog polja za pretragu.
- Primljeni adverti premješteni su u izbornik ⋮, s brojačem novih nodeova.

## 1.0.3
- Obavijest o vezi umjesto Bluetooth adrese prikazuje bateriju nodea i, preko Bluetootha, jačinu signala (preko WiFi-ja: LAN ili Tailscale).
- Obavijest o vezi više ne dodaje brojač nepročitanih na ikonu aplikacije.

## 1.0.2
- Polje za pretragu izgleda kao gumbovi kategorija ispod njega (isti rub i zaobljenost, manja visina) i ima gumb za brisanje.

## 1.0.1
- **Otkrij regije u dometu** – pri odabiru scopea regije (zadanog ili za kanal) aplikacija pita repetitore u izravnom dometu koje regije poslužuju, a regiju odabireš jednim dodirom.

## 1.0.0 – prva stabilna verzija
- Ikone kanala kao u originalnoj MeshCore aplikaciji: ((•)) za Public, # za hashtag kanale, lokot za privatne kanale.

## 0.9.9
- Linkovi u porukama su podcrtani i otvaraju se u pregledniku.
- Postavke → Radio → **Veličina hasha putanje** (1, 2 ili 3 bajta po hopu, sprema se na node).
- U radio postavkama dostupno je **svih 48 regionalnih preseta**.
- TX snaga se više ne može postaviti ispod 1 dBm.
- Obavijesti prikazuju samo ikonu MeshCore Go.

## 0.9.8
- Ispravljena provjera ažuriranja.
- Postavke → O aplikaciji → **Licenca**: MIT licenca i korištene komponente otvorenog koda.

## 0.9.6
- **Ažuriranje kroz aplikaciju**: aplikacija jednom dnevno provjerava ima li nova verzija i nudi preuzimanje i instalaciju (može se isključiti).

## 0.9.5
- Kontakti čije ime završava emojijem ili zastavom dobivaju taj emoji kao ikonu.
- Dugi pritisak na kontakt → **Ikona kontakta**: automatski, 1 slovo, 2 slova ili bilo koji emoji.

## 0.9.1 – 0.9.4
- Svaka kategorija kontakata (Svi, Chat, Repetitori, Chat sobe, Senzori, Favoriti) može se sortirati: prvo favoriti, zadnja aktivnost, abeceda ili zadnje čuti. Redoslijed se mijenja dugim pritiskom na kategoriju i pamti se za svaku posebno.
- "Prvo favoriti" prikazuje favorite, a zatim ostale kontakte, abecedno.
- Bolja vidljivost prekidača u AMOLED temi.

## 0.9.0
- **Scope regije**: zadani scope spremljen na nodeu i zaseban scope za svaki kanal (zadani, bez scopea ili odabrana regija).
- **Postavke obavijesti**: privatne poruke, kanali, chat sobe, samo spominjanja, obavijest o prekidu veze, zvuk i vibracija.
- Obavijesti po kanalu: sve poruke, samo spominjanja ili utišano. Kontakti se mogu utišati. Svaka obavijest o poruci ima gumb **Utišaj**.
- Novi jezici: **srpski** i **njemački** (uz hrvatski i engleski).

## 0.8.7
- **AMOLED tema** s pozadinama kao u originalnoj MeshCore aplikaciji.

## 0.8.6
- Naredba `neighbors` na repetitoru prikazuje imena, vrijeme i SNR umjesto kodova ključeva.

## 0.8.5
- Kad je poruka stigla različitim rutama, karta prikazuje **sve rute odjednom u različitim bojama**, s legendom.

## 0.8.3 – 0.8.4
- **Putanja na karti** i za tvoje privatne poruke i tvoje poruke u kanalima.

## 0.8.2
- Uz svaku poslanu privatnu poruku piše kako je otišla: direktno ili floodom i koji je pokušaj.

## 0.8.1
- Dugi pritisak na kontakt: dodaj u favorite / ukloni iz favorita, preimenuj, obriši.

## 0.7.9 – 0.8.0
- Zbijeniji popisi (kontakti, kanali, postavke, primljeni adverti).

## 0.7.4 – 0.7.8
- Ekran **Primljeni adverti** (kao Discover u originalnoj aplikaciji): nodeovi koje je čuo tvoj node, filteri po vrsti, detalji, dodavanje jednim dodirom, uključivanje i isključivanje automatskog dodavanja.
- Kad je uključeno ručno dodavanje, novi adverti se više ne upisuju sami u kontakte.
- Brojač "Čulo repetitora" ispod tvojih poruka u kanalu.

## 0.7.1 – 0.7.3
- Gumb **Nepročitano**: pokazuje koliko razgovora ima nepročitane poruke i vodi ravno u najnoviji.
- Putanja poruke na karti crta se crvenom isprekidanom crtom sa strelicama smjera.
- Ispravke izgleda za Android 15 (nema praznog prostora iznad popisa).

## 0.7.0
- Broj repetitora koji su čuli tvoju poruku u kanalu, s popisom repetitora i njihovim SNR-om.
- Dugi pritisak na poruku: odgovori (@spominjanje), kopiraj, putanja na karti, pošalji ponovno, obriši.
- **Putanja poruke na karti**: repetitori kroz koje je poruka prošla.
- **Kontrola rute za DM**: automatski, uvijek flood ili ručna putanja preko odabranih repetitora.

## 0.6.0
- Opcija **Zapamti lozinku** za prijavu na repetitor i chat sobu (sprema se samo na telefonu).
- Obavijesti koriste ikonu aplikacije.

## 0.5.0
- Službeni simboli MeshCore nodeova na karti, obojeni prema tome koliko je davno node zadnji put čut.

## 0.4.0
- Nova ikona aplikacije.
- **Engleski** jezik (prebacivanje u Postavkama, uz hrvatski).
- Podaci o autoru u Postavke → O aplikaciji.

## 0.3.0
- **Automatski odabir veze**: kod kuće se aplikacija spaja izravno preko WiFi-ja, izvan kuće preko Tailscalea – ništa ne treba ručno prebacivati.
- Jednostavni, okrugli simboli nodeova na karti.

## 0.2.0
- Aplikacija se sad zove **MeshCore Go**.
- Spajanje na nodeove **preko lokalne mreže bez Tailscalea, preko Bluetootha LE i preko USB-a**.
- Zasebni simboli na karti za companion nodeove, repetitore, chat sobe i senzore.
- Podesiva **veličina fonta** i izbor fonta.
- **Stalni rad u pozadini**: zanemaruje štednju baterije, drži vezu s nodeom i **automatski se ponovno spaja** (svaka opcija se može uključiti ili isključiti).

## 0.1.0 – prva verzija
- Android MeshCore klijent s **ugrađenim Tailscaleom**: ne treba zasebna Tailscale aplikacija ni sistemski VPN. Prijava Tailscale auth ključem ili preko preglednika.
- Spajanje na WiFi companion node preko TCP-a, kroz tvoj tailnet.
- Kontakti, kanali i privatne poruke s potvrdom isporuke; chat sobe.
- Administracija repetitora: prijava, status, trace i CLI konzola.
- Karta nodeova.
- Raspored i tijek rada kao u originalnoj MeshCore aplikaciji (Kontakti, Kanali, Karta, Postavke), u vlastitom dizajnu.
