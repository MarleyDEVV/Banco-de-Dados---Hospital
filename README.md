# Banco-de-Dados---Hospital
# 1. O Hospital Fundamental.
Mãos a Obra Analise a seguinte descrição e extraia dela os requisitos para o banco de dados: O hospital necessita de um sistema para sua área clínica que ajude a controlar consultas realizadas. Os médicos podem ser generalistas, especialistas ou residentes e têm seus dados pessoais cadastrados em planilhas digitais. Cada médico pode ter uma ou mais especialidades, que podem ser pediatria, clínica geral, gastroenterologia e dermatologia. Alguns registros antigos ainda estão em formulário de papel, mas será necessário incluir esses dados no novo sistema.

Os pacientes também precisam de cadastro, contendo dados pessoais (nome, data de nascimento, endereço, telefone e e-mail), documentos (CPF e RG) e convênio. Para cada convênio, são registrados nome, CNPJ e tempo de carência.

As consultas também têm sido registradas em planilhas, com data e hora de realização, médico responsável, paciente, valor da consulta ou nome do convênio, com o número da carteira. Também é necessário indicar na consulta qual a especialidade buscada pelo paciente.

Deseja-se ainda informatizar a receita do médico, de maneira que, no encerramento da consulta, ele possa registrar os medicamentos receitados, a quantidade e as instruções de uso. A partir disso, espera-se que o sistema imprima um relatório da receita ao paciente ou permita sua visualização via internet.
![BD-hospital1](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/8ac8fbce-45d8-49e9-8612-5d47fc36c83d)

# 2.Os Segredos do Hospital
Entender do assunto Considere a seguinte descrição e o diagrama ER abaixo:

No hospital, as internações têm sido registradas por meio de formulários eletrônicos que gravam os dados em arquivos.

Para cada internação, são anotadas a data de entrada, a data prevista de alta e a data efetiva de alta, além da descrição textual dos procedimentos a serem realizados.

As internações precisam ser vinculadas a quartos, com a numeração e o tipo.

Cada tipo de quarto tem sua descrição e o seu valor diário (a princípio, o hospital trabalha com apartamentos, quartos duplos e enfermaria).

Também é necessário controlar quais profissionais de enfermaria estarão responsáveis por acompanhar o paciente durante sua internação. Para cada enfermeiro(a), é necessário nome, CPF e registro no conselho de enfermagem (CRE).

A internação, obviamente, é vinculada a um paciente – que pode se internar mais de uma vez no hospital – e a um único médico responsável.
# Mãos a obra?

Faça a ligação do diagrama acima ao diagrama desenvolvido na atividade antrior, construindo relacionamentos com entidades relacionadas. E eleve o seu diagrama para que já selecionando os tipos de dados que serão trabalhados e em quais situações.

Por último, crie um script SQL para a geração do banco de dados e para instruções de montagem de cada uma das entidades/tabelas presentes no diagrama completo (considerando as entidades do diagrama da atividade anterior e as novas entidades propostas no diagrama acima). Também crie tabelas para relacionamentos quando necessário. Aplique colunas e chaves primárias e estrangeiras. Use ferramentas, como ERPlus, Lucidchart, draw.io (via web) e MySQL Workbench, ou mesmo um editor de imagens para o diagrama.

Você pode utilizar o MySQL Workbench ou o DBdiagram.io para montar os scripts SQL.
![BD-hospital2](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/7bca59c3-6c35-4112-bbfb-30205bb79338)

# 3. O Prisioneiro de dados.
Jogando nas regras que você criou: Crie scripts de povoamento das tabelas desenvolvidas na atividade anterior Observe as seguintes atividades: Inclua ao menos dez médicos de diferentes especialidades.

Ao menos sete especialidades (considere a afirmação de que “entre as especialidades há pediatria, clínica geral, gastrenterologia e dermatologia”).

Inclua ao menos 15 pacientes.

Registre 20 consultas de diferentes pacientes e diferentes médicos (alguns pacientes realizam mais que uma consulta). As consultas devem ter ocorrido entre 01/01/2015 e 01/01/2022. Ao menos dez consultas devem ter receituário com dois ou mais medicamentos.

Inclua ao menos quatro convênios médicos, associe ao menos cinco pacientes e cinco consultas.

Criar entidade de relacionamento entre médico e especialidade.

Criar Entidade de Relacionamento entre internação e enfermeiro.

Arrumar a chave estrangeira do relacionamento entre convênio e médico.

Criar entidade entre internação e enfermeiro.

Colocar chaves estrangeira dentro da internação (Chaves Médico e Paciente).

Registre ao menos sete internações. Pelo menos dois pacientes devem ter se internado mais de uma vez. Ao menos três quartos devem ser cadastrados. As internações devem ter ocorrido entre 01/01/2015 e 01/01/2022.

Considerando que “a princípio o hospital trabalha com apartamentos, quartos duplos e enfermaria”, inclua ao menos esses três tipos com valores diferentes.

Inclua dados de dez profissionais de enfermaria. Associe cada internação a ao menos dois enfermeiros.

Os dados de tipo de quarto, convênio e especialidade são essenciais para a operação do sistema e, portanto, devem ser povoados assim que o sistema for instalado.
# 4. A Ordem do Alterar.

Mãos a Obra. Pensando no banco que já foi criado para o Projeto do Hospital, realize algumas alterações nas tabelas e nos dados usando comandos de atualização e exclusão:

Crie um script que adicione uma coluna “em_atividade” para os médicos, indicando se ele ainda está atuando no hospital ou não.

Crie um script para atualizar ao menos dois médicos como inativos e os demais em atividade.
![BD-hospital3](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/feb8807b-a018-42c4-a952-251f11f984a0)

# 5. As Relíquias dos Dados.
Mãos a obra Crie um script e nele inclua consultas que retornem:

-- Consulta 1: Todos os dados e valor médio das consultas do ano de 2020 e das que foram feitas sob convênio.
![BD-hospital4](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/22e3af71-a845-4a5c-b697-23786a0ddcb8)

-- Consulta 2: Todos os dados das internações que tiveram data de alta maior que a data prevista para a alta
![BD-hospital5](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/3026f2f9-e417-4f88-9289-522e1a687ae0)

-- Consulta 3: Receituário completo da primeira consulta registrada com receituário associado
![BD-hospital6](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/e9930beb-abbb-4136-8abe-3d3c4ff9e6aa)

-- Consulta 4: Todos os dados da consulta de maior valor e também da de menor valor (ambas as consultas não foram realizadas sob convênio)
![BD-hospital7](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/9f38693d-8730-4c3e-b907-efebd7ba91e9)

-- Consulta 5: Todos os dados das internações em seus respectivos quartos, calculando o total da internação a partir do valor de diária do quarto e o número de dias entre a entrada e a alta
![BD-hospital8](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/1e969aec-bfb8-42ce-9577-42774cfc2578)

-- Consulta 6: Data, procedimento e número de quarto de internações em quartos do tipo “apartamento”
![BD-hospital9](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/ed65cecb-37b3-47e4-be74-bb946e7a22c8)

-- Consulta 7: Nome do paciente, data da consulta e especialidade de todas as consultas em que os pacientes eram menores de 18 anos na data da consulta e cuja especialidade não seja “pediatria”, ordenando por data de realização da consulta
![BD-hospital10](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/1531c042-f541-43ad-9d8b-94abb1cdd5d1)

-- Consulta 8: Nome do paciente, nome do médico, data da internação e procedimentos das internações realizadas por médicos da especialidade “gastroenterologia”, que tenham acontecido em “enfermaria”
![BD-hospital11](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/a5e6ffbf-ab58-4163-8f6b-db26e2b6c4ac)

-- Consulta 9: Os nomes dos médicos, seus CRMs e a quantidade de consultas que cada um realizou
![BD-hospital12](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/21e59bf1-31f9-47cd-b890-cea5bff8c76a)

-- Consulta 10: Todos os médicos que tenham "Gabriel" no nome
![BD-hospital13](https://github.com/MarleyDEVV/Banco-de-Dados---Hospital/assets/161721052/194f19bb-f5e6-4ea4-8bc7-2f1751fe7f61)

