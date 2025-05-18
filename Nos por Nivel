import java.util.*;

public class ArvorePorNivel {
    public static void main(String[] args) {
        NoArvore raiz = criarArvoreExemplo();
        List<List<Integer>> niveis = percorrerPorNivel(raiz);
        System.out.println("Saída: " + niveis);
    }

    static class NoArvore {
        int valor;
        NoArvore esquerda, direita;

        NoArvore(int valor) {
            this.valor = valor;
        }
    }

    public static List<List<Integer>> percorrerPorNivel(NoArvore raiz) {
        List<List<Integer>> resultado = new ArrayList<>();

        if (raiz == null) return resultado;

        Queue<NoArvore> fila = new LinkedList<>();
        fila.offer(raiz);

        while (!fila.isEmpty()) {
            int tamanhoNivel = fila.size();
            List<Integer> nivelAtual = new ArrayList<>();

            for (int i = 0; i < tamanhoNivel; i++) {
                NoArvore atual = fila.poll();
                nivelAtual.add(atual.valor);

                if (atual.esquerda != null) fila.offer(atual.esquerda);
                if (atual.direita != null) fila.offer(atual.direita);
            }

            resultado.add(nivelAtual);
        }

        return resultado;
    }

    private static NoArvore criarArvoreExemplo() {
        NoArvore raiz = new NoArvore(3);
        raiz.esquerda = new NoArvore(9);
        raiz.direita = new NoArvore(20);
        raiz.direita.esquerda = new NoArvore(15);
        raiz.direita.direita = new NoArvore(7);
        return raiz;
    }
}
