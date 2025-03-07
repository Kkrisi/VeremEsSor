package hu.szamalk;

import modell.Sor;
import modell.Verem;



public class Main {
    public static void main(String[] args) {
        Verem ver = new Verem();
        ver.noveles();

        Sor sor = new Sor();
        sor.elsoKettoCsere();
    }


}












package modell;
import java.util.Stack;
import java.util.Random;



public class Verem {
    Stack<Integer> verem = new Stack<>();
    private int binarisSzam;

    public Verem() {
        veremFeltolt();
        kiiras();
    }

    public void veremFeltolt(){
        verem.clear();
        Random rand = new Random();
        for (int i = 0; i < 8; i++) {
            verem.push(rand.nextInt(2));
        }
    }

    public void kiiras(){
        System.out.println("Verem tartalma: " + verem);

    }






    public void noveles() {

        for (int i = 0; i < 8; i++) {
            while (verem.size() != (8-i)) {
                verem.pop();
            }
            //System.out.println("verem kezdete :"+verem);

            int felsoElem = verem.peek();
            if (felsoElem == 0) {
                int lekertElem1 = verem.pop();
                verem.push(1);
                //System.out.println(i + "verem tartalma1:" + verem);
            } else {
                int lekertElem2 = verem.pop();
                //System.out.println(i + "verem tartalma2:" + verem);
            }


            while (verem.size() < 8) {
                verem.push(1);
            }
            System.out.println("verem vége    :"+verem);
            }
        }


    }























    package modell;
import java.util.LinkedList;
import java.util.Queue;
import java.util.Random;


public class Sor {
    Queue<Integer> sor = new LinkedList<>();

    public Sor() {
        sorFeltolt();
        kiiras();
    }

    public void sorFeltolt(){
        sor.clear();
        Random rand = new Random();
        for (int i = 1; i < 5; i++) {
            sor.add(i);
        }
    }

    public void kiiras(){
        System.out.println("Sor tartalma: " + sor);
    }






    public void elsoKettoCsere() {


        System.out.println("Sor tartalma: " + sor);
    }
}
