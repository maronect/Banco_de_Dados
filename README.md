# Banco_de_Dados
<h1>
<p>Aluno: Marone Carvalho Taques</p>
<p>Tema: Sistema de Gerenciamento de Escola</p>
</h1>

<h2>Objetivo: Desenvolvimento de um MER (Modelo Entidade Relacionamento) que descreva o funcionamento de uma escola.</h2>


<h2>Notação: {} indica a presença de atributos derivados</h2>

<h3>Entidades, Atributos e comentários, respectivamente:</h3>

<p>Professor.
<p> Disciplina: Sala, Grade{Turno, Horário}.
<p>Aluno: Grade Curricular, Turma, Boletim, Méritos (medalhas e premições em olimpiadas, competições e afins).
<p>Familiar (Responsavel pelo pagamento da mensalidade e matícula).
<p>Mensalidade (Pagamento para manutenção do aluno na unidade de estudo).
<p>Matrícula: Documento{Identidade, Visto, Passaporte}, Foto 3/4, Comprovante de Residência, Pagamento, Desconto, Certidão de Nascimento, Histórico Escolar.
<p> Gestão Administrativa.
<p>Recursos: Manutenção Estrutural, Trasnporte{Viagens Coletivas, Condução}, Energéticos, Alimentícios, Materiais Educativos.
<p>Estrutura Escolar: Nome, Localização{País, Estado, Cidade, Bairro, CEP}.
<p>Pessoas:Nome{P_nome, S_nome}, Contato, Endereço, Documento de Identificação, Usuário Online, Senha Online, Horário de Trabalho, Salário.
<p>Técnicos.
<p>Plataformas Digitais: Endereço(URL).
<p>Profissional de saúde.
<p>Zeladores.

<h3>Relacionamentos e cardinalidades entre entidades</h3>

<p> Professor <b>ensina</b> uma ou mais Disciplinas. Estas necessitam de um ou mais professores para serem ensinadas.
<p> Disciplina <b>é estudada</b> por um ou mais Alunos e um aluno estuda uma ou mais disciplinas
<p> Aluno <b>depende</b> de um familiar, e um familiar pode ter 1 ou mais alunos como dependente
<p> Familiar pode <b>efetuar</b> no mínimo uma matrícula ou mensalidade. Já uma mensalidade ou matrícula apenas pode ser feita por uma família.
<p> Apenas uma Matrícula e Mensalidade são <b>administradas</b> pela gestão administrativas. Enquanto a gestão administrativa pode administrar tanto uma matrícula ou mensalidade, quanto várias.
<p> Gestão adminsitrativa <b>coordena</b> de um/uma a vários Recurssos, Pessoas, e Estrutura Estrutura de Ensino. Já os recursos, pessoas e a estrutura de ensino só podem ser coordenado por uma gestão administrativa.  
<p> Profissional de saúde pode <b>prestar atendimento</b> a tanto nenhuma quanto várias pessoas, enquanto as pessoas podem tanto não ser atendiadas, caso não precisem, quanto serem atendidas por vários.
<p>Técnicos podem <b>prestam manutenção</b> tanto a 1 plataforma das plataformas digitais quanto para várias. Assim como uma unica plataforma pode receber manutencão de vários técnicos.
<p>Zeladores <b>mantêm a integridade</b> de apenas uma estrutura de ensino. Enquanto uma estrutura de ensino pode receber manutenção de 1 ou mais zeladores.

<h3>Especialização</h3>
<p> A entidade <b>Pessoa</b> gera váriso subtipos: Familiares, Aluno, Professor, Tecnico, Zelador e Proficional de Saúde. Todos estes apresentam, em comum, os atributos referentes a pessoas, mas divergem a depender de sua <b>especialização</b>, adquirindo relacionamentos e atributos específicos.
