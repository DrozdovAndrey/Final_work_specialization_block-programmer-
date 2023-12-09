# Итоговая контрольная работа по блоку специализация


**Информация о проекте**

* Необходимо организовать систему учета для питомника в котором живут домашние и вьючные животные.

1.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
cat > "Домашние животные"
Собаки
Кошки
Хомяки

'Ctrl+d'
```

```bash
cat > "Вьючные животные"
Лошади
Верблюды
Ослы

'Ctrl+d'
```

```bash
cat "Домашние животные" "Вьючные животные" > Animals
cat Animals
mv "Animals" "Друзья человека"
```

</details>

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/1_2.png)

2.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
mkdir folder_for_attestation
mv 'Друзья человека' folder_for_attestation/
ls
cd folder_for_attestation/
ls
```

</details>

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/2.png)

3.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
sudo apt-get update
sudo apt update
sudo apt install mysql-server
sudo service mysql status
```

</details>

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/3_1.png)
![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/3_2.png)
![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/3_3.png)
![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/3_4.png)

4.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
wget http://ftp.us.debian.org/debian/pool/main/s/sl/sl_5.02-1_amd64.deb
sudo dpkg -i sl_5.02-1_amd64.deb
sudo dpkg -r sl
```

</details>

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/4_2.png)

5.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
  730  mkdir attestation

  731  cd attestation/

  732  cat > Домашние животные

  733  cat > "Домашние животные"

  734  cat > "Вьючные животные"

  735  cat "Домашние животные" "Вьючные животные" > Animals 

  736  cat Animals

  737  mv "Animals" "Друзья человека"

  738  clear

  739  mkdir folder_for_attestation && mv "Друзья человека" /attestation/folder_for_attestation 

  740  ls

  741  rmdir folder_for_attestation/

  742  ls

  743  clear

  744  mkdir folder_for_attestation

  745  mv "Друзья человека" /attestation/folder_for_attestation

  746  mv "Друзья человека" attestation/folder_for_attestation

  747  ls

  748  mkdir folder_for_attestation

  749  rmdir folder_for_attestation

  750  clear

  751  mkdir folder_for_attestation

  752  mv 'Друзья человека' attestation/folder_for_attestation/

  753  mv 'Друзья человека' folder_for_attestation/

  754  ls

  755  cd folder_for_attestation/

  756  ls

  757  clear

  758  cd..

  759  cd.

  760  cd..

  761  cd 

  762  cd attestation/

  763  clear

  764  sudo apt-get update

  765  sudo apt update

  766  sudo apt install mysql

  767  sudo apt install mysql-server

  768  sudo service mysql status

  769  clear

  770  wget http://ftp.us.debian.org/debian/pool/main/s/sl/sl_5.02-1_amd64.deb

  771  sudo dpkg -i sl_5.02-1_amd64.deb

  772  sudo dpkg -r sl

  773  clear

  774  history

```

</details>

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/5.png)

6.

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/diagram.png)

7.

```sql
CREATE DATABASE Друзья_человека;
```

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/7.png)

8.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
CREATE TABLE Родительский_класс (
  id INT PRIMARY KEY AUTO_INCREMENT,
  тип VARCHAR(50)
);


CREATE TABLE Домашние_животные (
  id INT PRIMARY KEY,
  вид VARCHAR(50),
  FOREIGN KEY (id) REFERENCES Родительский_класс(id)
);


CREATE TABLE Собаки (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


CREATE TABLE Кошки (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


CREATE TABLE Хомяки (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


CREATE TABLE Вьючные_животные (
  id INT PRIMARY KEY,
  вид VARCHAR(50),
  FOREIGN KEY (id) REFERENCES Родительский_класс(id)
);


CREATE TABLE Лошади (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);


CREATE TABLE Верблюды (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);


CREATE TABLE Ослы (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);

show databases;
show tables;
```

</details>

![pictures for project](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/blob/main/Source/8.png)


9.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
INSERT INTO Верблюды ( имя, команда, дата_рождения)
VALUES ('Зефир', 'Но, пошел', '2019-09-01'),
       ('Багдад', 'На месте' '2020-11-12'),
       ('Скорость', 'Ждать' '2021-04-05');

INSERT INTO Кошки ( имя, команда, дата_рождения)
VALUES ('Маркиз', 'Кис-кис', '2021-01-20'),
       ('Снежка', 'Давай играть', '2022-03-08');

INSERT INTO Лошади ( имя, команда, дата_рождения)
VALUES ('Спирит', 'Но', '2020-01-21'),
       ('Воронок', 'Бррррр', '2022-03-08');

INSERT INTO Ослы ( имя, команда, дата_рождения)
VALUES ('Нарик', 'Пошёл', '2019-01-21'),
       ('Степан', 'Стой', '2021-03-08');

INSERT INTO Собаки ( имя, команда, дата_рождения)
VALUES ('Шарик', 'Дай лапу', '2019-01-21'),
       ('Бим', 'Лежать', '2020-03-08');

INSERT INTO Хомяки ( имя, команда, дата_рождения)
VALUES ('Долгожитель', 'Кушать', '2022-01-21'),
       ('Хома', 'Отойди', '2023-03-08');
```

</details>

10.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
TRUNCATE TABLE Верблюды;
```

```sql
CREATE TABLE Парнокопытные AS
SELECT * FROM Лошади
UNION
SELECT * FROM Ослы;
```

</details>

11.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
CREATE TABLE Парнокопытные AS
SELECT *, TIMESTAMPDIFF(MONTH, дата_рождения, CURDATE()) AS возраст_в_месяцах
FROM (
    SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки
    UNION ALL
    SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки
    UNION ALL
    SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки
    UNION ALL
    SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади
    UNION ALL
    SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы
) AS животные
WHERE дата_рождения >= DATE_SUB(CURDATE(), INTERVAL 3 YEAR)
AND дата_рождения <= DATE_SUB(CURDATE(), INTERVAL 1 YEAR);

```

</details>

12.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
CREATE TABLE Полный_состав AS
SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки
UNION ALL
SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки
UNION ALL
SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки
UNION ALL
SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади
UNION ALL
SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы;

```

</details>

13. , 14. , 15. - [-= Перейти к коду Java =-](https://github.com/DrozdovAndrey/Final_work_specialization_block-programmer-/tree/main/Java)


*Подготовил студент Geek Brains* **`Дроздов Андрей`**
