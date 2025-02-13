# **Star Schema para Análise de Professores no Power BI**

## 📌 **Visão Geral**
O **Star Schema** foi projetado para fornecer uma análise eficiente dos dados relacionados aos professores, incluindo disciplinas, cursos e departamentos. Esse modelo facilita consultas rápidas e otimizadas no **Power BI**, garantindo uma estrutura bem organizada e de fácil compreensão.

---
## 🌟 **Estrutura do Modelo**
O esquema é composto por:
- **Uma tabela de fato** que centraliza os eventos e métricas associadas aos professores.
- **Cinco tabelas de dimensão** que armazenam detalhes sobre professores, disciplinas, cursos, departamentos e datas.

### 🔹 **Tabelas de Fato**
#### **Fact_Professor** (Eventos e Métricas)
| Campo | Tipo | Descrição |
|-----------------|-----------|-------------|
| **ProfessorID** (PK, FK) | INT | Identificador único do professor. |
| **DisciplineID** (FK) | INT | Identificador único da disciplina ministrada. |
| **CourseID** (FK) | INT | Identificador único do curso ministrado. |
| **DepartmentID** (FK) | INT | Identificador único do departamento do professor. |
| **DateID** (FK) | INT | Identificador único da data associada ao evento. |
| **Measure** | DECIMAL | Métrica analisada (exemplo: carga horária total, número de alunos atendidos). |

---
### 🔹 **Tabelas de Dimensão**

#### **Dim_Professors** (Professores)
| Campo | Tipo | Descrição |
|------------------|-----------|-------------|
| **ProfessorID** (PK) | INT | Identificador único do professor. |
| **ProfessorName** | VARCHAR | Nome completo do professor. |
| **ProfessorBirthDate** | DATE | Data de nascimento. |
| **ProfessorGender** | VARCHAR | Gênero do professor. |

#### **Dim_Disciplines** (Disciplinas)
| Campo | Tipo | Descrição |
|-----------------|-----------|-------------|
| **DisciplineID** (PK) | INT | Identificador único da disciplina. |
| **DisciplineName** | VARCHAR | Nome da disciplina. |
| **DisciplineCredits** | INT | Quantidade de créditos da disciplina. |

#### **Dim_Courses** (Cursos)
| Campo | Tipo | Descrição |
|-------------|-----------|-------------|
| **CourseID** (PK) | INT | Identificador único do curso. |
| **CourseName** | VARCHAR | Nome do curso. |
| **CourseCredits** | INT | Quantidade de créditos do curso. |

#### **Dim_Departments** (Departamentos)
| Campo | Tipo | Descrição |
|---------------|-----------|-------------|
| **DepartmentID** (PK) | INT | Identificador único do departamento. |
| **DepartmentName** | VARCHAR | Nome do departamento. |

#### **Dim_Dates** (Datas)
| Campo | Tipo | Descrição |
|-----------|-----------|-------------|
| **DateID** (PK) | INT | Identificador único da data. |
| **Date** | DATE | Data no formato 'YYYY-MM-DD'. |
| **Year** | INT | Ano correspondente. |
| **Month** | INT | Mês correspondente. |
| **Day** | INT | Dia correspondente. |

---
## 🚀 **Destaques e Benefícios**
✅ **Modelo otimizado para consultas rápidas no Power BI** 📊
✅ **Análises temporais detalhadas com a tabela de datas** ⏳
✅ **Relacionamentos bem definidos entre tabelas para insights estratégicos** 🔗

Com esse modelo, você poderá criar **dashboards interativos e análises profundas** sobre distribuição de disciplinas, carga horária dos professores, relação entre cursos e departamentos, e muito mais! 🎯📈

