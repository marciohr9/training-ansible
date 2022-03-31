# Como funciona a estruturação da roles

O **Ansible** usa de estrutura padrões para fazer a boa execução do seu código, essa estrutura pode ser definida tanto dentro do provisioning que é o playbook que será executado ou essa mesma estrutura é replicada dentro da pasta **"roles"** que será usada para modularizar e organizar o código facilitando a sim a compreenção ou o uso de partes dele.

Como fica a estruturação da pasta roles.

- **Roles**
  - <nome_role>
    _( todas as pastas dentro da pasta role devem contar o nome que será usado para a role no arquivo principal de chamada, e cada pasta deve conter a seguinte estrutura.)_
    - handlers
      _( pasta ou tag usada em que todas os serviços que podem ser replicados em multiplas tasks são salvos, serviços como reinicialização de uma aplicação e coisas afins. )_
    - tasks
      _( pasta ou tag padrão usada onde se contem todas as tarefas a serem executadas por aquele grupo de máquinas )_
    - templastes
      _( template é um caso especial, o ansible faz uso dos templates em jinja ou seja todos os arquivos na pasta de template devem terminar com a extensão **.j2** dentro dos templates você pode substituir palavras ou áreas especificas pelas váriaveis previamente definidas na pasta de **group\_vars** da mesma forma que você utiliza essas váriaveis dentro do playbook para facilitar o reuso e dificultar o erro por mudanças constantes no código. )_
