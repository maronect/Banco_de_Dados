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
<p>Aluno: Grade Curricular, Turma, Boletim/Notas, Méritos (medalhas e premições em olimpiadas, competições e afins), Documento de Identificação, Foto 3/4, Comprovante de Residência, Pagamento, Desconto, Certidão de Nascimento, Histórico Escolar.
<p>Familiar (Responsavel pelo pagamento dos valores(matrícula, mensalidade e atividades extracurriculares: Artes, Robótica, Esportes e Aulas de Reforço)).
<p> Gestões Administrativas(Responsavel pelo histórico de alunos e pelas notas fiscais relacionadas a: Eventos, Manutenção Estrutural, Trasnporte{Viagens Coletivas, Condução}, Energéticos, Alimentícios e Materiais Educativos).
<p>Estrutura de Ensino: Nome, Localização{País, Estado, Cidade, Bairro, CEP}.
<p>Pessoas:Nome{P_nome, S_nome}, Contato, Endereço, Documento de Identificação, Usuário Online, Senha Online, Horário de Trabalho, Salário.
<p>Técnicos:Usuário Online de Adminsitrador e Senha Online de Administrador.
<p>Plataformas Digitais: Endereço(URL).
<p>Profissional de saúde: Equipamentos de Saúde Atribuidos(Imobilizadores e Macas).
<p>Zeladores: Equipamentos de Manutenção atribuidos: Panos, Rodos, Vassouras, Baldes e Uniforme.

<h3>Relacionamentos e cardinalidades entre entidades</h3>

<p> Professor <b>ensina</b> uma ou mais Disciplinas. Estas necessitam de um ou mais professores para serem ensinadas.
<p> Disciplina <b>é estudada</b> por um ou mais Alunos e um aluno estuda uma ou mais disciplinas
<p> Aluno <b>depende</b> de um familiar, e um familiar pode ter 1 ou mais alunos como dependente
<p> Familiar pode <b>Pagar</b> um ou mais valores, podendo ser este: a mensalidade, a matrícula ou referente a atividades extracurriculares(Artes, Robótica, Esportes e Aulas de Reforço). Enquanto As gestões administrativas podem receber um ou mais de um valor como pagamento.
<p> Gestões adminsitrativas <b>coordenam</b> de uma a várias Pessoas. Já as pessoas só podem ser coordenadas apenas por uma gestão administrativa.
<p> Gestões adminsitrativas <b>administram</b> uma estrutura de ensino. Já uma estrutura de ensino pode ser anminsitrada por uma ou mais gestões admnistrativas.
<p> Profissional de saúde pode <b>prestar atendimento</b> a tanto nenhuma quanto várias pessoas, enquanto as pessoas podem tanto não ser atendiadas, caso não precisem, quanto serem atendidas por vários.
<p>Técnicos podem <b>prestam manutenção</b> tanto a 1 plataforma das plataformas digitais quanto para várias. Assim como uma unica plataforma pode receber manutencão de vários técnicos.
<p>Zeladores <b>mantêm a integridade</b> de apenas uma estrutura de ensino. Enquanto uma estrutura de ensino pode receber manutenção de 1 ou mais zeladores.

<h3>Especialização</h3>
<p> A entidade <b>Pessoa</b> gera váriso subtipos: Familiares, Aluno, Professor, Tecnico, Zelador e Proficional de Saúde. Todos estes apresentam, em comum, os atributos referentes a pessoas, mas divergem a depender de sua <b>especialização</b>, adquirindo relacionamentos e atributos específicos.

<h3>Explicação das escolhas de entidades</h3>

<p><b>Aluno</b>, <b>Professor</b>, <b>Disciplina</b> e <b>Matrícula</b> foram indicados a serem criados como obrigatórios, centralizando a ideia de ambiente escolar.</p>

<p><b>Matrícula</b>, <b>Mensalidade</b> e as <b>Atividades Extracurriculares</b> são os possiveis pagamentos realizados pelos familiares responsaveis pelo aluno. Tal pagamento é direcionado à entidade responsavel por administrar e coordenar as pessoas e a unidade de ensino como um todo, as <b>gestões administrativas</b>.</p>

<p>A gestão administrativa tem o controle do histórico de alunos e na geração de nota fiscal. Esta nota fiscal seria referente a:</p>

<p>Reformas estruturais na isntituição, transporte, quanto a mobilidade dos alunos até a escola e para passeios fora desta, energéticos, para internet, energia, no geral, e equipamentos eléticos, como cantina e tomadas, alimentícios, referente à lanchonete e materiais educativos para equipamentos voltados ao ensino motor em aulas práticas como objetos relacionados a arte, tecnologia, entre outros.</p>

<p>A estrutura de ensino correspode ao ambiente em que as pessoas estariam presente durante o periodo estudantil.</p>

<p>A entidade <b>Pessoas</b> merece destaque.</p>

<p>Nesta caracteristicas em comum para: Alunos, os estudantes, Familiares, responsaveis pelo pagamento e manutenção dos alunos na instituição de ensino, Professores, os que mentorarão as aulas, Técnicos, responsaveis por fazer a manutenção de plataformas digitais, Proficionais de saúde, proficionais que manterão a saude física e mental dos presentes na instituição e zeladores, os quais proverão a manutenção da integridade física da estrutura de ensino, estarão agrupadas. Entre as caracteristicas comumente presente entre as pessoas: Nome, Contato, Endereço, Documento de Identificação, Usuário Online, Senha Oline, sendo estes responsaveis pelo acesso á plataformas disponiveis na internet, relacionadas a instituição; salário e horas de trabalho, para proficionais que rootineiramente dedicam seu tempo ao grupo de ensino. </p>