# Crew

## Feladat leírása

Írj egy `Person` osztályt, amelyben az alábbi adattagok vannak: `String name`, `int age`, `int height`.

Legyen továbbá egy `Crew` interface, amely az alábbi metódusokat deklarálja:

    public void addFriend(Person friend);
    public Person getTallestFriend();
    public Person getShortestFriend();
    public Person getYoungestFriend();
    public Person getOldestFriend();

A `MeetUp` osztály implementálja a `Crew` interface-t.

A `MeetUpTest` osztályban vedd fel az alábbi adattagokat:

    private MeetUp sut;

    private Person johnSilver = new Person("Long John Silver", 47, 192);
    private Person captainSmollet = new Person("Captain Smollet", 39, 184);
    private Person benGunn = new Person("Ben Gunn Dog", 52, 172);
    private Person jim = new Person("Jim Hawkins", 14, 168);
    private Person doctorLivesey = new Person("Doctor Livesey", 35, 178);

Illetve az alábbi test metódusokat:

    @Test
    public void testLegfiatalabb() {
        assertEquals(jim, sut.getYoungestFriend());
    }

    @Test
    public void testLegoregebb() {
        assertEquals(benGunn, sut.getOldestFriend());
    }

    @Test
    public void testLegkisebb() {
        assertEquals(jim, sut.getShortestFriend());
    }

    @Test
    public void testLegmagasabb() {
        assertEquals(johnSilver, sut.getTallestFriend());
    }

Írd meg a `MeetUp` osztály hiányzó kódját úgy, hogy a fent definiált teszt metódusok mindegyike sikeresen lefusson. Lehetőleg használd azt a tudást, amit az elméleti órán szereztél a kollekciók sorbarendezésével kapcsolatban.
