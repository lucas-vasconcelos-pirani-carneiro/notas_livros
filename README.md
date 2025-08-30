# Notas de Livros

Este repositório contém anotações em LaTeX de livros estudados, organizadas por livro e capítulo.  
A ideia é centralizar os resumos e exemplos em um só lugar, facilitando revisões e colaborações.

## Estrutura
```txt
📂 notas_livros/
├── 📂 nome-do-livro_autor/
│   ├── 📂 capitulos/
│   │   └── cap01_introducao.tex
│   ├── 📂 imagens/
│   │   └── imagem01.jpeg
│   ├── 📂 compilados/
│   │   └── anotacoes.pdf
│   ├── 📄 main.tex
│   ├── 📄 preambulo.tex
│   ├── 📄 bibliografia.bib
│   └── 📄 Makefile
├── 📄 README.md
└── 📄 .gitignore
```

- `/capitulos` : Arquivos LaTeX de cada capítulo ou seção.
- `/imagens` : Diagramas e figuras utilizadas nas anotações.
- `/compilados` : PDFs finais compilados.
- `main.tex` : Arquivo principal do livro (sumário + inclusão dos capítulos).
- `preambulo.tex` : Pacotes, estilos e comandos personalizados do LaTeX.
- `bibliografia.bib` : Banco de referências para citações bibliográficas.
- `Makefile` : Automatiza a compilação e organização dos arquivos .pdf e temporários.
- `.gitignore` : Ignora arquivos temporários do LaTeX.

## Como compilar os PDFs usando Makefile
Cada livro deste repositório possui um arquivo Makefile que automatiza o processo de compilação dos arquivos LaTeX, geração do PDF e limpeza de arquivos temporários. Assim, todo o fluxo fica padronizado e fácil de usar.

### Passos 

- Acesse a pasta do livro desejado.*Exemplo* :
>```bash
>cd nome-do-livro_autor
>```

- Compile o projeto  
Este comando **compila** o arquivo `main.tex` e move o `.pdf` gerado para o diretório `compilados/` com um nome padronizado:

>```bash
>make
>```

Exemplo de saída: `compilados/anotacoes.pdf`

- **Limpe arquivos** temporários do LaTeX. (mantém apenas o PDF final)

>```bash
>make clean
>```

- Remova também os PDFs compilados

>```bash
>make cleanall
>```

## Observações
- É necessário ter um compilador LaTeX instalado, como o pdflatex (disponível no pacote TeX Live para Linux, macOS ou Windows).
- Os arquivos temporários (como .aux, .log) nunca são versionados no GitHub, graças ao .gitignore já incluído.
- Você pode adaptar o nome do PDF a ser gerado modificando a variável correspondente no topo do Makefile.

## Licença
Este projeto está licenciado sob a licença `MIT`.   
Sinta-se à vontade para sugerir melhorias, abrir issues ou contribuir com novos resumos e anotações para outros livros!
