erDiagram
    Historico {
        string codigo_curso PK
        string matricula_aluno PK
        string nome_curso
        string nome_aluno
        string situacao_aluno
    }
    
     Componente{
      string codigo PK
      string descricao
    }
    
    Professor {
        string professor_matricula PK
        string nome_professor
    }
    
    Diario {
        string diario PK
        string codigo_curso FK
        string matricula_aluno FK
        string codigo FK
        string professor_matricula FK
        string semestre
        string notas
        string faltas
        string status
    }
    
    Historico ||--o{ Diario : "has"
    Diario ||--o{ Componente : "has"
    Diario ||--o{ Professor : "has"
