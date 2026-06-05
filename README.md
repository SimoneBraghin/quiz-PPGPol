# Quiz de Ciência Política
**Cursinho Popular UFSCar × PPGPol**

Quiz interativo de vestibular para estudantes pré-universitários, com questões reais de ENEM, FUVEST, VUNESP e COMVEST sobre Ciência Política e Sociologia Política.

🔗 **Acesse o quiz:** [seu-usuario.github.io/quiz-ppgpol](https://seu-usuario.github.io/quiz-ppgpol)

---

## Funcionalidades

- **44 questões** de provas reais (ENEM, FUVEST, VUNESP, COMVEST)
- Questões **embaralhadas** a cada sessão
- Aluno escolhe **quantas questões** quer responder (5, 10, 20, 30 ou todas)
- **Cronômetro** configurável por questão (sem limite, 2, 3 ou 5 min)
- **Gabarito só no final** — com detalhamento de acertos, erros e em branco
- Funciona em **mobile e desktop**
- **Sem servidor** — HTML + JSON puro, hospedado no GitHub Pages

---

## Estrutura do projeto

```
quiz-ppgpol/
├── index.html              ← quiz interativo (página principal)
├── data/
│   └── questoes.json       ← banco de questões (editável)
├── curadoria/
│   ├── relatorio_curadoria.html   ← relatório de curadoria (129 questões analisadas)
│   ├── acervo_incluidas.html      ← 45 questões incluídas com enunciado completo
│   └── acervo_excluidas.html      ← 29 questões excluídas com motivo
└── README.md
```

---

## Como adicionar questões

Edite o arquivo `data/questoes.json`. Cada questão segue este formato:

```json
{
  "id": 45,
  "num_original": "Q23",
  "vestibular": "ENEM 2019",
  "eixo": "eixo-3",
  "eixo_label": "Eixo 3 — Partidos, Sistemas Eleitorais e Presidencialismo",
  "enunciado": "Texto completo da questão...",
  "alternativas": {
    "A": "Texto da alternativa A",
    "B": "Texto da alternativa B",
    "C": "Texto da alternativa C",
    "D": "Texto da alternativa D",
    "E": "Texto da alternativa E"
  },
  "gabarito": "C"
}
```

**Eixos disponíveis:**
- `eixo-1` — Política e Poder (Weber, Maquiavel, Foucault, Arendt)
- `eixo-2` — Estado Moderno e Regimes Políticos (contratualistas, democracia, ditadura)
- `eixo-3` — Partidos, Sistemas Eleitorais e Presidencialismo *(sem questões no banco atual)*
- `eixo-4` — Teoria das Elites (Mosca, Pareto, Michels, Wright Mills)
- `eixo-5` — Cidadania, Direitos e Participação (Marshall, CF/1988, movimentos sociais)

---

## Como publicar no GitHub Pages

1. Faça upload de todos os arquivos neste repositório
2. Vá em **Settings → Pages**
3. Em **Source**, selecione `Deploy from a branch` → `main` → `/ (root)`
4. Clique em **Save**
5. Em ~1 minuto o site estará disponível em `https://seu-usuario.github.io/nome-do-repositorio`

> ⚠️ **Atenção:** O quiz usa `fetch('data/questoes.json')`. Isso **não funciona** se você abrir o `index.html` diretamente no navegador (protocolo `file://`). Para testar localmente, use uma extensão como *Live Server* no VS Code, ou publique direto no GitHub Pages.

---

## Distribuição atual do banco

| Eixo | Questões |
|------|----------|
| Eixo 1 — Política e Poder | 11 |
| Eixo 2 — Estado Moderno e Regimes Políticos | 20 |
| Eixo 3 — Partidos e Sistemas Eleitorais | 0 ⚠️ |
| Eixo 4 — Teoria das Elites | 2 |
| Eixo 5 — Cidadania, Direitos e Participação | 11 |
| **Total** | **44** |

| Vestibular | Questões |
|------------|----------|
| ENEM | 11 |
| VUNESP | 14 |
| COMVEST | 6 |
| FUVEST | 7 |
| Coletânea ENEM (q100) | 6 |

---

## Sobre o projeto

Desenvolvido no âmbito do **Cursinho Popular da UFSCar** em parceria com o **PPGPol — Programa de Pós-Graduação em Ciência Política da UFSCar**.

Este site/quiz faz parte da parceria entre o Programa de Pós-Graduação em Ciência Política e o Cursinho Popular da UFSCar que tem como objetivo produzir, a partir dos documentos de área e dos vestibulares realizados no Estado de São Paulo, um material de apoio para ensino de temas de política de forma transversal, bem como de preparação para questões de vestibulares de mesmo caráter.

Esta é uma atividade de extensão do PPGPol e é composta por docentes e discentes do programa. São eles: 

- Profa. Dra. Gleidylucy Oliveira (coordenadora docente),
- Bel. Dannilo Carlos (coordenador discente)
- Bel. Lilian Tassim Salantino (bolsista do projeto),
- Me. Lucas Romano López (bolsista do projeto),
- Bel. Mariana Stuchi (bolsista do projeto), e
- Me. Simone Braghin (bolsista do projeto).
