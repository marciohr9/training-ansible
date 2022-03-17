# Estrutura do Ansible

O Ansible funciona em um servidor como um serviço independente gerindo e atualizando o ambiente unicamente através do SSH, sem necessidade de nenhum código interno no host, apenas SSH e Python.

A **máquina de controle** que é a principal gerênciadora dos projetos com **Ansible** conta com uma estrutura distribuida em cima de 3 tipos de scripts da seguinte forma:
    
    * **Inventário** (  Lista as Máquinas que serão configuradas ).
    * **Playbook** ( arquivo em que normalmente fica todo o passo a passo de configuração e estruturação do projeto).
    * **Roles** ( Formas de modularização do código ).