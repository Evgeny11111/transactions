# Часть 1: синхронизация на уровне приложения

## Описание

Вам предоставлен класс AppSynchronizedAccounts, который содержит метод перевода денежных средств между банковскими
счетами.
Необходимо обеспечить корректную работу данного метода в многопоточной среде с помощью механизмов синхронизации.

## Мотивация

Добавление методов синхронизации позволит корректно обрабатывать параллельные переводы денежных средств из нескольких
потоков, что является крайне важным при выполнении приложения в многопоточных среде. Без синхронизации разные потоки
могут одновременно обращаться к общим ресурсам (балансам аккаунтов), и это может приводить к непредсказуемым
результатам, например, к race condition или к data race.

## Задача

Необходимо дополнить класс AppSynchronizedAccounts методами синхронизации для обеспечения корректной работы в
многопоточной среде. Также необходимо учесть возможность возникновения взаимной блокировки потоков и избегать
использование глобальных lock'ов, которое может привести выполнение приложения фактически к однопоточному режиму.

Вы можете протестировать свое решение с помощью класса AppSynchronizedAccountsTest.

## Ресурсы

- [Deadlock](https://ru.wikipedia.org/wiki/%D0%92%D0%B7%D0%B0%D0%B8%D0%BC%D0%BD%D0%B0%D1%8F_%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D0%BE%D0%B2%D0%BA%D0%B0)
- Книга [Java Concurrency in Practice](https://leon-wtf.github.io/doc/java-concurrency-in-practice.pdf) глава 10.
  Avoiding Liveness Hazards.

## Успехов в решении задания!
