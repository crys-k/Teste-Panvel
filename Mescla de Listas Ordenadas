import java.util.*;

public class MesclarListasOrdenadas {
    public static void main(String[] args) {
        List<Integer> l1 = Arrays.asList(1, 2, 4);
        List<Integer> l2 = Arrays.asList(1, 3, 4);

        List<Integer> resultado = mesclarListas(l1, l2);
        System.out.println("Saída: " + resultado);
    }

    public static List<Integer> mesclarListas(List<Integer> l1, List<Integer> l2) {
        List<Integer> resultado = new ArrayList<>();
        int i = 0, j = 0;

        while (i < l1.size() && j < l2.size()) {
            if (l1.get(i) <= l2.get(j)) {
                resultado.add(l1.get(i++));
            } else {
                resultado.add(l2.get(j++));
            }
        }

        adicionarRestantes(resultado, l1, i);
        adicionarRestantes(resultado, l2, j);

        return resultado;
    }

    private static void adicionarRestantes(List<Integer> resultado, List<Integer> lista, int indice) {
        while (indice < lista.size()) {
            resultado.add(lista.get(indice++));
        }
    }
}
