import java.util.Scanner;


public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] numeros = new int[10];


        System.out.println("Digite 10 valores inteiros:");
        for (int i = 0; i < 10; i++) {
            numeros[i] = scanner.nextInt();
        }

        boolean ordemVetor = true;
        for (int i = 0; i < 9; i++) {
            if (numeros[i] > numeros[i + 1]) {
                ordemVetor = false;
                break;
            }
        }
        System.out.println("O vetor está " + (ordemVetor ? "ordenado." : "não está ordenado."));


        boolean continuar = true;
        while (continuar) {
            System.out.print("Digite o elemento a ser encontrado: ");
            int elemento = scanner.nextInt();
            int posicao = -1;

            for (int i = 0; i < 10; i++) {
                if (numeros[i] == elemento) {
                    posicao = i;
                    break;
                }
            }

            if (posicao != -1) {
                System.out.println("Elemento encontrado na posição: " + posicao);
            } else {
                System.out.println("Elemento não encontrado.");
            }

            System.out.print("Deseja continuar a busca?  ");

        }

        scanner.close();
    }
}
