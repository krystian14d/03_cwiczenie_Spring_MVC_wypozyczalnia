3rd exercise from Javastart.pl "Spring exercises" package 

Main focus on Spring MVC.

PROBLEMY:
klasa ItemService:
 - metoda findItemById - linijka 21
   - itemRepository zwraca mi optional, chciałbym to później zmapować na obiekt ItemDto, jak poprawić ten zapis? 
   - Zastosowałem metodę .get() na obiekcie zwróconym z itemrepository, ale jeśli itemrepo zwróci mi null to będę mieć błąd... a ten null jest obsługiwany później w klasie ItemController. Jak to poprawić?

Lombok i konstruktory:
 - klasa ItemDtoMapper:
   - jak mapuję ItemDto -> Item, to nie podaję wtedy ID, bo ID jest generowane samo przez bazę danych
   - jak mapuję Item -> ItemDto, to wtedy mapuję też ID bo jest pobierane z bazy danych 
 - Jak w takim razie odpowiednio napisać mapper, i przede wszystkim klasę ItemDto (analogicznie klasa OrderDto)? 
 - Jak w klasach DTO dam adnotacje @AllArgsConstructor i @ReqArgsConstructor i oznaczę pola wymagane słowem final, to jeśli chcę stworzyć obiekt z wszystkimi polami to mi wyrzuca błąd...

Dodanie klas DTO dla Order - jak do tego najlepiej podejść?
Dodałem klasę OrderService, która komunikuje się z orderRepository. Natomiast orderService z orderController powinno komunikować się za pomocą typu OrderDto.
W klasie OrderDto - pole List<Item> items nie powinno wyglądać tak: List<ItemDto> items?
Jeśli tak, to jak je zmapować w klasie OrderDtoMapper?

