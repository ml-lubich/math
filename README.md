# Math

> Some of my undergraduate math projects, neatly typed in **LaTeX**.
> First-year topics that pushed my comfort zone — multivariable
> calculus, differential equations — and the first time I learned and
> fell in love with LaTeX. From here on out I swore to do all my math
> in LaTeX :)

```mermaid
flowchart LR
    TEX[("📝 LaTeX source")]
    BUILD{{"🛠 latex / pdflatex"}}
    OUT["📄 PDFs"]
    EULER[/"📕 Extending Euler's Method"/]
    VOP[/"📕 Variation of Parameters"/]
    COMPLEX[/"📕 What are the Complex Numbers?"/]
    WRAP[/"📕 Wrap up of Math 1B"/]

    TEX --> BUILD --> OUT
    OUT --> EULER
    OUT --> VOP
    OUT --> COMPLEX
    OUT --> WRAP

    classDef io fill:#0e1116,stroke:#2f81f7,stroke-width:1.5px,color:#e6edf3;
    classDef tool fill:#161b22,stroke:#3fb950,stroke-width:1.5px,color:#e6edf3;
    classDef brain fill:#161b22,stroke:#d29922,stroke-width:1.5px,color:#e6edf3;
    classDef out fill:#0e1116,stroke:#a371f7,stroke-width:1.5px,color:#e6edf3;
    class TEX io;
    class BUILD tool;
    class OUT brain;
    class EULER,VOP,COMPLEX,WRAP out;
```

## Table of contents

- [Contents](#contents)
- [LaTeX build (algorithm)](#latex-build-algorithm)
- [Topic map](#topic-map)
- [🗺️ Repository map](#️-repository-map)

## LaTeX build (algorithm)

```mermaid
flowchart LR
    A([*.tex source])
    B["pdflatex pass 1<br/>resolve refs"]
    C{"refs changed?"}
    D["pdflatex pass 2<br/>fix labels"]
    E["bibtex (if .bib)"]
    F["pdflatex final pass"]
    G([*.pdf])
    A --> B --> C
    C -- yes --> D --> E --> F --> G
    C -- no  --> G
```

## Topic map

```mermaid
flowchart TB
    M["Math 1B + Multivariable"]
    ODE["Differential Equations"]
    NUM["Numerical methods"]
    LIN["Linear theory"]
    CPLX["Complex Numbers"]
    SER["Series + Integrals"]

    M --> ODE
    M --> CPLX
    M --> SER
    ODE --> NUM
    ODE --> LIN
    NUM -.-> EUL["Extending Euler's Method.pdf"]
    LIN -.-> VOP["Variation of Parameters.pdf"]
    CPLX -.-> CXN["What are the Complex Numbers?.pdf"]
    SER -.-> WRP["Wrap up of Math 1B.pdf"]
```

## Contents

| File | Topic |
|---|---|
| `Extending Euler's Method.pdf` | Numerical ODE: extending Euler's method. |
| `Variation of Parameters.pdf` | Solving inhomogeneous linear ODEs via variation of parameters. |
| `What are the Complex Numbers?.pdf` | Construction and intuition for `ℂ`. |
| `Wrap up of Math 1B.pdf` | End-of-course synthesis (single-variable integral calc / series). |


## 🗺️ Repository map

Top-level layout of `math` rendered as a Mermaid mindmap (auto-generated from the on-disk tree).

```mermaid
mindmap
  root((math))
    files
      README.md
```
