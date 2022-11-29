   ### 📍 2022/3º Semestre - GROUP HEXTECH
 <p align="justify">No meu terceiro semestre na FATEC, eu e meu grupo tivemos como cliente a empresa IACIT. Uma empresa de consultoria meteorológica, e hoje, um dos  serviços é fornecer aos clientes, relatórios customizados de dados meteorológicos. Como trabalham processando muitas informações manualmente, há uma perda de tempo e desperdício de recursos. </p>
<p align="justify">Por isso, o intuito do nosso grupo é fazer um sistema que nos permita realizar a importação dos dadosmeteorológicos, bem como armazená-los em uma base de dados, para posteriormente gerar os relatórios desejados por nossos clientes.</p>


 <li><a href="https://github.com/GroupHextech/HEXTECH-API3sem/tree/main">→ Repositório deste Projeto</a></li> 
  <li><a href="https://github.com/GroupHextech/HEXTECH-API3sem/blob/main/documents/wireframe_sprint1.pdf">→ Protótipo no Wireframe do Figma</a></li> 
 
## 🔧 Tecnologias Utilizadas
- **Banco de Dados:** PostgreSQL, PGAdmin;
- **Back-end:** Java JDK, JPA, Sprintboot, Spring, Hibernate, Apache Tomcat;
- **Front-end:** HTML5, CSS3, JavaScript, jQuery, Bootstrap, Thymeleaf, Ajax e Figma;
- **Ferramentas:** GitHub, Git, VS Code, Excel, MS Teams, Jira.

## 👨🏻‍💻 Contribuições Pessoais 
<details>
  <summary> Product Backlog, Planejamento das Sprints, Front-End, PO, Manual do Usuário </summary>
<p align="justify">Neste projeto tambem fui escolhido para ser o Product Owner do grupo. No início do projeto, atuei exclusivamente no gerenciamento das tasks no Jira, elaboração do Product Backlog, Sprint Backlog, Front-End, organizei os Planning Pokers e fiz as devidas "tratativas" com o cliente. </p>
 
   <details><summary> Alguns códigos que contribui: </summary>
  
  ```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HexTech</title>

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>

    <link href="./assets/css/style.css" rel="stylesheet" />

    <!-- Bootstrap core CSS     -->
    <link href="/assets/css/bootstrap.min.css" rel="stylesheet" />

    <!-- Animation library for notifications   -->
    <link href="/assets/css/animate.min.css" rel="stylesheet" />

    <!--  Light Bootstrap Table core CSS    -->
    <link
      href="/assets/css/light-bootstrap-dashboard.css?v=1.4.0"
      rel="stylesheet"
    />

    <!--     Fonts and icons     -->
    <link
      href="http://maxcdn.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css"
      rel="stylesheet"
    />
    <link
      href="http://fonts.googleapis.com/css?family=Roboto:400,700,300"
      rel="stylesheet"
      type="text/css"
    />
    <link href="/assets/css/pe-icon-7-stroke.css" rel="stylesheet" />

    <style>
      * {
        margin: 0;
        padding: 0;
      }

      #chart-container {
        position: relative;
        height: 100vh;
        overflow: hidden;
      }

      .fomu {
        border-radius: 15px;
        box-shadow: 3px 1px 10px lightgrey;
      }
      .sb-sidenav .sb-sidenav-menu .nav .sb-sidenav-menu-heading {
        padding: 1.75rem 1rem 0.75rem;
        font-size: 0.75rem;
        font-weight: bold;
        text-transform: uppercase;
      }
    </style>
  </head>

  <body style="background-color: #eeeeee">
    <div class="wrapper">
      <!-- Barra lado -->
      <div
        class="sidebar"
        data-color="gray"
        data-image="assets/img/sidebar-5.jpg"
      >
        <div class="sidebar-wrapper">
          <div class="logo" style="box-shadow: 3px 1px 10px rgb(71, 71, 71)">
            <a class="simple-text">
              <img
                src="assets/img/logo.png"
                height="20px"
                width="20px"
                style="margin-top: -5px"
              />HEXTECH</a
            >
          </div>

          <ul class="nav">
            <li id="painelDeControle" class="active">
              <a onclick="painel()">
                <i class="pe-7s-home"></i>
                <p>Painel de Controle</p>
              </a>
            </li>
            <div
              class="sb-sidenav-menu-heading"
              style="
                padding: 1.75rem 1rem 0.75rem;
                font-size: 1.25rem;
                font-weight: bold;
                text-transform: uppercase;
              "
            >
              Cadastrar
            </div>
            <li id="regiao">
              <a onclick="cadastroRegiao()">
                <i class="pe-7s-plus"></i>
                <p>Região</p>
              </a>
            </li>
            <li id="estado">
              <a onclick="cadastroEstado()">
                <i class="pe-7s-plus"></i>
                <p>Estado</p>
              </a>
            </li>
            <li id="estacao">
              <a onclick="cadastro()">
                <i class="pe-7s-plus"></i>
                <p>Estação</p>
              </a>
            </li>
            <li id="pesquisa">
              <a onclick="pesquisa()">
                <i class="pe-7s-search"></i>
                <p>Pesquisar</p>
              </a>
            </li>
            <li id="filtroEstacoes">
              <a onclick="filtrarEstacoes()" href="/filtroEstacao">
                <i class="pe-7s-search"></i>
                <p>Filtrar Estações</p>
              </a>
            </li>
            <li id="sobreNos">
              <a onclick="sobreNos()">
                <i class="pe-7s-info"></i>
                <p>Sobre Nós</p>
              </a>
            </li>
          </ul>
        </div>
      </div>

      <div class="main-panel">
        <!-- Barra top -->
        <nav
          class="navbar navbar-default navbar-fixed"
          style="box-shadow: 3px 1px 10px lightgrey"
        >
          <div class="container-fluid">
            <div class="navbar-header">
              <button
                type="button"
                class="navbar-toggle"
                data-toggle="collapse"
              >
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
              </button>
              <a class="navbar-brand"> </a>
            </div>
            <div class="collapse navbar-collapse">
              <ul class="nav navbar-nav navbar-left">
                <li>
                  <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                    <i class="fa pe-7s-user"></i>
                  </a>
                </li>
              </ul>

              <ul class="nav navbar-nav navbar-right">
                <li>
                  <a href="logout.php" style="color: black"> Sair </a>
                </li>
              </ul>
            </div>
          </div>
        </nav>

        <!-- Conteudo -->
        <div class="content" style="padding: 30px 0px 0px 0px">
          <iframe
            id="iframe"
            width="100%"
            scrolling="no"
            style="border: none"
          ></iframe>
          <iframe
            id="estacoes"
            width="100%"
            scrolling="no"
            style="border: none"
          ></iframe>
          <iframe
            id="estados"
            width="100%"
            scrolling="no"
            style="border: none"
          ></iframe>
          <iframe
            id="regioes"
            width="100%"
            scrolling="no"
            style="border: none"
          ></iframe>
          <script>
            var altura = window.screen.height;

            document.getElementById("iframe").src = "/grafico";
            document.getElementById("estados").height = 0;
            document.getElementById("estacoes").height = 0;
            document.getElementById("regioes").height = 0;

            function painel() {
              document.getElementById("iframe").height = altura - 241;
              document.getElementById("estados").height = 0;
              document.getElementById("estacoes").height = 0;
              document.getElementById("regioes").height = 0;
              document.getElementById("iframe").src = "/grafico";
              document.querySelector("#painelDeControle").classList.toggle("active");
              document.querySelector("#estacao").classList.remove("active");
              document.querySelector("#regiao").classList.remove("active");
              document.querySelector("#estado").classList.remove("active");
              document.querySelector("#pesquisa").classList.remove("active");
              document.querySelector("#filtroEstacoes").classList.remove("active");
              document.querySelector("#sobreNos").classList.remove("active");
            }

            function cadastro() {
              document.getElementById("iframe").height = altura - 241;
              document.getElementById("estados").height = 0;
              document.getElementById("estacoes").height = 0;
              document.getElementById("regioes").height = 0;
              document.getElementById("iframe").src = "/novaEstacao";
              document.querySelector("#estacao").classList.toggle("active");
              document.querySelector("#painelDeControle").classList.remove("active");
              document.querySelector("#regiao").classList.remove("active");
              document.querySelector("#estado").classList.remove("active");
              document.querySelector("#pesquisa").classList.remove("active");
              document.querySelector("#filtroEstacoes").classList.remove("active");
              document.querySelector("#sobreNos").classList.remove("active");
            }
            function cadastroRegiao() {
              document.getElementById("iframe").height = altura - 241;
              document.getElementById("estados").height = 0;
              document.getElementById("estacoes").height = 0;
              document.getElementById("regioes").height = 0;
              document.getElementById("iframe").src = "/novaRegiao";
              document.querySelector("#regiao").classList.toggle("active");
              document.querySelector("#painelDeControle").classList.remove("active");
              document.querySelector("#estacao").classList.remove("active");
              document.querySelector("#estado").classList.remove("active");
              document.querySelector("#pesquisa").classList.remove("active");
              document.querySelector("#filtroEstacoes").classList.remove("active");
              document.querySelector("#sobreNos").classList.remove("active");
            }
            function cadastroEstado() {
              document.getElementById("iframe").height = altura - 241;
              document.getElementById("estados").height = 0;
              document.getElementById("estacoes").height = 0;
              document.getElementById("regioes").height = 0;
              document.getElementById("iframe").src = "/novoEstado";
              document.querySelector("#estado").classList.toggle("active");
              document.querySelector("#painelDeControle").classList.remove("active");
              document.querySelector("#estacao").classList.remove("active");
              document.querySelector("#regiao").classList.remove("active");
              document.querySelector("#pesquisa").classList.remove("active");
              document.querySelector("#filtroEstacoes").classList.remove("active");
              document.querySelector("#sobreNos").classList.remove("active");
            }
            function pesquisa() {
              document.getElementById("iframe").src = "";
              document.getElementById("iframe").height = 0;
              document.getElementById("estados").height = altura - 400;
              document.getElementById("estacoes").height = altura - 400;
              document.getElementById("regioes").height = altura - 400;
              document.getElementById("estados").src = "/estados";
              document.getElementById("estacoes").src = "/estacoes";
              document.getElementById("regioes").src = "/regioes";
              document.querySelector("#estado").classList.remove("active");
              document.querySelector("#painelDeControle").classList.remove("active");
              document.querySelector("#estacao").classList.remove("active");
              document.querySelector("#regiao").classList.remove("active");
              document.querySelector("#pesquisa").classList.toggle("active");
              document.querySelector("#filtroEstacoes").classList.remove("active");
              document.querySelector("#sobreNos").classList.remove("active");
            }
            function filtrarEstacoes() {
              document.querySelector("#filtroEstacoes").classList.toggle("active");
              document.querySelector("#regiao").classList.remove("active");
              document.querySelector("#painelDeControle").classList.remove("active");
              document.querySelector("#estacao").classList.remove("active");
              document.querySelector("#estado").classList.remove("active");
              document.querySelector("#pesquisa").classList.remove("active");
              document.querySelector("#sobreNos").classList.remove("active");
            }
            function sobreNos() {
              document.getElementById("iframe").height = altura - 241;
              document.getElementById("estados").height = 0;
              document.getElementById("estacoes").height = 0;
              document.getElementById("regioes").height = 0;
              document.getElementById("iframe").src = "/sobreNos"
              document.querySelector("#sobreNos").classList.toggle("active");
              document.querySelector("#regiao").classList.remove("active");
              document.querySelector("#painelDeControle").classList.remove("active");
              document.querySelector("#estacao").classList.remove("active");
              document.querySelector("#estado").classList.remove("active");
              document.querySelector("#pesquisa").classList.remove("active");
              document.querySelector("#filtroEstacoes").classList.remove("active");
            }
          </script>
        </div>
      </div>
    </div>
  </body>

  <!--   Core JS Files   -->
  <script src="/assets/js/jquery.3.2.1.min.js" type="text/javascript"></script>
  <script src="/assets/js/bootstrap.min.js" type="text/javascript"></script>

  <!--  Charts Plugin -->
  <script src="/assets/js/chartist.min.js"></script>

  <!--  Notifications Plugin    -->
  <script src="/assets/js/bootstrap-notify.js"></script>

  <!--  Google Maps Plugin    -->
  <script
    type="text/javascript"
    src="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY_HERE"
  ></script>

  <!-- Light Bootstrap Table Core javascript and methods for Demo purpose -->
  <script src="/assets/js/light-bootstrap-dashboard.js?v=1.4.0"></script>
</html>

 ----------------------------------------------------------------------------------------------------------------------------------------------------------------------

<html xmlns="http://www.w3.org/1999/xhtml" xmlns:th="http://www.thymeleaf.org">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Gráfico</title>

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>

    <!-- CSS only -->
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi"
      crossorigin="anonymous"
    />
    <!-- JavaScript Bundle with Popper -->
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-OERcA2EqjJCMA+/3y+gxIOqMEjwtxJY7qPCqsdltbNJuaOe923+mo//f6V8Qbsw3"
      crossorigin="anonymous"
    ></script>

    <!--  Bootstrap core CSS  -->
    <link href="/assets/css/bootstrap.min.css" rel="stylesheet" />

    <!-- Animation library for notifications -->
    <link href="/assets/css/animate.min.css" rel="stylesheet" />

    <!--  Light Bootstrap Table core CSS    -->
    <link
      href="/assets/css/light-bootstrap-dashboard.css?v=1.4.0"
      rel="stylesheet"
    />

    <!--     Fonts and icons     -->
    <link
      href="http://maxcdn.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css"
      rel="stylesheet"
    />
    <link
      href="http://fonts.googleapis.com/css?family=Roboto:400,700,300"
      rel="stylesheet"
      type="text/css"
    />
    <link href="/assets/css/pe-icon-7-stroke.css" rel="stylesheet" />

    <style>
      * {
        margin: 0;
        padding: 0;
      }

      #chart-container {
        position: relative;
        height: 100vh;
        overflow: hidden;
      }

      .fomu {
        border-radius: 15px;
        box-shadow: 3px 1px 10px lightgrey;
      }
    </style>
  </head>

  <body style="background-color: #eeeeee">
    <div class="row mx-1 my-3">
      <div
        class="col-md-3"
        style="padding: 0px; padding-left: 2%; padding-right: 2%"
      >
        <label for="data1">Data Inicial</label>
        <input class="form-control fomu" type="date" id="data1" />
        <script>
          today = "2021-01-01";
          document.getElementById("data1").value = today;
        </script>
      </div>

      <div
        class="col-md-3"
        style="padding: 0px; padding-left: 2%; padding-right: 2%"
      >
        <label for="data2">Data Final</label>
        <input class="form-control fomu" type="date" id="data2" />
        <script>
          today = "2021-01-31";
          document.getElementById("data2").value = today;
        </script>
      </div>

      <div
        class="col-md-3"
        style="padding: 0px; padding-left: 2%; padding-right: 2%"
      >
        <label>Estação</label>
        <select class="form-control fomu" id="estacao" name="selectEstacao">
          <option
            th:each="est : ${estacoes}"
            th:value="${{est.idEstacao}}"
            th:text="${{est.nomeEstacao}}"
          ></option>
          <option value="A301">Recife (PE)</option>
          <option value="83377">Brasília (DF)</option>
        </select>
      </div>

      <div
        class="col-md-3 d-flex align-items-end"
        style="padding: 0px; padding-left: 2%; padding-right: 2%"
      >
        <button
          class="form-control fomu"
          onclick="env()"
          style="
            box-shadow: 3px 1px 10px lightgrey;
            color: white;
            background-color: rgb(141, 140, 140);
          "
        >
          Enviar
        </button>
      </div>
    </div>

    <!-- Legenda -->
    <div class="col-md-12" style="text-align: center; margin-top: 30px">
      <input
        type="color"
        value="#FF2828"
        disabled
        style="border-style: hidden; height: 20px; width: 16px"
      /><label style="margin-left: 5px">Temperatura Máxima</label>
      <input
        type="color"
        value="#91cc75"
        disabled
        style="
          margin-left: 30px;
          border-style: hidden;
          height: 20px;
          width: 16px;
        "
      /><label style="margin-left: 5px">Temperatura Média</label>
      <input
        type="color"
        value="#5470c6"
        disabled
        style="
          margin-left: 30px;
          border-style: hidden;
          height: 20px;
          width: 16px;
        "
      /><label style="margin-left: 5px">Temperatura Mínima</label>
    </div>

    <div id="grafico"></div>
    <div style="text-align: center;"><a href="/"><button class="btn fomu">Voltar</button></a></div>

    <!-- Grafico -->
    <script src="https://fastly.jsdelivr.net/npm/echarts@5.3.3/dist/echarts.min.js"></script>
    <script>
      var altura = window.screen.height;
      document.getElementById("grafico").innerHTML =
        '<div id="chart-container" class="col-md-12" style="height: ' +
        (altura - 370) +
        'px;"></div>';

      function env() {
        var data1 = document.getElementById("data1").value;
        var data2 = document.getElementById("data2").value;
        var estacao = document.getElementById("estacao").value;

        $.ajax({
          method: "GET",
          url:
            "https://apitempo.inmet.gov.br/estacao/diaria/" +
            data1 +
            "/" +
            data2 +
            "/" +
            estacao,
          success(dados) {
            let linhas = dados.length;
            const datas = [];
            var max = [];
            var med = [];
            var min = [];

            // ARRUMAR DATAS-----------------------------------------
            for (let i = 0; i < linhas; i++) {
              datas.push(dados[i].DT_MEDICAO);
            }
            for (let i = 0; i < linhas; i++) {
              if (dados[i].TEMP_MAX != null) {
                max.push(dados[i].TEMP_MAX.replace('"', ""));
              }
            }
            for (let i = 0; i < linhas; i++) {
              if (dados[i].TEMP_MED != null) {
                med.push(dados[i].TEMP_MED.replace('"', ""));
              }
            }
            for (let i = 0; i < linhas; i++) {
              if (dados[i].TEMP_MIN != null) {
                min.push(dados[i].TEMP_MIN.replace('"', ""));
              }
            }

            var dom = document.getElementById("chart-container");
            var myChart = echarts.init(dom, null, {
              renderer: "canvas",
              useDirtyRect: false,
            });
            var app = {};

            var option;

            const posList = [
              "left",
              "right",
              "top",
              "bottom",
              "inside",
              "insideTop",
              "insideLeft",
              "insideRight",
              "insideBottom",
              "insideTopLeft",
              "insideTopRight",
              "insideBottomLeft",
              "insideBottomRight",
            ];
            app.configParameters = {
              rotate: {
                min: -90,
                max: 90,
              },
              align: {
                options: {
                  left: "left",
                  center: "center",
                  right: "right",
                },
              },
              verticalAlign: {
                options: {
                  top: "top",
                  middle: "middle",
                  bottom: "bottom",
                },
              },
              position: {
                options: posList.reduce(function (map, pos) {
                  map[pos] = pos;
                  return map;
                }, {}),
              },
              distance: {
                min: 0,
                max: 100,
              },
            };
            app.config = {
              rotate: 90,
              align: "left",
              verticalAlign: "middle",
              position: "insideBottom",
              distance: 15,
              onChange: function () {
                const labelOption = {
                  rotate: app.config.rotate,
                  align: app.config.align,
                  verticalAlign: app.config.verticalAlign,
                  position: app.config.position,
                  distance: app.config.distance,
                };
                myChart.setOption({
                  series: [
                    {
                      label: labelOption,
                    },
                    {
                      label: labelOption,
                    },
                    {
                      label: labelOption,
                    },
                    {
                      label: labelOption,
                    },
                  ],
                });
              },
            };
            const labelOption = {
              show: true,
              position: app.config.position,
              distance: app.config.distance,
              align: app.config.align,
              verticalAlign: app.config.verticalAlign,
              rotate: app.config.rotate,
              formatter: "{c}  {name|{a}}",
              fontSize: 16,
              rich: {
                name: {},
              },
            };
            option = {
              tooltip: {
                trigger: "axis",
                axisPointer: {
                  type: "shadow",
                },
              },
              legend: {
                data: ["TEMP_MAX", "TEMP_MED", "TEMP_MIN"],
              },
              toolbox: {
                show: true,
                orient: "vertical",
                left: "right",
                top: "center",
                feature: {
                  mark: {
                    show: true,
                  },
                  dataView: {
                    show: true,
                    readOnly: false,
                  },
                  magicType: {
                    show: true,
                    type: ["line", "bar", "stack"],
                  },
                  restore: {
                    show: true,
                  },
                  saveAsImage: {
                    show: true,
                  },
                },
              },
              xAxis: [
                {
                  type: "category",
                  axisTick: {
                    show: false,
                  },
                  data: datas,
                },
              ],
              yAxis: [
                {
                  type: "value",
                },
              ],
              series: [
                {
                  name: "",
                  type: "line",
                  barGap: 0,
                  color: "#FF2828 ",
                  label: labelOption,
                  emphasis: {
                    focus: "series",
                  },
                  data: max,
                },
                {
                  name: "",
                  type: "line",
                  color: "#91cc75 ",
                  label: labelOption,
                  emphasis: {
                    focus: "series",
                  },
                  data: med,
                },
                {
                  name: "",
                  type: "line",
                  color: "#5470c6 ",
                  label: labelOption,
                  emphasis: {
                    focus: "series",
                  },
                  data: min,
                },
              ],
            };

            if (option && typeof option === "object") {
              myChart.setOption(option);
            }

            window.addEventListener("resize", myChart.resize);
          },
        });
      }
    </script>
  </body>
</html>
```
   </details>
 </details>


 
## 🔹 Hard Skills 
- JAVA: Meu primeiro contato com a linguagem. Tive a oportunidade de conhecer um pouco da sintaxe, estrutura e funções básicas. Com o apoio dos desenvolvedores do grupo, pude aprender a realizar algumas funções e compreender o funcionamento da linguagem.
- Springboot: Entendi como pode ser útil e de muita ajuda a implementação deste framework para simplificar as configurações de aplicações web. Ou seja, creio que foi um conhecimento relevante que agreguei ao meu portifolio.

## 🔹 Soft Skills
- <p align="justify">Resiliência: Nesta API, devido aos problemas de equipe que passamos, pude desenvolver a resiliência para melhor me adaptar aos problemas/obstáculos e seguir adiante com foco na entrega do produto. Foi um desafio e tanto. A necessidade de ser resiliente, enfrentar os problemas de cabeça fria e  driblar estes com certa estratégia, foi fundamental para concluirmos o projeto.
- Estratégia: Creio que essa soft skills é complementar e consequente da acima... Como eu recebi o cargo de Product Owner, era minha responsabilidade de entender as dores, anseios e desejos do cliente para com o projeto à ser executado. Portanto, aprendi a colher os requisitos, regras de negócio, funcionalidades etc.

 
 
