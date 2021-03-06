**Тестирование приложения Money Transfer, которое позволяет пополнять баланс счёта с помощью перевода.**

В период с 11.06.2020 по 15.06.2020г. было проведено тестирование работы приложения, которое позволяет отображать баланс счёта клиента после перевода денежных средств. В итоге выявлено, что приложение работает некорретно. Вероятно, ошибка появляется в результате ввода больших сумм  перевода или баланса.

Описание тестирования:

Было проведено несколько видов тестов:

1. Функциональное тестирование - для того, чтобы понять, какие функции выполняет приложение.
2. Нефункциональное тестирование - для того, чтобы понять, насколько корректно приложение выполняет свою задачу (сложение) и выполняет ли вообще.

Также были проведены тесты эквивалентных значений: 
- в первую очередь было применено позитивное тестирование: согласно задаче были применены следующие суммы: 2 млрд как первоначальный баланс на счёте, 500млн. как сумма перевода. Итог: неверный подсчёт (вместо ожидаемой общей суммы на счёте в 2,5 млрд. приложение выдало сумму с минусом: -1794967297).
- второй этап позитивного тестирования включал ввод чисел, которые были меньше оговоренной суммы в задаче: к примеру, в поле баланса был введён 1 млн., 1 млрд, 1,5 млрд., перевода-100 тыс., 1 млрд, 1,5 млрд. Итог: приложение работает корректно, подсчёт итогой суммы верный. 
- затем было применено негативное тестирование: вместо цифр в число перевода и баланса счёта были добавлены буквы и символы. Итог: верная работа приложения, появилось сообщение об ошибке.
- при тестировании граничных значений, к примеру: сумма перевода была изменена с 500млн. на 1 млрд. при неизменном балансе счёта в 2 млрд. приложение сработало некорректно, сумма была высчитана неверно (Сумма = -1294967296).

**Результаты тестирования**
- 80% успешные тесты
- 20% неуспешные тесты

Ссылки на выявленные в результате тестирования дефекты:
- https://github.com/NatalyBolgova/Money_Transfer/issues/1
- https://github.com/NatalyBolgova/Money_Transfer/issues/2 

**Общие рекомендации**

В результате тестирования было выявлено, что проблема кроется в максимальной сумме, которая может храниться на счёте клиента. Вероятно, нужно увеличить значение переменной итоговой суммы по счёту.




