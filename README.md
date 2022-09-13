# projeto-conceitual-oficina

## **Resumo do desafio**
Nesse desafio, foi feita a criação de um diagrama para uma oficina mecânica.

### **Descrição das tabelas:**
* **Cliente:** Será guardada as informações básicas do cliente e seu código. Nas inforções de Cliente, ficará armazenado o código da equipe que está responsável pelo serviço.
* **Veículo:** Essa tabela está ligada ao cliente, pois um veículo pertence a um cliente. Cardinalidade (1,n), porque um cliente pode ter mais de um veículo.
* **Mecânico:** Possui as informações básicas dos mecânicos. Ficará salvo também nessa tabela a qual equipe um mecânico estará relacionado.
* **Equipe:** Tabela que representará cada equipe de mecânicos. As equipes serão diferenciadas pelo seu código. Sobre os relacionamentos ligados à tabela equipe, as seguintes tabelas receberão "idEquipe" como chave estrangeira:
1. Cliente: Para saber qual equipe está atendendo o cliente. Cardinalidade: (1,n);
2. Veículo: Para saber qual equipe está cuidando do veículo. Cardinalidade: (1,n);
3. Mecânico: Receberá a chave estrangeira para identificar sua equipe. Cardinalidade: (1,n);
4. Ordem de serviço: Identificará qual equipe está responsável pelo serviço. Cardinalidade: (1,n);
5. Pedido de peças: Receberá o código da equipe para registrar quem fez os pedidos.
* **Ordem do serviço:** Tabela que contém as informações do serviço a ser prestado. Por essa tabela, faz-se a interação com a tabela Peça e a Tabela referência de serviço. 
* **Peça:** Armazenará as informações das peças separadamente. Uma peça pode ser usada em vários serviços, e um serviço pode requisitar várias peças, por isso a cardinalidade será (n,m)
* **Pedido de peças:** Essa é a tabela contendo as informações de cada pedido que será feito por uma equipe para um serviço. Por isso, ela conterá as chaves estrangeiras:
1. idPeça;
2. idEquipe;
3. idOrdem de serviço.
* **Tabela referência de serviço:** Tabela com os valores referência de cada serviço. Cardinalidade (n,m).
* **Ordem de serviço consulta a tabela:** Tabela que armazena as chaves primárias de Ordem de serviço e Tabela referência de serviço após uma consulta.
#### [Confira o Diagrama](diagrama_oficinalMecanica.png)