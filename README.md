import java.util.Scanner;

public class VerificarTriangulo {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Solicita os lados do triângulo
        System.out.print("Digite o tamanho do lado 1: ");
        double lado1 = input.nextDouble();

        System.out.print("Digite o tamanho do lado 2: ");
        double lado2 = input.nextDouble();

        System.out.print("Digite o tamanho do lado 3: ");
        double lado3 = input.nextDouble();

        if (eTriangulo(lado1, lado2, lado3)) {
            if (lado1 == lado2 && lado2 == lado3) {
                System.out.println("É um triângulo equilátero.");
            } else if (lado1 == lado2 || lado2 == lado3 || lado1 == lado3) {
                System.out.println("É um triângulo isósceles.");
            } else {
                System.out.println("É um triângulo escaleno.");
            }
        } else {
            System.out.println("Não é possível formar um triângulo com esses lados.");
        }
    }

    public static boolean eTriangulo(double lado1, double lado2, double lado3) {
        return lado1 + lado2 > lado3 && lado1 + lado3 > lado2 && lado2 + lado3 > lado1;
    }
}
