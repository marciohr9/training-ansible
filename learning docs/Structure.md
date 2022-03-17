# Estrutura do Ansible

## Teoria da Arquitetura Base 

O Ansible funciona em um servidor como um serviço independente gerindo e atualizando o ambiente unicamente através do SSH, sem necessidade de nenhum código interno no host, apenas SSH e Python. Isso é em teoria a base para como o Ansible deve normativamente funcionar, como uma **Infrastructure as Code (IaC)**.

A **máquina de controle** que é a principal gerênciadora dos projetos com **Ansible** conta com uma estrutura distribuida em cima de 3 tipos de scripts da seguinte forma:
    
  - **Inventário** (  Lista as Máquinas que serão configuradas ).
  - **Playbook** ( arquivo em que normalmente fica todo o passo a passo de configuração e estruturação do projeto).
  - **Roles** ( Formas de modularização do código ).

Exemplo visual abaixo.

[!IaCAnsible(https://i.imgur.com/3h2NMZR.jpg)]