<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>

**Drone Bélico 🛩️**
</center></font>

>*Observação 1: A estrutura inicial deste documento é só um exemplo. O seu grupo deverá alterar esta estrutura de acordo com o que está sendo solicitado na disciplina.*

>*Observação 2: O índice abaixo não precisa ser editado se você utilizar o Visual Studio Code com a extensão **Markdown All in One**. Essa extensão atualiza o índice automaticamente quando o arquivo é salvo.*

**Conteúdo**

- [Autores](#autores)
- [Descrição do Projeto](#descrição-do-projeto)
- [Análise de Requisitos Funcionais e Não-Funcionais](#análise-de-requisitos-funcionais-e-não-funcionais)
- [Diagrama de Atividades](#diagrama-de-atividades)
- [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)
- [Descrição dos Casos de Uso](#descrição-dos-casos-de-uso)
- [Diagrama de Sequência](#diagrama-de-sequência)
- [Diagrama de Classes](#diagrama-de-classes)
- [Diagrama de Estados](#diagrama-de-estados)
- [Diagrama de Implantação](#diagrama-de-implantação)
- [Referências](#referências)


# Autores

* Aluno 1 : Lendy Naiara Carpio Pacheco - 10428525
* Aluno 2 : Rafael de Souza Alves de Lima - 10425819
* Aluno 3 : Daniela Pereira da Silva - 10410906
* Aluno 4 : Caio Henrique Santos Carvalho - 10425408


# Descrição do Projeto

O projeto visa garantir uma solução tecnológica eficiente e inovadora para operações militares, incluindo funcionalidades avançadas de monitoramento, navegação e segurança.


# Análise de Requisitos Funcionais e Não-Funcionais
 **Requisitos Funcionais**

Os requisitos funcionais definem as principais funcionalidades do sistema:
* **Gerenciamento da Frota:** Permitir o monitoramento e controle simultâneo de múltiplos drones, exibindo status e telemetria em tempo real.
* **Operação Remota e Autônoma:** Controlar drones manualmente via interface ou permitir operação autônoma por meio de inteligência artificial.
* **Navegação Inteligente:** Utilizar sensores como LIDAR, GPS e câmeras para mapear o ambiente, evitar obstáculos e ajustar rotas dinamicamente.
* **Comunicação Segura e Estável:** Garantir conexão confiável entre drones e servidores, com protocolos seguros e redundância para evitar falhas.
* **Registro e Auditoria:** Armazenar dados de missões, trajetórias e eventos críticos com criptografia e logs de auditoria.
* **Segurança Avançada:** Implementar autenticação multifator e monitoramento contínuo para prevenir acessos não autorizados.

**Requisitos Não Funcionais**

Os requisitos não funcionais garantem qualidade e confiabilidade do sistema:
* **Desempenho:** O sistema deve processar dados e comandos dos drones em tempo real.
* **Segurança:** Implementação de criptografia avançada e autenticação robusta.
* **Disponibilidade:** Infraestrutura distribuída para alta disponibilidade e failover automático.
* **Usabilidade:** Interface intuitiva para operação eficiente por militares e técnicos.


# Diagrama de Atividades

![Diagrama de Atividades](https://github.com/grupo4G/UML-01-FCI/blob/62eb0e77bf56ec806b219f41d03e8b25aab93065/docs/img/Diagrama.png)


# Diagrama de Casos de Uso

![Diagrama de Caso de Uso](https://github.com/grupo4G/UML-01-FCI/blob/62eb0e77bf56ec806b219f41d03e8b25aab93065/docs/img/DiagramaDeCasoDeUso.png)


# Descrição dos Casos de Uso

## Caso de Uso: Autenticar Acesso ao Sistema

| Campo                  | Autenticar Acesso ao Sistema                                              |
|------------------------|---------------------------------------------------------------------------|
| **Nome do Caso de Uso** | Autenticar Acesso ao Sistema                                              |
| **Ator Principal**      | Operador Militar                                                          |
| **Atores Secundários**  | Sistema de Autenticação                                                   |
| **Resumo**              | Este caso de uso descreve as etapas para autenticar o operador no sistema, garantindo acesso seguro. |
| **Pré-condições**       | O operador precisa estar previamente cadastrado.                          |
| **Pós-condições**       | O operador terá acesso autorizado ao sistema.                             |
| ***FLUXO PRINCIPAL*** |   
| Ações do Ator                                | Ações do Sistema                                                     |
| 1. Operador acessa a interface de login      | 2. Sistema solicita autenticação com senha ou biometria             |
| 3. Operador insere suas credenciais          | 4. Sistema valida os dados                                          |
|                                             | 5. Caso válidos, acesso é concedido ao operador                     |                                              
| ***FLUXOS ALTERNATIVOS*** |
| Código | Descrição                                                                 |
| A1     | Se o operador errar as credenciais, o sistema registra a tentativa mal sucedida. |
| A2     | Após múltiplas tentativas incorretas, o sistema bloqueia o acesso do operador.    |
|***FLUXOS DE EXCEÇÃO*** |
| Código | Descrição                                                                 |
| E1     | Falha de comunicação com o servidor de autenticação impede o login.       |
| E2     | Biometria inválida ou erro no segundo fator de autenticação.              |
|***RESTRIÇÕES E VALIDAÇÕES*** |- O operador deve possuir cadastro válido.<br>- O sistema deve seguir as políticas de autenticação segura (biometria, múltiplos fatores).<br>- Registro de logs para cada tentativa de acesso deve ser mantido.|


## Caso de Uso: Bloquear Sistema após Tentativas de Erro

| Campo                   | Bloquear Sistema após Tentativas de Erro                                       |
|-------------------------|---------------------------------------------------------------------------------|
| **Nome do Caso de Uso** | Bloquear Sistema após Tentativas de Erro                                       |
| **Ator Principal**      | Sistema de Autenticação                                                         |
| **Atores Secundários**  | Operador Militar                                                                |
| **Resumo**              | Este caso de uso descreve o bloqueio automático do sistema após múltiplas tentativas de autenticação mal sucedidas, garantindo a segurança do acesso. |
| **Pré-condições**       | O operador deve ter tentado autenticar-se várias vezes com falha.               |
| **Pós-condições**       | O acesso do operador é temporariamente bloqueado até que seja desbloqueado por um administrador. |
| ***FLUXO PRINCIPAL***   |   
| Ações do Ator                          | Ações do Sistema                                                             |
| -                                     | 1. Detecta número excessivo de tentativas mal sucedidas                      |
| -                                     | 2. Gera log da tentativa mal sucedida                                        |
| -                                     | 3. Bloqueia o acesso do operador ao sistema                                  |
| -                                     | 4. Notifica o administrador do sistema                                       |
| ***FLUXOS ALTERNATIVOS*** |
| Código | Descrição                                                                 |
| A1     | O sistema pode solicitar autenticação com fator adicional antes do bloqueio definitivo. |
| A2     | O operador pode tentar redefinir a senha antes de atingir o limite de tentativas. |
| ***FLUXOS DE EXCEÇÃO*** |
| Código | Descrição                                                                 |
| E1     | Falha no registro de logs pode impedir rastreabilidade do bloqueio.       |
| E2     | Sistema não detecta corretamente o número de falhas e não executa o bloqueio. |
| ***RESTRIÇÕES E VALIDAÇÕES*** |- O sistema deve registrar todas as tentativas de autenticação.<br>- Deve haver um número máximo de tentativas permitido (ex: 3).<br>- O bloqueio deve ser reversível apenas por administradores com credenciais válidas.<br>- Notificações devem ser geradas para administradores. |


## Caso de Uso: Alterar Senha

| Campo                   | Alterar Senha                                                                   |
|-------------------------|----------------------------------------------------------------------------------|
| **Nome do Caso de Uso** | Alterar Senha                                                                   |
| **Ator Principal**      | Operador Militar                                                                |
| **Atores Secundários**  | Sistema de Autenticação                                                         |
| **Resumo**              | Este caso de uso descreve o processo pelo qual um operador militar altera sua senha de acesso ao sistema. |
| **Pré-condições**       | O operador deve estar autenticado no sistema.                                   |
| **Pós-condições**       | A nova senha é salva e utilizada nas próximas autenticações.                    |
| ***FLUXO PRINCIPAL***   |   
| Ações do Ator                          | Ações do Sistema                                                             |
| 1. Acessa a opção de alterar senha     | 2. Solicita senha atual e nova senha                                         |
| 3. Informa senha atual e nova senha    | 4. Valida a senha atual e verifica requisitos da nova senha                  |
|                                       | 5. Atualiza a senha no sistema e confirma alteração                          |
| ***FLUXOS ALTERNATIVOS*** |
| Código | Descrição                                                                 |
| A1     | O sistema pode solicitar confirmação da nova senha digitada.              |
| A2     | O operador pode cancelar a operação antes da confirmação final.           |
| ***FLUXOS DE EXCEÇÃO*** |
| Código | Descrição                                                                 |
| E1     | A senha atual informada está incorreta.                                    |
| E2     | A nova senha não atende aos critérios mínimos de segurança.               |
| E3     | Erro de comunicação impede a atualização da senha no banco de dados.      |
| ***RESTRIÇÕES E VALIDAÇÕES*** |- A nova senha deve seguir as políticas de segurança (mínimo de caracteres, caracteres especiais, etc).<br>- O sistema deve validar a senha atual antes de permitir a alteração.<br>- Deve ser registrada uma notificação de alteração de senha para o operador.<br>- Todas as alterações devem ser registradas em log para auditoria. |


# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
