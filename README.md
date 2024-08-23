#### **Projeto:**

Sistema Web de Gerenciamento de Consultas Médicas

### **Descrição do Projeto:**

Site de Gerenciamento de consultas médicas onde usuários serão cadastrados e poderão agendar sua consulta com médicos especializados.

### **Elaboração do Escopo e Objetivos do Projeto:**

- **Escopo:**
    
    Este sistema de gerenciamento é uma aplicação web que permitirá o cadastro e a consulta de usuários, que irão ou que agendaram uma consulta médica. Também a busca e visualização de informações detalhadas do usuário (por exemplo medicamentos que ele tem alergia), para que o trabalho seja mais eficiente e eficaz. Utilizando uma filtragem, o aplicativo fornecerá dados sobre a consulta do dia ou da semana.
    
- **Objetivos:**
    - **Específicos:**
        
        Eficiência e Eficácia - Facilitar o processo e o controle de consultas médicas.
        
        Cadastro de Pacientes - O sistema consegue cadastrar usuários, com informações básicas (cpf, nome, telefone), para quando o paciente agendar uma consulta novamente o histórico médico já estará registrado 
        
        **Agendamento de Consultas: -** Permitir que os usuários agendem, editem e cancelem consultas médicas com facilidade.
        
        **Filtragem de Dados:** Fornecer uma filtragem para que os administradores possam visualizar consultas do dia ou da semana.
        
    - **Mensuráveis:**
        
        **Tempo de Processamento:** Tempo médio para agendar e gerenciar consultas.
        
        **Tempo de Processamento:** Tempo médio para agendar e gerenciar consultas.
        
    - **Atingíveis:**
        
        **Tecnologia Adequada:** Utilização de tecnologias e ferramentas que garantam a estabilidade e segurança do sistema.
        
    - **Relevantes:**
        
        **Aumento da Produtividade:** Permitir que médicos e administradores sejam mais produtivos e eficientes em suas funções diárias.
        
        **Melhoria na Gestão de Consultas:** Reduzir erros humanos e melhorar a organização no agendamento e controle de consultas.
        

### **Planejamento do Projeto:**

- **Cronograma:**

| Etapa | Descrição | Tempo Estimado |
| --- | --- | --- |
| **Planejamento** | Levantamento de requisitos, escopo, diagramas, objetivos e recursos utilizados ao longo do projeto | 1 dia |
| **Desenvolvimento**  | Configuração do Ambiente de desenvolvimento Criando Models e Controllers | 1 dia |
| **Codificação** | Codificação do projeto (PHP Laravel) - Fazer agendamento e Views | 1 dia |
| **Testes e Ajustes** | Testes funcionais, integração, correção de bugs | 1 dia |
|  |  |  |
- **Recursos:**
    
    **Programadores:** Especialistas em desenvolvimento frontend e backend.
    
    **Designer:** Responsável pela experiência do usuário e design da interface, garantindo que a aplicação seja intuitiva e visualmente atraente.
    
    **Servidor Web:** Hospedagem para a aplicação web
    
    **Banco de Dados:** Onde os dados do sistema são armazenados e gerenciados (PostgreSQL)
    
    **Ferramentas de Desenvolvimento:**  Visual Studio Code, Git, GitHub, Notion, ChatGpt
    
    **Ferramentas de Prototipagem:**  Figma
    
    **Ferramentas para criação de Diagramas:**  Draw.io
    
    **Linguagem e Framework:** Php e Laravel 
    

### **Análise de Riscos:**

**Risco 1:** Atrasos no desenvolvimento devido a mudanças nos requisitos ou problemas técnicos.

**Solução:** Planejamento detalhado e flexível, comunicação constante com a equipe e gerenciamento ágil. Desenvolvimento de Sprints ao longo da semana

### **Desenvolvimento:**

**Diagrama de Desenvolvimento**

Diagrama de Classe

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/79194d87-0048-4f56-bfd8-d3f4f1dbc3be/a9e4997c-0792-43d9-b35f-86bfae03274d/image.png)

Diagrama de Fluxo

+---------------------+
|  Acesso ao Sistema  |
+---------------------+
           |
           v
+-------------------------------+
|     Tela de Login/Registro     |
|-------------------------------|
|        Novo Usuário            |
|        Usuário Existente       |
+-------------------------------+
           |
   +-------+--------+
   |                |
   v                v
+---------------------+     +----------------------+
|   Preenchimento     |     |   Inserção de        |
|   do Formulário     |     |   Credenciais        |
+---------------------+     +----------------------+
           |                        |
           v                        v
+---------------------+     +----------------------+
|   Sistema valida    |     |   Sistema valida     |
|   informações       |     |   credenciais        |
+---------------------+     +----------------------+
           |                        |
           v                        v
+---------------------+     +----------------------+
|   Cadastro Completo |     |   Login Bem-Sucedido |
+---------------------+     +----------------------+
           |                        |
           v                        v
+-------------------------------+   +-----------------------------+
|   Redireciona para Tela de    |   |   Redireciona para Painel   |
|   Login                       |   |   Principal                 |
+-------------------------------+   +-----------------------------+
                                   |
                                   v
                        +------------------------+
                        |     Painel Principal   |
                        |------------------------|
                        |   Agendar Consulta     |
                        |   Visualizar Consultas |
                        |   Logout               |
                        +------------------------+
                           |           |         |
                           v           v         v
           +---------------------+  +-------------------+  +--------------------+
           | Agendar Consulta    |  | Visualizar        |  | Logout             |
           |---------------------|  | Consultas         |  |--------------------|
           | Usuário escolhe     |  | Seleciona Período |  | Encerrar Sessão    |
           | médico e data/hora  |  |                   |  |                    |
           +---------------------+  +-------------------+  +--------------------+
                    |                    |                      |
                    v                    v                      v
     +-----------------------------+    +----------------------------+
     | Sistema verifica            |    | Sistema filtra consultas   |
     | disponibilidade             |    |                            |
     +-----------------------------+    +----------------------------+
        |             |                         |
   +----+----+  +-----+-----+           +-------+-------+
   | Disponível |  | Não      |           | Mostrar       |
   |            |  | Disponível |          | Consultas     |
   +------------+  +-----------+           +---------------+
        |                 |                      |
        v                 v                      v
+------------------+     +-----------------+    +-------------------+
| Consulta Agendada |     | Mensagem de Erro|    | Visualizar Consultas |
| + Mensagem de    |     | + Usuário Tenta |    | (continua)           |
| Confirmação      |     | Novamente        |    +-------------------+
+------------------+     +------------------+  
           
