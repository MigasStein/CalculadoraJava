# Calculadora Java
Segue o script da calculadora em Java

import java.util.Scanner;

public class calculadora {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner teclado = new Scanner(System.in);

		System.out.print("Digite o primeiro numero: ");
		double priNumero = teclado.nextDouble();

		System.out.print("Digite o operador (+, -, *, /): ");
		char op = teclado.next().charAt(0);

		System.out.print("Digite o segundo número: ");
		double segNumero = teclado.nextDouble();

		double resultado;

		switch (op) {
		case '+':
			resultado = priNumero + segNumero;
			break;
		case '-':
			resultado = priNumero - segNumero;
			break;
		case '*':
			resultado = priNumero * segNumero;
			break;
		case '/':
			if (segNumero == 0) {
				System.out.println("Erro: divisão por zero!");
				return;
			}
			resultado = priNumero / segNumero;
			break;
		default:
			System.out.println("Operador inválido!");
			return;
		}

		System.out.println("Resultado: " + resultado);
		teclado.close();

	}

}
