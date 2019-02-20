# P3prova1
Prova Programação 3 - 20/02/2019

Relatório:

Classes:

  Main:
      Classe principal, onde são gerenciados todos os recursos do sistema e suas devidas utilizações (usuarios, projetos,    atividades).   
  
  Usuario:
      Classe utilizada apenas para guardar dados dos usuarios, não contem métodos por falta de necessidade.
      
  Tarefa:
      Classe utilizada para guardar a descrição de uma tarefa expecífica e o responsável por realiza-la.
  
  ObjetoAcademico:
      Classe abstrata utilizada para manter informações sobre eventos academicos (Projetos e Atividades)
    
  Atividade e Projeto:
      Subclasses que utilizam da estrutura basica de ObjetoAcademico para criar um ambiente de trabalho compartilhado, cada um com suas particularidades.
  
Distribuição de metodos:
    A classe Main mantem o controle dos metodos responsáveis pelo gerenciamento (criação e composição) dos objetos do sistema. 
  
Classe Abstrata e Herança:
  A classe abstrata ObjetoAcademico serve de estrutura basica para todo tipo de evento (Subclasse) que possua um responsável, uma lista de participantes, início e fim.
  ObjetoAcademico tem como metodo abstrato alocarResponsavel() para que cada evento crie suas proprias regras a respeito de quem pode ser um responsável (como no caso da subclasse Projeto, que delimita o responsável apenas para professores e pesquisadores).
  
Interface:
    A interface Relatar força as classes a implementar a função que imprime as informações que devem estar presentes no relatório individual de cada objeto (Usuario, Projeto, Atividade, Tarefa).
    Tornando os relatórios gerais simples de serem gerados, simplesmente listando os relatórios individuais na sequencia desejada.

Tratamento de Exceções:
    Todas as formas de entrada do programa são restritas a menus numéricos e Strings, as funções que selecionam as opções dos menus lidam com o tratamento de exceptions do tipo NumberFormatException, exigindo uma nova entrada.
    
Extensibilidade:
    Novos tipos de eventos academicos (ObjetoAcademico), que possuam inicio e fim, lista de usuarios e um responsavel, pondem ser criados apenas tornando-os subclasses de ObjetoAcademico.

Reuso:
    O pouco reuso de código necessário do programa esta na utilização da classe abstrata ObjetoAcademico, pois dita boa parte das informações e comportamentos necessárias para a classe Projeto e a classe Atividade.
  
