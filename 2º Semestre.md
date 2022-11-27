  ### 📍 2021/2º Semestre - INODEVS 
  <img align="right" src="https://user-images.githubusercontent.com/82103455/196815906-0dac1fb3-67a3-495f-bc2a-57d7e393e3f5.jpg" height="240px">
 <p align="justify">No meu segundo semestre na FATEC, eu e meu grupo tivemos como cliente a empresa JETSOFT, uma empresa que oferece aos seus clientes e parceiros soluções surpreendentes e inovadoras, privilegiando as relações humanas, estando próximos, conhecendo profundamente suas atividades e desejos, para apoiar de forma ágil e flexível a implementação das suas diversas estratégias de negócio..</p>
<p align="justify">O objetivo do nosso grupo é criar um CRUD para uma empresa de software, com a proposta de emitir relatórios mensais apresentando um quadro de presença de colaboradores em postos de trabalhos acordados em contrato.</p>


 <li><a href="https://github.com/Inodevs/Inodevs">→ Repositório deste Projeto</a></li> 
  <li><a href="https://www.figma.com/proto/tipWpDl8AF1pPSGCAsVdGA/Untitled?node-id=94%3A2&scaling=scale-down-width&page-id=91%3A2&starting-point-node-id=94%3A2">→ Protótipo no Wireframe do Figma</a></li> 
 
## 🔧 Tecnologias Utilizadas
- **Banco de Dados:** MySQL e Wampserver;
- **Back-end:** PHP;
- **Front-end:** HTML5, CSS e JavaScript;
- **Ferramentas:** GitHub, VS Code, Canva, Excel e Figma.

## 👨🏻‍💻 Contribuições Pessoais

<details>
  <summary> FrontEnd, Design, Manual do Usuário e GitHub </summary>
<p align="justify">Dei o pontapé inicial do front-end e design do site, elaborei os wireframes das telas no figma e até no WIX para ter mais noção de recursos de UX, sempre em acordo com todos do grupo. Também contribui com a criação do manual do usuário e elaboração do repositório no github.</p>
 
  <details><summary> Alguns códigos que contribui: </summary>
  
  ```
  
<div class="site">
    <div id="cabecalho">
        <div class= " menu-principal ">
            <img class= "imagem" src="../img/perfil.jpg" alt=" Logo Inodevs">
            <br>
            <br>
            <a href="#conteudo-principal">Quem somos</a>
            <a href="#conteudo-secundario">Serviços</a>
            <a href="#rodape">Fale conosco</a>
        </div>
    </div>

    <div id="conteudo">
        <div id="conteudo-principal">
            <h1>Quem somos</h1>
             Somos uma empresa de tecnologia que esta iniciando sua jornada. <br>
             Nossa equipe é composta por um grupo de sete alunos do curso matutino de análise e desenvolvimento de <br> 
             sistemas da Fatec de São José dos Campos. 
            <br>
            <br>
            <br>
            <img class= "perfis" src="../img/imagem3.jpg" title="Scrum master Kauã Renó" alt="Scrum master Kauã Renó ">
            <img class= "perfis" src="../img/imagem7.jpg" title="Product Owner Luiz Habaeb" alt=" Product Owner Luiz Habaeb ">
            <img class= "perfis" src="../img/imagem6.jpg" title="Desenvolvedor Gustavo Kenji" alt=" Desenvolvedor Gustavo Kenji ">
            <img class= "perfis" src="../img/imagem1.jpg" title="Desenvolvedora Júlia Maria" alt=" Desenvolvedora Júlia Maria ">
            <img class= "perfis" src="../img/imagem2.jpg" title=" Desenvolvedora Júlia Rafaela" alt=" Desenvolvedora Júlia Rafaela ">
            <img class= "perfis" src="../img/imagem4.jpg" title="Desenvolvedor Luis Henrique" alt=" Desenvolvedor Luis Henrique ">
            <img class= "perfis" src="../img/imagem5.jpg" title="Desenvolvedora Maria Eduarda" alt=" Desenvolvedora Maria Eduarda ">
        </div>
    </div>

    <br>
    <br>
    <div id="rodape">

        <h1>Fale conosco:</h1>
        <p id="telefone-email">
            Inodevs.contact@gmail.com: <a href="mailto: Inodevs.contact@gmail.com?Subject=Título%20da%20mensagem" target="_blank">Enviar email</a> 
            <br>
            <br>
            Github: <a href="https://github.com/Inodevs" target="_blank">  Inodevs</a>
            <br>
        </p>
        <p id="endereco">
            <br>
            São José dos Campos - SP
        </p>
        <p>
            <a id="voltar" href="../php/controle.php">Voltar para o menu</a>
        </p>
        <b>        
            <small id="copyright">
            &copy; Inodevs Ltda. Todos os Direitos Reservados.
            </small>
        </b>
    </div>

</div>
    
    // CSS
    
    /*imagem de fundo*/
body {
    background-image: url(../img/fundo.jpg);
    background-repeat: no-repeat ;
    background-size: 100%;
    background-attachment: fixed;
    color: #333;
    margin-bottom: 50px;
    margin-top: 50px;
}

/*fundo branco no texto*/
.site{
    width: 70%;
    background-color: white;
    margin: 0 auto;
    height: auto;
}

.perfis{
    width: 80px;
    height: 80px;

}
/*.php{
    width: 120px;
    height: 80px;
}
/*.php{
    width: 230px;
    height: 120px;
}*/
.imagem{
    width: 300px;
    height: 300px;  
}

body, input, select, textarea {
    font-family: "Segoe UI";
    text-align: center;
}

a{
    border-radius: 6px; 
    padding:5px;
    text-decoration: none;
    text-align:center;	
    color:#ccc;
    background: rgb(95, 93, 98);	
    width:120px;  
    height:24px;
}

a:hover {
    color: #000;
    text-decoration: none;
}

p {
    font-size: 16px;
    margin-bottom: 1.5em;
    line-height: 1.4em;
    font-family: Marker Felt, fantasy;
}

#conteudo-principal h1 {
    font-size: 36px;
    margin-bottom: 0.5em;
   font-family: Marker Felt, fantasy;
}

#conteudo-principal h2,
#conteudo-secundario h1 {
    font-size: 24px;
    margin-bottom: 0.5em;
    font-family: Marker Felt, fantasy;
}

#conteudo-secundario p {
    font-size: 14px;
}

#rodape h1{
    font-size: 24px;
    margin-bottom: 0.5em;
    font-family: Marker Felt, fantasy;
}

#rodape {
    padding-bottom: 25px;
}

.menu-principal{
    margin: 0 auto;
    padding-top: 25px;
}

li {
    list-style-type: none;
}

.php{
    width: 200px;
    height: 100px; 
}

#voltar {
    color: black;
}

@media screen and (max-width: 480px) {     
    #rodape h1{
        font-size: 12px;
    }

    #conteudo-secundario p {
        font-size: 6.5px;
    }

    #conteudo-principal h2,
    #conteudo-secundario h1 {
        font-size: 16px;
    }

    p {
        font-size: 12px;
    }
    
    #conteudo-principal h1 {
        font-size: 20px;
    }

    .imagem{
        width: 175px;
        height: 150px;  
    }

    #copyright{
        font-size: 10px;
    }

    .site{
        width: 80%;
    }

    .perfis{
        width: 60px;
        height: 60px;
    }

    body {
        margin-bottom: 25px;
        margin-top: 25px;
        background-size: 230%;
    }

}
  
  ```
 
  </details>    
    
  <details><summary> Complementando... </summary>
  <p align="justify">Vale destacar também que foi meu primeiro ano na FATEC, fazendo um curso de tecnologia e participando de um projeto que, embora acadêmico, possui responsabilidades relevantes e tem alta dimensão de aprendizado. No início do semestre me lembro de ficar com receio de não conseguir realizar um bom trabalho, mas foi ai que surgiu o aprendizado diário com o time, professores e colegas de sala. Ali comecei a aprender o compromisso com as Dailys e a importância destas, aprendi como funcionava o SCRUM, ou seja, até eu chegar  no Manual do Usuário, Elaboração do Github e "desenho" dos Wireframes (como citei antes) foram muitas horas dedicadas de pesquisa, aprendi a pesquisa e pude contribuir com o grupo aplicando todo o conteúdo que absorvi durante o semestre para contribuir com os itens que citei até aqui. </p>
  </details>
</details>
 
## 🔹 Hard Skills
- MySQL: Meu primeiro contato com a ferramenta. Tive a oportunidade de conhecer um pouco da sintaxe do MySQL, consequentemente da liguagem SQL. Com o apoio dos desenvolvedores do grupo, pude aprender a realizar consultas básicas nas tabelas e contribuir com ideias para o desenvolvimento do projeto.
- Github: Fiquei responsável por elaborar o Github do projeto. Nunca tinha tido o contato direto com a plataforma e foi bem interessante aprender o _markdown_ para criar uma boa estrutura de apresentação do projeto para o cliente. Na faculdade nós não tinhamos uma matéria de dedicada à isso, embora sempre tivemos apoio dos professores. Então pesquisei por conta própria e o aprendizado foi fundamental para  a API e também para o meu trabalho.

## 🔹 Soft Skills
- <p align="justify">Product Owner: Nesta API eu tive a oportunidade de trabalhar como PO no meu time. Portanto, foi uma experiência que agregou muito no quesito de "negociação" e gerenciamento do projeto. No início da Sprint 1, como eu nunca havia trabalhado dessa forma, acabei fazendo algumas perguntas "redundantes" e sem muita relevância para o cliente/projeto. Porém ao decorrer do projeto acessei bastante materiais de SCRUM, gerenciamento de projetos e relacionamento com o cliente - o que fez total diferença até o fim do projeto porque extraímos informações imprescindíveis para a conclusão do sistema.
- Levantamento de Requisitos: Creio que essa soft skills é complementar e consequente da acima... Como eu recebi o cargo de Product Owner, era minha responsabilidade de entender as dores, anseios e desejos do cliente para com o projeto à ser executado. Portanto, aprendi a colher os requisitos, regras de negócio, funcionalidades etc.

 
 
