# containers04

# Lucrare de laborator Nr4: Utilizarea containerelor ca medii de execuție

# Scopul 
Scopul acestei lucrări de laborator este familiarizarea cu Docker și utilizarea containerelor ca medii de execuție pentru a configura un server web Apache pe o imagine de Ubuntu.

# Sarcina
Sarcina principală a fost crearea unui container bazat pe Ubuntu care să includă un server web Apache și să găzduiască o pagină web simplă cu mesajul „Hello, World!”.

# Descrierea executării lucrării de laborator
1. Deschiți terminalul în directorul containers04 și executați comanda:

docker run -ti -p 8000:80 --name containers04 ubuntu bash
<img width="803" alt="Screenshot 2025-03-09 at 11 52 06" src="https://github.com/user-attachments/assets/0ab58660-7503-49b6-b5bf-86a411a0fa50" />

2. In fereastra deschisa, executați următoarele comenzi și explicați-le:
apt update
<img width="913" alt="Screenshot 2025-03-09 at 11 52 49" src="https://github.com/user-attachments/assets/67f99b90-4e22-4e28-b1fc-5bb9112a9ea9" />
apt install apache2 -y
service apache2 start
<img width="1720" alt="Screenshot 2025-03-09 at 11 54 00" src="https://github.com/user-attachments/assets/eba36b07-77ac-46d7-8cc9-191a2abcf8a4" />
Instaleaza şi porneşte serverul web apache2.

4. Deschideți browserul și introduceți în bara de adrese http://localhost:8000. Ce vedeți? Pagina apache
<img width="1784" alt="Screenshot 2025-03-09 at 11 54 24" src="https://github.com/user-attachments/assets/39125034-6520-41b9-b587-e75f3bb818a5" />

5. Executați următoarele comenzi:
ls -l /var/www/html/
echo '<h1>Hello, World!</h1>' > /var/www/html/index.html
Reîmprospătați pagina în browser. Ce vedeți? - Hello, World!
<img width="278" alt="Screenshot 2025-03-09 at 11 55 07" src="https://github.com/user-attachments/assets/fa8b209f-f46d-4056-a10c-6099d722e674" />

5. Executați următoarele comenzi:
cd /etc/apache2/sites-enabled/
cat 000-default.conf
Ce vedeți pe ecran?
<img width="826" alt="Screenshot 2025-03-09 at 11 56 07" src="https://github.com/user-attachments/assets/94500e38-fc55-4ad5-ba3d-fbbbc7a2e6ba" />

6. Inchideți fereastra terminalului cu comanda exit.

7. Afisați lista de containere:
docker ps -a
<img width="1785" alt="Screenshot 2025-03-09 at 11 56 57" src="https://github.com/user-attachments/assets/90ed5bc9-7459-48db-8831-e7aa87d9e112" />

8. Stergeți containerul:
docker rm containers04
<img width="247" alt="Screenshot 2025-03-09 at 11 57 20" src="https://github.com/user-attachments/assets/0030f68b-fca2-4f96-88d6-d3b22d29b031" />

# Concluzie
Această lucrare m-a ajutat să înțeleg cum să folosesc Docker pentru a crea și gestiona containere. De asemenea, am învățat cum să instalez și să configurez un server web Apache într-un container și cum să creez o pagină web simplă. Docker oferă un mediu eficient pentru testarea și dezvoltarea aplicațiilor în containere izolate.
