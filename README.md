# Módulo: Estruturas de Controle em Java - NTT DATA

Módulo: Estruturas de Controle em Java — NTT DATA (2 horas)  
Este módulo fundamental apresenta os principais conceitos de estruturas de controle da linguagem Java. Durante o curso, você aprende a trabalhar com estruturas condicionais (if, else, switch) e estruturas de repetição (for, while, do-while). Além disso, são realizados diversos exercícios práticos que fixam o aprendizado e estimulam a resolução de problemas comuns no desenvolvimento de software. O uso de recursos modernos do Java, como switch expressions (Java 14+), é apresentado para melhorar a legibilidade e eficiência do código.

Ferramentas: Java JDK, IntelliJ IDEA (ambiente de desenvolvimento)  
Duração: 2 horas  
Competências: lógica de programação, controle de fluxo, manipulação de loops e condições, prática em IDE profissional

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)  
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-000000?style=for-the-badge&logo=intellij-idea&logoColor=white)

---

Este repositório contém exercícios práticos e exemplos do módulo "Estruturas de Controle em Java" do bootcamp da NTT DATA, com duração de 2 horas.

Durante este módulo, são exploradas as principais estruturas de controle da linguagem Java, tais como:

- Condicionais: `if`, `else if`, `else` e `switch` (incluindo expressões modernas do Java 14+)  
- Estruturas de repetição: `for`, `while` e `do-while`

Exercícios focados em tabuada, cálculo de IMC, seleção de números pares/ímpares, e divisibilidade.

O código está organizado para facilitar a compreensão e prática. Ideal para quem está iniciando no desenvolvimento Java e deseja fortalecer a lógica de programação.

---

## Exercício 1: Tabuada de 1 a 10

```java
import java.util.Scanner;

public class Tabuada {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite um número para ver a tabuada de 1 até 10:");
        int number = scanner.nextInt();

        for (int i = 1; i <= 10; i++) {
            System.out.printf("%d x %d = %d%n", number, i, number * i);
        }

        scanner.close();
    }
}
