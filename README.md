# Simple-tasks-on-JAVA.-Task2
Напишите программу которая  проверяет введенное с клавиатуры число и говорит  * является ли данное число палиндромом.  * Палиндром - это число которое читается одинаково и спереди назад и сзади наперед.  * Примеры 12321, 45654, 787 и т.д.  *  * Дополнительное условие: программа принимает только числа длинной 5 знаков.  * В случае если было введено число длинной != 5, программа должна выполнить еще  * одно прохождение цикла и попросить снова ввести значение с клавиатуры.  * У данной задачи есть разные варианты решения.  * 1) С помощью конвертации чисел в строки 
Первый способ:

package controlstatement;

import java.util.Scanner;

public class task3 {
    public static void main(String[] args) {
        System.out.println("Введите число на проверку, максимальное количество символов пять: ");
        Scanner in = new Scanner(System.in);
        int t = 0;
        String str = " ";
        while (!(t < 99999 && t > 9999)) {
            t = in.nextInt();
            if (t < 99999 && t > 9999) {
                str = Integer.toString(t);
                if (str.charAt(0) == str.charAt(4) && str.charAt(1) == str.charAt(3)) {
                    System.out.println("Ваше число является полиандром! ");
                } else {
                    System.out.println("Ваше число не полиандр!");
                }}
                else{
                    System.out.println("Введите другое число из пяти символов: ");
                }
            }
        }
    }


Второй способ:

package controlstatement;

import java.util.Scanner;

public class task3b {
    public static void main(String[] args) {
        System.out.println("Введите число на проверку, максимальное количество символов пять: ");
        String str = " ";
        Scanner in = new Scanner(System.in);
        while (!(str.length() == 5)) {
            str = in.nextLine();
            if (str.length() == 5) {
                String reverse = new StringBuffer(str).reverse().toString();
                if (str.equals(reverse)) {
                    System.out.println("Ваше число является полиандром! ");
                } else {
                    System.out.println("Ваше число не полиандр!");
                }
            } else {
                System.out.println("Введите другое число из пяти символов: ");
            }
        }
    }
}
