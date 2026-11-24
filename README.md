<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#10100d">
<title>MZ FITNESS | Treino Inteligente</title>

<style>
:root {
 --preto:#0b0c0b;
 --card:#171914;
 --card2:#22241c;
 --amarelo:#f4d21e;
 --branco:#f7f7f2;
 --cinza:#a5a79a;
 --borda:#34362d;
}

*{box-sizing:border-box}

body{
 margin:0;
 background:var(--preto);
 color:var(--branco);
 font-family:Arial,Helvetica,sans-serif;
}

button,input,select{font:inherit}

button{cursor:pointer}

.app{
 max-width:1100px;
 margin:auto;
 padding-bottom:85px;
}

header{
 height:72px;
 padding:15px 22px;
 display:flex;
 justify-content:space-between;
 align-items:center;
 border-bottom:1px solid var(--borda);
 background:#10110f;
 position:sticky;
 top:0;
 z-index:10;
}

.logo{
 font-size:27px;
 font-weight:1000;
 letter-spacing:-1px;
}

.logo span{color:var(--amarelo)}

.logo small{
 display:block;
 font-size:9px;
 letter-spacing:3px;
 color:var(--cinza);
}

.avatar{
 width:40px;
 height:40px;
 background:var(--amarelo);
 color:#111;
 border-radius:50%;
 display:grid;
 place-items:center;
 font-weight:bold;
}

main{padding:22px 18px}

.hero{
 min-height:280px;
 border-radius:20px;
 padding:28px;
 background:
 linear-gradient(90deg,#090a09 5%,#090a09d9 55%,#090a0940),
 linear-gradient(135deg,#393a29,#171914);
 border:1px solid #48452a;
 display:flex;
 flex-direction:column;
 justify-content:center;
}

.etiqueta{
 color:var(--amarelo);
 font-size:11px;
 letter-spacing:3px;
 font-weight:bold;
}

.hero h1{
 font-size:clamp(32px,7vw,52px);
 line-height:1;
 margin:15px 0;
 max-width:500px;
}

.hero p{
 color:#c4c5bb;
 max-width:450px;
 line-height:1.6;
}

.btn{
 background:var(--amarelo);
 color:#111;
 border:0;
 border-radius:30px;
 padding:13px 20px;
 font-weight:900;
}

.btn-sec{
 background:transparent;
 color:white;
 border:1px solid var(--borda);
 border-radius:25px;
 padding:10px 15px;
}

.cards{
 display:grid;
 grid-template-columns:repeat(2,1fr);
 gap:13px;
 margin:18px 0;
}

.card{
 background:var(--card);
 border:1px solid var(--borda);
 border-radius:17px;
 padding:17px;
 margin-bottom:12px;
}

.numero{
 font-size:29px;
 font-weight:900;
 margin:9px 0;
}

.muted{
 color:var(--cinza);
 font-size:13px;
 line-height:1.5;
}

.titulo{
 font-size:23px;
 margin:10px 0 18px;
}

.secao{
 display:flex;
 justify-content:space-between;
 align-items:center;
 margin:25px 0 13px;
}

.secao h2{font-size:19px;margin:0}

.menu-cards{
 display:grid;
 grid-template-columns:repeat(2,1fr);
 gap:12px;
}

.menu-card{
 background:var(--card);
 border:1px solid var(--borda);
 border-radius:16px;
 padding:18px;
 color:white;
 text-align:left;
 min-height:110px;
}

.menu-card .icone{font-size:25px}
.menu-card strong{display:block;margin:10px 0}
.menu-card small{color:var(--cinza)}

nav{
 position:fixed;
 bottom:0;
 left:0;
 right:0;
 background:#11120ff5;
 border-top:1px solid var(--borda);
 display:flex;
 justify-content:center;
 z-index:20;
}

.nav-in{
 width:min(100%,700px);
 display:flex;
 justify-content:space-around;
 padding:10px 3px;
}

nav button{
 border:0;
 background:none;
 color:#999b90;
 font-size:10px;
 display:grid;
 gap:5px;
 justify-items:center;
}

nav button span{font-size:20px}
nav button.ativo{color:var(--amarelo)}

.campo{
 display:grid;
 gap:7px;
 margin:13px 0;
}

.campo label{
 color:var(--cinza);
 font-size:12px;
}

input,select{
 background:#0c0e0b;
 color:white;
 border:1px solid #414337;
 padding:13px;
 border-radius:10px;
 width:100%;
}

input:focus,select:focus{
 outline:1px solid var(--amarelo);
}

.grade-form{
 display:grid;
 grid-template-columns:1fr 1fr;
 gap:10px;
}

.linha{
 display:flex;
 justify-content:space-between;
 align-items:center;
 gap:10px;
 padding:13px 0;
 border-bottom:1px solid var(--borda);
}

.tag{
 color:var(--amarelo);
 border:1px solid #665b20;
 border-radius:20px;
 padding:5px 10px;
 font-size:10px;
}

.resultado{
 background:#28291d;
 border:1px solid #665b20;
 border-radius:13px;
 padding:16px;
 margin-top:14px;
}

.oculto{display:none}

.vazio{
 text-align:center;
 padding:25px;
 color:var(--cinza);
 background:var(--card);
 border-radius:14px;
}

.acoes{
 display:flex;
 flex-wrap:wrap;
 gap:8px;
}

.alerta{
 color:var(--cinza);
 font-size:11px;
 line-height:1.5;
 margin-top:15px;
}

.exercicio{
 display:flex;
 align-items:center;
 gap:12px;
}

.ex-img{
 width:55px;
 height:55px;
 background:var(--card2);
 border-radius:12px;
 display:grid;
 place-items:center;
 font-size:25px;
}

@media(max-width:500px){
 main{padding:17px 13px}
 .hero{padding:23px;min-height:260px}
 .grade-form{grid-template-columns:1fr}
 nav button{font-size:9px}
}
</style>
</head>

<body>

<div class="app">

<header>
 <div class="logo">
  MZ<span>.</span>
  <small>FITNESS · TREINO INTELIGENTE</small>
 </div>
 <div class="avatar" id="avatar">MZ</div>
</header>

<main id="conteudo"></main>

<nav>
 <div class="nav-in">
  <button class="ativo" data-pagina="inicio">
   <span>⌂</span>Início
  </button>
  <button data-pagina="treinos">
   <span>▤</span>Treinos
  </button>
  <button data-pagina="evolucao">
   <span>↗</span>Evolução
  </button>
  <button data-pagina="calculos">
   <span>∑</span>Cálculos
  </button>
  <button data-pagina="alunos">
   <span>♙</span>Alunos
  </button>
 </div>
</nav>

</div>

<script>

// =====================================
// MZ FITNESS - SISTEMA PRINCIPAL
// =====================================

const conteudo=document.getElementById("conteudo");

function ler(chave,padrao){
 try{
  return JSON.parse(localStorage.getItem("mz_"+chave)) ?? padrao;
 }catch(e){return padrao;}
}

function salvar(chave,dados){
 localStorage.setItem("mz_"+chave,JSON.stringify(dados));
}

let perfil=ler("perfil",{
 nome:"Atleta MZ",
 peso:83,
 altura:1.70,
 objetivo:"Hipertrofia"
});

let alunos=ler("alunos",[]);
let medidas=ler("medidas",[]);

let fichas=ler("fichas",[
 {
  nome:"TREINO A - PEITO E TRÍCEPS",
  exercicios:"Supino reto; Supino inclinado; Crucifixo; Tríceps corda"
 },
 {
  nome:"TREINO B - COSTAS E BÍCEPS",
  exercicios:"Puxada alta; Remada; Serrote; Rosca direta"
 },
 {
  nome:"TREINO C - PERNAS",
  exercicios:"Agachamento; Leg press; Extensora; Mesa flexora"
 },
 {
  nome:"TREINO D - OMBROS E ABDÔMEN",
  exercicios:"Desenvolvimento; Elevação lateral; Face pull; Prancha"
 }
]);

let biblioteca=ler("biblioteca",[
 "Supino reto",
 "Supino inclinado",
 "Crucifixo",
 "Puxada alta",
 "Remada baixa",
 "Remada curvada",
 "Agachamento",
 "Leg press",
 "Cadeira extensora",
 "Mesa flexora",
 "Desenvolvimento",
 "Elevação lateral",
 "Rosca direta",
 "Tríceps corda",
 "Prancha"
]);

let pagina="inicio";

// =====================================
// NAVEGAÇÃO
// =====================================

document.querySelectorAll("nav button").forEach(botao=>{
 botao.addEventListener("click",()=>{
  pagina=botao.dataset.pagina;

  document.querySelectorAll("nav button").forEach(b=>{
   b.classList.remove("ativo");
  });

  botao.classList.add("ativo");
  renderizar();
 });
});

function ir(p){
 pagina=p;

 document.querySelectorAll("nav button").forEach(b=>{
  b.classList.toggle("ativo",b.dataset.pagina===p);
 });

 renderizar();
}

function titulo(etapa,nome,descricao=""){
 return `
 <div class="etiqueta">${etapa}</div>
 <h1 class="titulo">${nome}</h1>
 ${descricao?`<p class="muted">${descricao}</p>`:""}
 `;
}

// =====================================
// TELA INICIAL
// =====================================

function inicio(){

 return `
 <section class="hero">

  <div class="etiqueta">FORÇA · FOCO · MOVIMENTO</div>

  <h1>Seu ritmo.<br>Seu próximo nível.</h1>

  <p>
   Cada passo conta.
   O seu próximo treino começa aqui.
   Construa sua melhor versão.
  </p>

  <div>
   <button class="btn" onclick="ir('treinos')">
    ACESSAR MEUS TREINOS →
   </button>
  </div>

 </section>

 <div class="cards">

  <div class="card">
   <div class="muted">PESO ATUAL</div>
   <div class="numero">${perfil.peso} kg</div>
   <span class="tag">${perfil.objetivo}</span>
  </div>

  <div class="card">
   <div class="muted">ALUNOS</div>
   <div class="numero">${alunos.length}</div>
   <span class="muted">Cadastrados</span>
  </div>

  <div class="card">
   <div class="muted">FICHAS DE TREINO</div>
   <div class="numero">${fichas.length}</div>
   <span class="muted">Disponíveis</span>
  </div>

  <div class="card">
   <div class="muted">EVOLUÇÃO</div>
   <div class="numero">${medidas.length}</div>
   <span class="muted">Registros realizados</span>
  </div>

 </div>

 <div class="secao">
  <h2>Explore o MZ FITNESS</h2>
 </div>

 <div class="menu-cards">

  <button class="menu-card" onclick="ir('treinos')">
   <div class="icone">🏋️</div>
   <strong>Meus treinos</strong>
   <small>Fichas e exercícios</small>
  </button>

  <button class="menu-card" onclick="ir('evolucao')">
   <div class="icone">📈</div>
   <strong>Minha evolução</strong>
   <small>Peso e medidas</small>
  </button>

  <button class="menu-card" onclick="ir('calculos')">
   <div class="icone">🧮</div>
   <strong>Calculadoras</strong>
   <small>IMC e metabolismo</small>
  </button>

  <button class="menu-card" onclick="ir('alunos')">
   <div class="icone">👥</div>
   <strong>Área de alunos</strong>
   <small>Cadastro e gestão</small>
  </button>

 </div>

 <p class="alerta">
 MZ FITNESS — Treino inteligente.
 </p>
 `;
}

// =====================================
// TREINOS
// =====================================

function telaTreinos(){

 let html=`
 ${titulo("MZ FITNESS / TREINAMENTO","Meus treinos",
 "Organize sua rotina e acompanhe seus exercícios.")}

 <div class="acoes">
  <button class="btn" onclick="novaFicha()">+ Nova ficha</button>
  <button class="btn-sec" onclick="novoExercicio()">+ Exercício</button>
 </div>
 `;

 fichas.forEach((f,i)=>{
  html+=`
  <div class="card">
   <div class="linha">
    <strong>${f.nome}</strong>
    <span class="tag">FICHA ${String.fromCharCode(65+i)}</span>
   </div>

   <p class="muted">${f.exercicios}</p>

   <div class="acoes">
    <button class="btn-sec" onclick="editarFicha(${i})">Editar</button>
    <button class="btn-sec" onclick="excluirFicha(${i})">Excluir</button>
   </div>
  </div>
  `;
 });

 html+=`
 <div class="secao">
  <h2>Biblioteca de exercícios</h2>
 </div>
 <div class="card">
 `;

 biblioteca.forEach(ex=>{
  html+=`
  <div class="linha">
   <div class="exercicio">
    <div class="ex-img">🏋️</div>
    <strong>${ex}</strong>
   </div>
   <span class="tag">EXERCÍCIO</span>
  </div>
  `;
 });

 html+="</div>";

 return html;
}

function novaFicha(){

 let nome=prompt("Nome da nova ficha:");

 if(!nome)return;

 let exercicios=prompt("Digite os exercícios separados por ponto e vírgula:");

 fichas.push({nome,exercicios:exercicios||""});

 salvar("fichas",fichas);
 renderizar();
}

function editarFicha(i){

 let nome=prompt("Nome da ficha:",fichas[i].nome);

 if(nome===null)return;

 let exercicios=prompt("Exercícios:",fichas[i].exercicios);

 fichas[i]={
  nome,
  exercicios:exercicios===null?fichas[i].exercicios:exercicios
 };

 salvar("fichas",fichas);
 renderizar();
}

function excluirFicha(i){

 if(confirm("Deseja excluir esta ficha?")){
  fichas.splice(i,1);
  salvar("fichas",fichas);
  renderizar();
 }
}

function novoExercicio(){

 let nome=prompt("Nome do exercício:");

 if(nome){
  biblioteca.push(nome);
  salvar("biblioteca",biblioteca);
  renderizar();
 }
}

// =====================================
// EVOLUÇÃO
// =====================================

function telaEvolucao(){

 return `
 ${titulo("MZ FITNESS / PROGRESSO","Minha evolução",
 "Acompanhe seu desenvolvimento físico.")}

 <div class="card">

  <h2>Registrar medidas</h2>

  <form id="formMedidas">

   <div class="grade-form">

    <div class="campo">
     <label>Peso (kg)</label>
     <input name="peso" type="number" step=".1" required>
    </div>

    <div class="campo">
     <label>Cintura (cm)</label>
     <input name="cintura" type="number" step=".1">
    </div>

    <div class="campo">
     <label>Peito (cm)</label>
     <input name="peito" type="number" step=".1">
    </div>

    <div class="campo">
     <label>Braço (cm)</label>
     <input name="braco" type="number" step=".1">
    </div>

   </div>

   <button class="btn">SALVAR EVOLUÇÃO</button>

  </form>

 </div>

 <div class="secao">
  <h2>Histórico</h2>
 </div>

 ${medidas.length===0?
 `<div class="vazio">Nenhuma medição registrada.</div>`:
 medidas.slice().reverse().map(m=>`
 <div class="card">
  <div class="linha">
   <strong>${m.peso} kg</strong>
   <span class="muted">${m.data}</span>
  </div>
  <p class="muted">
   Cintura: ${m.cintura||"-"} cm |
   Peito: ${m.peito||"-"} cm |
   Braço: ${m.braco||"-"} cm
  </p>
 </div>
 `).join("")}

 <div class="secao">
  <h2>Perfil do atleta</h2>
 </div>

 <div class="card">
  <form id="formPerfil">

   <div class="campo">
    <label>Nome</label>
    <input name="nome" value="${perfil.nome}" required>
   </div>

   <div class="grade-form">

    <div class="campo">
     <label>Altura (metros)</label>
     <input name="altura" type="number" step=".01"
     value="${perfil.altura}" required>
    </div>

    <div class="campo">
     <label>Objetivo</label>
     <select name="objetivo">
      <option>Hipertrofia</option>
      <option>Emagrecimento</option>
      <option>Condicionamento</option>
     </select>
    </div>

   </div>

   <button class="btn">ATUALIZAR PERFIL</button>

  </form>
 </div>
 `;
}

// =====================================
// CALCULADORAS
// =====================================

function telaCalculos(){

 return `
 ${titulo("MZ FITNESS / FERRAMENTAS","Calculadoras",
 "Ferramentas para acompanhar seus indicadores.")}

 <div class="card">

  <h2>Calculadora de IMC</h2>

  <form id="formIMC">

   <div class="campo">
    <label>Peso em kg</label>
    <input name="peso" type="number" step=".1" min="1" required>
   </div>

   <div class="campo">
    <label>Altura em metros</label>
    <input name="altura" type="number" step=".01" min=".5" max="2.8" required>
   </div>

   <button class="btn">CALCULAR IMC</button>

  </form>

  <div id="resultadoIMC"></div>

  <p class="alerta">
   O IMC é uma referência geral. Ele não diferencia
   massa muscular de gordura e não é um diagnóstico.
  </p>

 </div>

 <div class="card">

  <h2>Metabolismo basal</h2>

  <form id="formBasal">

   <div class="campo">
    <label>Peso (kg)</label>
    <input name="peso" type="number" step=".1" required>
   </div>

   <div class="campo">
    <label>Altura (cm)</label>
    <input name="altura" type="number" required>
   </div>

   <div class="campo">
    <label>Idade</label>
    <input name="idade" type="number" min="15" max="100" required>
   </div>

   <div class="campo">
    <label>Sexo biológico para a fórmula</label>
    <select name="sexo">
     <option value="m">Masculino</option>
     <option value="f">Feminino</option>
    </select>
   </div>

   <button class="btn">CALCULAR METABOLISMO</button>

  </form>

  <div id="resultadoBasal"></div>

  <p class="alerta">
   Estimativa pela equação de Mifflin-St Jeor.
   Não substitui avaliação profissional.
  </p>

 </div>
 `;
}

// =====================================
// ÁREA DE ALUNOS
// =====================================

function telaAlunos(){

 return `
 ${titulo("MZ FITNESS / ADMINISTRAÇÃO","Gestão de alunos",
 "Cadastre e acompanhe os membros.")}

 <div class="card">

  <h2>Novo cadastro</h2>

  <form id="formAluno">

   <div class="campo">
    <label>Nome completo</label>
    <input name="nome" required>
   </div>

   <div class="campo">
    <label>E-mail</label>
    <input name="email" type="email">
   </div>

   <div class="campo">
    <label>Telefone</label>
    <input name="telefone">
   </div>

   <div class="campo">
    <label>Plano</label>
    <select name="plano">
     <option>Mensal</option>
     <option>Trimestral</option>
     <option>Semestral</option>
     <option>Anual</option>
     <option>Experimental</option>
    </select>
   </div>

   <div class="campo">
    <label>Objetivo</label>
    <select name="objetivo">
     <option>Hipertrofia</option>
     <option>Emagrecimento</option>
     <option>Condicionamento</option>
     <option>Saúde e bem-estar</option>
    </select>
   </div>

   <div class="campo">
    <label>Status</label>
    <select name="status">
     <option>Ativo</option>
     <option>Pendente</option>
     <option>Inativo</option>
    </select>
   </div>

   <button class="btn">CADASTRAR ALUNO</button>

  </form>

 </div>

 <div class="secao">
  <h2>Alunos cadastrados (${alunos.length})</h2>
 </div>

 ${alunos.length===0?
 `<div class="vazio">Nenhum aluno cadastrado.</div>`:
 alunos.map((a,i)=>`
 <div class="card">

  <div class="linha">
   <strong>${a.nome}</strong>
   <span class="tag">${a.status}</span>
  </div>

  <p class="muted">
   ${a.email||"Sem e-mail"}<br>
   ${a.telefone||"Sem telefone"}
  </p>

  <div class="linha">
   <span class="muted">${a.plano} · ${a.objetivo}</span>
   <button class="btn-sec" onclick="excluirAluno(${i})">
    Excluir
   </button>
  </div>

 </div>
 `).join("")}

 <p class="alerta">
 Esta versão salva os dados apenas no navegador.
 Para utilização comercial será necessário implementar
 login, banco de dados seguro e controle de permissões.
 </p>
 `;
}

// =====================================
// FORMULÁRIOS E CÁLCULOS
// =====================================

function conectarFormularios(){

 const fm=document.getElementById("formMedidas");

 if(fm){
  fm.onsubmit=e=>{
   e.preventDefault();

   let d=Object.fromEntries(new FormData(fm));

   perfil.peso=Number(d.peso);

   medidas.push({
    ...d,
    data:new Date().toLocaleDateString("pt-BR")
   });

   salvar("perfil",perfil);
   salvar("medidas",medidas);

   renderizar();
  };
 }

 const fp=document.getElementById("formPerfil");

 if(fp){
  fp.onsubmit=e=>{
   e.preventDefault();

   let d=Object.fromEntries(new FormData(fp));

   perfil={...perfil,...d};
   perfil.altura=Number(d.altura);

   salvar("perfil",perfil);
   renderizar();
  };
 }

 const fa=document.getElementById("formAluno");

 if(fa){
  fa.onsubmit=e=>{
   e.preventDefault();

   alunos.push(
    Object.fromEntries(new FormData(fa))
   );

   salvar("alunos",alunos);
   renderizar();
  };
 }

 const fi=document.getElementById("formIMC");

 if(fi){
  fi.onsubmit=e=>{
   e.preventDefault();

   let d=Object.fromEntries(new FormData(fi));

   let imc=Number(d.peso)/(Number(d.altura)**2);

   let classificacao=
    imc<18.5?"Abaixo do peso":
    imc<25?"Faixa considerada adequada":
    imc<30?"Sobrepeso":
    imc<35?"Obesidade grau I":
    imc<40?"Obesidade grau II":
    "Obesidade grau III";

   document.getElementById("resultadoIMC").innerHTML=`
    <div class="resultado">
     <div class="etiqueta">SEU RESULTADO</div>
     <div class="numero">${imc.toFixed(1)}</div>
     <strong>${classificacao}</strong>
    </div>
   `;
  };
 }

 const fb=document.getElementById("formBasal");

 if(fb){
  fb.onsubmit=e=>{
   e.preventDefault();

   let d=Object.fromEntries(new FormData(fb));

   let resultado=
    10*Number(d.peso)+
    6.25*Number(d.altura)-
    5*Number(d.idade)+
    (d.sexo==="m"?5:-161);

   document.getElementById("resultadoBasal").innerHTML=`
    <div class="resultado">
     <div class="etiqueta">METABOLISMO BASAL ESTIMADO</div>
     <div class="numero">${Math.round(resultado)} kcal/dia</div>
    </div>
   `;
  };
 }
}

// =====================================
// EXCLUSÃO DE ALUNOS
// =====================================

function excluirAluno(i){

 if(confirm("Deseja excluir este aluno?")){
  alunos.splice(i,1);
  salvar("alunos",alunos);
  renderizar();
 }
}

// =====================================
// RENDERIZAÇÃO
// =====================================

function renderizar(){

 document.getElementById("avatar").textContent=
 (perfil.nome||"MZ")
 .split(" ")
 .map(x=>x[0])
 .join("")
 .slice(0,2)
 .toUpperCase();

 if(pagina=
