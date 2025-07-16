# M-dulo-Estruturas-de-Controle-em-Java---NTT-DATA
Módulo: Estruturas de Controle em Java - NTT DATA

# Módulo: Estruturas de Controle em Java - NTT DATA

Módulo: Estruturas de Controle em Java — NTT DATA (2 horas)
Este módulo fundamental apresenta os principais conceitos de estruturas de controle da linguagem Java. Durante o curso, você aprende a trabalhar com estruturas condicionais (if, else, switch) e estruturas de repetição (for, while, do-while). Além disso, são realizados diversos exercícios práticos que fixam o aprendizado e estimulam a resolução de problemas comuns no desenvolvimento de software. O uso de recursos modernos do Java, como switch expressions (Java 14+), é apresentado para melhorar a legibilidade e eficiência do código.

Ferramentas: Java JDK, IntelliJ IDEA (ambiente de desenvolvimento)
Duração: 2 horas
Competências: lógica de programação, controle de fluxo, manipulação de loops e condições, prática em IDE profissional

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-000000?style=for-the-badge&logo=intellij-idea&logoColor=white)

Este repositório contém exercícios práticos e exemplos do módulo "Estruturas de Controle em Java" do bootcamp da NTT DATA, com duração de 2 horas.  

Durante este módulo, são exploradas as principais estruturas de controle da linguagem Java, tais como:

- Condicionais: `if`, `else if`, `else` e `switch` (incluindo expressões modernas do Java 14+)
- Estruturas de repetição: `for`, `while` e `do-while`


- Exercícios focados em tabuada, cálculo de IMC, seleção de números pares/ímpares, e divisibilidade

O código está organizado para facilitar a compreensão e prática. Ideal para quem está iniciando no desenvolvimento Java e deseja fortalecer a lógica de programação.

---

**Ferramentas usadas:**  
- Java JDK  
- IntelliJ IDEA  

Sinta-se à vontade para explorar e praticar!

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Exercício 1: Tabuada de 1 a 10
        System.out.println("Exercício 1: Tabuada");
        System.out.println("Digite um número para ver a tabuada de 1 até 10:");
        int number = scanner.nextInt();
        for (int i = 1; i <= 10; i++) {
            System.out.printf("%d x %d = %d%n", number, i, number * i);
        }
        System.out.println("\n======================================");

        // Exercício 2: Cálculo do IMC
        System.out.println("Exercício 2: Cálculo do IMC");
        System.out.println("Informe a altura (em metros):");
        double altura = scanner.nextDouble();
        System.out.println("Digite seu peso (em kg):");
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
        System.out.println("\n======================================");

        // Exercício 3: Números pares ou ímpares em ordem decrescente
        System.out.println("Exercício 3: Números pares ou ímpares");
        System.out.println("Digite o primeiro número:");
        int primeiro = scanner.nextInt();
        System.out.println("Digite o segundo número (maior que o primeiro):");
        int segundo = scanner.nextInt();
        System.out.println("Deseja ver os números pares ou ímpares? (par/impar)");
        String escolha = scanner.next();

        System.out.println("Números " + escolha + " entre " + segundo + " e " + primeiro + " (decrescente):");
        for (int i = segundo; i >= primeiro; i--) {
            if (escolha.equalsIgnoreCase("par") && i % 2 == 0) {
                System.out.println(i);
            } else if (escolha.equalsIgnoreCase("impar") && i % 2 != 0) {
                System.out.println(i);
            }
        }
        System.out.println("\n======================================");

        // Exercício 4: Números divisíveis pelo primeiro número
        System.out.println("Exercício 4: Divisibilidade");
        System.out.println("Informe um número base:");
        int baseNumber = scanner.nextInt();

        while (true) {
            System.out.println("Informe um número para verificação:");
            int toVerify = scanner.nextInt();

            if (toVerify < baseNumber) {
                System.out.printf("Informe um número maior que %d\n", baseNumber);
                continue;
            }

            int resto = toVerify % baseNumber;
            System.out.printf("%d %% %d = %d\n", toVerify, baseNumber, resto);

            if (resto != 0) {
                break;
            }
        }
        System.out.println("\nFim dos exercícios.");
        scanner.close();
    }
}
