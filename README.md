# containers04

# Lucrare de laborator Nr4: Utilizarea containerelor ca medii de execuție

# Scopul 
Scopul acestei lucrări de laborator este familiarizarea cu Docker și utilizarea containerelor ca medii de execuție pentru a configura un server web Apache pe o imagine de Ubuntu.

# Sarcina
Sarcina principală a fost crearea unui container bazat pe Ubuntu care să includă un server web Apache și să găzduiască o pagină web simplă cu mesajul „Hello, World!”.

# Descrierea executării lucrării de laborator
1. Deschiți terminalul în directorul containers04 și executați comanda:

docker run -ti -p 8000:80 --name containers04 ubuntu bash

2. In fereastra deschisa, executați următoarele comenzi și explicați-le:

apt update
apt install apache2 -y
service apache2 start

3. Deschideți browserul și introduceți în bara de adrese http://localhost:8000. Ce vedeți?

4. Executați următoarele comenzi:

ls -l /var/www/html/
echo '<h1>Hello, World!</h1>' > /var/www/html/index.html
Reîmprospătați pagina în browser. Ce vedeți? - Hello, World!

5. Executați următoarele comenzi:
cd /etc/apache2/sites-enabled/
cat 000-default.conf
Ce vedeți pe ecran?

6. Inchideți fereastra terminalului cu comanda exit.

7. Afisați lista de containere:
docker ps -a

8. Stergeți containerul:
docker rm containers04

# Concluzie
Această lucrare m-a ajutat să înțeleg cum să folosesc Docker pentru a crea și gestiona containere. De asemenea, am învățat cum să instalez și să configurez un server web Apache într-un container și cum să creez o pagină web simplă. Docker oferă un mediu eficient pentru testarea și dezvoltarea aplicațiilor în containere izolate.
