# Sistema de Locadora de Veículos 

**Curso:** Análise e Desenvolvimento de Sistemas  
**Disciplina:** Programação Orientada a Objetos - INF008  
**Professor(a):** Sandro Santos Andrade  

**Integrantes da Dupla (Listados em ordem alfabética):**  
* Mariana Santos do Rêgo (20242160028)  
* Thais Ribeiro Menezes (20242160013)

---

# Pré-Requisitos do Sistema
Seguindo as instruções disponibilizada no documento de orientação, foram utilizados os seguites recursos:  
* **Java JDK 25**
* **Maven**
* **Java FX 21.0.2**
* **Docker e Docker Compose**
* **MariaDB – Sistema gerenciador de banco de dados**

---

# Comandos para Compilar e Executar  
O sistema de Locadora de Veículos foi desenvolvido com base nos arquivos fornecidos pelo professor da disciplina. O projeto foi arquitetado utilizando Microkernel e Plugins. A equipe realizou alterações na distribuição dos arquivos da pasta disponibilizada para a construção do trabalho visando maior clareza e organização do projeto geral. Visando evitar erros ou problemas na executação do sistema, os passos para compilação e execução são:  

**1º Passo: Subir o Banco de Dados (Docker)**  

1. Abrir o terminal na pasta do projeto, onde está localizado o docker-compose.yml e executar 
   docker-compose up

2. Assim, o banco do MariaDB inicializará o script init.sql (também presente na pasta) e as tabelas serão criadas.

3. No projeto, dentro do pacote "database", há uma classe DBTest, que checará se o banco de dados foi carregado no código.

**2º Passo: Compilação do Projeto e geração dos Plugins**  

Passo obrigatório que compilará o projeto e gerará automaticamente os arquivos .jar dos plugins, localizados na pasta target/plugins, permitindo que o sistema os carregue dinamicamente.

Executar no terminal o comando:
 mvn clean package

**3º Passo: Executar a Aplicação**

Após o passo anterior, a interface gráfica deverá ser inicializada com o comando:
mvn javafx:run

**Teste de Remoção de Plugins**  

1. Certificar de ter executado o passo 2.
2. Navegar até a pasta gerada com a compilação: target/plugins
3. Delete algum dos arquivos de plugin .jar (ex: car-rental-system-1.0-SNAPSHOT-suv.jar ou car-rental-system-1.0-SNAPSHOT-report1.jar)
4. Execute o sistema novamente com o comando:
mvn java fx:run
5. Ao tentar acessar a funcionalidade do plugin deletado, o sistema exibirá um alerta de erro, informando indisponibilidade deste. No entanto, o resto da aplicação funcionará normalmente.


---

# Vídeo da Apresentação  
Segue abaixo o link para visualização da apresentação dos pontos centrais do Sistema para Locação de Veículos. O vídeo contém a participação de todos os integrantes e foi estruturado de forma a apresentação as decisões de estrutura e código centrais desenvolvidos durante a construção do sistema. Foi utilizado o software Active Presenter para a gravação do vídeo e o mesmo foi postado na plataforma Youtube.  
**Link do vídeo:** https://youtu.be/Up3HdcvO2XQ?si=zDsRlZBQyEFpg9_q









