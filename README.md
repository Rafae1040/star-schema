# star-schema
Criando um Star Schema para Cenários de Vendas com Power BI


# Tabelas de Fato:
Fact_Professor:

ProfessorID (PK, FK): Identificador único do professor.
DisciplineID (FK): Identificador único da disciplina ministrada pelo professor.
CourseID (FK): Identificador único do curso ministrado pelo professor.
DepartmentID (FK): Identificador único do departamento ao qual o professor está associado.
DataID (FK): Identificador único da data associada aos eventos do professor.
Measure: Valor analisado (medida específica relacionada ao professor).
Tabelas de Dimensão:
Dim_Professors:

ProfessorID (PK): Identificador único do professor.
ProfessorName: Nome completo do professor.
ProfessorBirthDate: Data de nascimento do professor.
ProfessorGender: Gênero do professor.
Dim_Disciplines:

DisciplineID (PK): Identificador único da disciplina.
DisciplineName: Nome da disciplina.
DisciplineCredits: Créditos associados à disciplina.
Dim_Courses:

CourseID (PK): Identificador único do curso.
CourseName: Nome do curso.
CourseCredits: Créditos associados ao curso.
Dim_Departments:

DepartmentID (PK): Identificador único do departamento.
DepartmentName: Nome do departamento.
Dim_Dates:

DataID (PK): Identificador único da data.
Date: Data no formato 'yyyy-mm-dd'.
Year: Ano da data.
Month: Mês da data.
Day: Dia da data.

# Notas Adicionais:
O esquema em estrela foi projetado com foco na análise dos dados dos professores.
As tabelas de dimensão contêm detalhes relevantes sobre professores, disciplinas, cursos, departamentos e datas.
A tabela de fato (Fact_Professor) vincula as chaves estrangeiras às chaves primárias das tabelas de dimensão.
Foi adicionada uma tabela de dimensão de datas para suportar análises temporais, mesmo que a granularidade não seja fixada.
Os relacionamentos entre as tabelas devem ser estabelecidos conforme as chaves primárias e estrangeiras indicadas.
Observação sobre Datas:
Para compensar a falta de dados de datas no modelo relacional original, foram adicionadas datas associadas a eventos específicos, como a oferta de disciplinas e cursos. A granularidade das datas pode ser ajustada conforme a necessidade da análise.
