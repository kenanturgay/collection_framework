# collection_framework



        package com.workintech.collections;

        import java.text.CollationElementIterator;
        import java.util.*;

        public class Main {
        public static void main(String[] args) {


        // Arrayler sabit boyutları vardır.

        //  String[] names = new String[100] bu bize dezavantaj sağlıyor. Hafıza zararlı ve ihtiyaca göre esneyemez.
        // Diziler homojen data tutarlar.

        //sort, search gibi işlemler develpoer kontrolündedir. Bunlar yapmamıza gerek yok çünkü computer sciencelar bunu yapıyor.Veri yapıları destekleyen metod eksikliği denir.


        System.out.println("Hello world!");

        Object[] names = new Object[5];

        names[0] = "Kenan";
        names[1]=5;
        names[2]= new Student(1, "Kenan");

        System.out.println(Arrays.toString(names));


        //Wrapper Classlar
        int age =29;
        double salary=2000;
        boolean isValid=false;

        //Integer, Double, Boolean primitive tipler içine Wrapper classlar
        int x = Integer.parseInt("5");
        int y = new Integer(5);

        if(x==y){
            System.out.println("Eşit");
        }else{
            System.out.println("Eşit değil");
        }

        //eşittir çünkü wrapper classların autoBoxing özeliğinden dolayı. Ayrı ayrı memory de yer tutmaz

        // Java Collections Framework(Java veri yapıları)
        //Multitip data tutmaya collection denir.
        // Framework? => React bir librarydir. Boilerplate kodları azaltrı

        System.out.println("*************************************************");
        //Listler
        List<String> fruit = new ArrayList<>();// Polymorphism özelliği sayesinde böyle yazabiliyor.

        //Listeleirn sabit boyutları yoktur.
        //Listeler eklendiği sırada çalışırlar.(Insertion ordering)
        //Listeler uniqeu data tutmazlar. Yani aynı elemanı 2 defa ekleyebilirz.



        fruit.add("ELMA");
        fruit.add("hıyar");
        fruit.add("Çilek");
        fruit.add("ELMA");

        System.out.println(fruit);

        System.out.println(fruit.get(1));
        fruit.set(1,"Kivi");

        System.out.println(fruit.get(1));


        System.out.println("************************");
        //Listleri gezme

        //  for veya foreach ile yapavbiliriz.

        for (String f : fruit){
            System.out.println(f);
        }


        System.out.println("******************************");

        for(int i = 0; i<fruit.size(); i++){
            System.out.println(fruit.get(i));
        }

        System.out.println("***********************************");


        //Heterojen data tutarlar

        List first = new ArrayList<>();

        first.add("sadsa");
        first.add(2);
        first.add(true);
        first.add(new Student(1,"Kenan"));

        System.out.println(first);

        // List<int> şekilinde yazamayız. Primitive olarak yazamayız.


        System.out.println("------------------------------------------------");



        //Iterator pattern

        List<String> vegatables = new ArrayList<>();
        vegatables.add("hıyar");
        vegatables.add("biber");
        vegatables.add("pivaz");

        System.out.println(vegatables.contains("biber"));

        Iterator iter = vegatables.iterator();
        while(iter.hasNext())
        {
            System.out.println(iter.next());
        }


        // Collections classlarda faydalı metodlar var. => Collections.sort() = > put the elements in order, Collectipons

        Collections.sort(vegatables);


        System.out.println(vegatables);


        Collections.reverse(vegatables);

        System.out.println(vegatables);


        //addAll()

        //LINKEDLIST

        // Linkedlerin özelikleri Listelrin özellikleri ile aynı

        //Avantajaları => sona ve ortaya eleman ekleme veya silme linkedlist hızlı ama Okuma için arrayList daha hızlı

        List<String> c1 = new LinkedList<>();

        c1.add("Fırat");
        c1.add("sss");
        c1.add("hrrr");

















    }
}
