# Módulo Estruturas de Controle em Java - NTT DATA

![Java](https://img.shields.io/badge/Java-%23007396?style=for-the-badge&logo=java&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-%2368159D?style=for-the-badge&logo=intellij-idea&logoColor=white)
![NTT DATA](https://img.shields.io/badge/NTT%20DATA-%230078B8?style=for-the-badge&logo=building&logoColor=white)
![DIO.me](https://img.shields.io/badge/DIO.me-%23F26C4F?style=for-the-badge&logo=graduation-cap&logoColor=white)


## Sobre o Módulo

Este repositório contém os exercícios práticos do módulo **Estruturas de Controle em Java** do bootcamp da **NTT DATA**, com duração de 2 horas.  

Durante o módulo, foram abordados os principais conceitos de estruturas de controle em Java, como:  
- Estruturas condicionais (`if`, `else if`, `else`, `switch`)  
- Estruturas de repetição (`for`, `while`, `do-while`)  
- Uso de recursos modernos do Java, incluindo `switch` com expressão lambda (Java 14+)  

O módulo é ideal para quem está começando no desenvolvimento em Java e quer consolidar os conceitos de lógica e controle de fluxo.

## Tecnologias utilizadas  
- Java JDK  
- IntelliJ IDEA  

## Conteúdo do repositório

- Exercícios para praticar tabuada, cálculo de IMC, seleção de números pares/ímpares em intervalos, e verificação de divisibilidade.  
- Códigos organizados para fácil leitura e execução.

---

## Código Java com os 4 exercícios juntos

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Exercício 1: Tabuada de 1 até 10
        System.out.println("Exercício 1: Tabuada");
        System.out.print("Digite um número: ");
        int number = scanner.nextInt();
        for (int i = 1; i <= 10; i++) {
            System.out.printf("%d x %d = %d%n", number, i, number * i);
        }
        System.out.println("\n==============================\n");

        // Exercício 2: Cálculo do IMC
        System.out.println("Exercício 2: Cálculo do IMC");
        System.out.print("Informe a altura (em metros): ");
        double altura = scanner.nextDouble();
        System.out.print("Digite seu peso (em kg): ");
        double peso = scanner.nextDouble();
        double imc = peso / (altura * altura);

        if (imc <= 18.5) {
            System.out.println("Abaixo do peso");
        } else if (imc <= 24.9) {
            System.out.println("Peso ideal");
        } else if (imc <= 29.9) {
            System.out.println("Levemente acima do peso");
        } else if (imc <= 34.9) {
            System.out.println("Obesidade Grau I");
        } else if (imc <= 39.9) {
            System.out.println("Obesidade Grau II (Severa)");
        } else {
            System.out.println("Obesidade III (Mórbida)");
        }
        System.out.println("\n==============================\n");

        // Exercício 3: Números pares ou ímpares entre dois números, ordem decrescente
        System.out.println("Exercício 3: Números pares ou ímpares");
        System.out.print("Digite o primeiro número: ");
        int primeiro = scanner.nextInt();
        System.out.print("Digite o segundo número (maior que o primeiro): ");
        int segundo = scanner.nextInt();
        System.out.print("Deseja ver números pares ou ímpares? (par/impar): ");
        String escolha = scanner.next();

        System.out.printf("Números %s entre %d e %d (decrescente):%n", escolha, segundo, primeiro);
        for (int i = segundo; i >= primeiro; i--) {
            if (escolha.equalsIgnoreCase("par") && i % 2 == 0) {
                System.out.println(i);
            } else if (escolha.equalsIgnoreCase("impar") && i % 2 != 0) {
                System.out.println(i);
            }
        }
        System.out.println("\n==============================\n");

        // Exercício 4: Números divisíveis pelo primeiro número até encontrar resto diferente de 0
        System.out.println("Exercício 4: Divisibilidade");
        System.out.print("Informe um número base: ");
        int baseNumber = scanner.nextInt();

        while (true) {
            System.out.print("Informe um número para verificação: ");
            int toVerify = scanner.nextInt();

            if (toVerify < baseNumber) {
                System.out.printf("Informe um número maior que %d%n", baseNumber);
                continue;
            }

            int resto = toVerify % baseNumber;
            System.out.printf("%d %% %d = %d%n", toVerify, baseNumber, resto);

            if (resto != 0) {
                break;
            }
        }
        System.out.println("\nFim dos exercícios.");
        scanner.close();
    }
}
