# hhtpContent
public class JvmComprehension {

    public static void main(String[] args) {
        int i = 1;                      // Создается переменная i типа int со значением 1
        Object o = new Object();        // Создается новый объект типа Object в области памяти Heap, и ему присваивается ссылка o
        Integer ii = 2;                 // Создается новый объект типа Integer со значением 2 в области памяти Heap, и ему присваивается ссылка ii
        printAll(o, i, ii);             // Вызывается метод printAll(o, i, ii) в текущем фрейме стека. Виртуальная машина сохраняет в стеке новый фрейм для метода printAll.
        System.out.println("finished"); // Метод printAll завершается. Виртуальная машина удаляет фрейм printAll из стека и возвращает управление методу main. Вызывается метод println() и выводится на консоль строка "finished".
                                            Метод main завершается. Виртуальная машина удаляет фрейм main из стека, и программа завершает свою работу.
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // Создается новая переменная uselessVar типа Integer со значением 700 в области памяти Heap.
        System.out.println(o.toString() + i + ii);  // Вызывается метод toString() для объекта o и происходит конкатенация результатов методов toString() и значений переменных i и ii. Результат выводится на консоль.
    }
}
