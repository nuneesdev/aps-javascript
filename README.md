# aps-javascript
Esseé um gerador de respostas engraçadas feito como APS da disciplina de JavaScript 2025/1 – Unicarioca.
alert("🤣 Bem-vindo ao Oráculo do Zé! Prepare-se para respostas que não ajudam em nada, mas alegram o dia!");

// Entrada de dados
let nome = prompt("Qual seu nome, curioso?");
let humor = prompt("Como você está se sentindo hoje?");

// Resposta personalizada com humor
if (humor.toLowerCase() === "triste") {
  alert("😢 Não fique assim! O Zé tá aqui pra te fazer rir!");
} else {
  alert("😁 Então vamo rir junto, " + nome + "!");
}

// Array com respostas engraçadas
let respostasEngracadas = [
"Claro que sim... só que não.",
  "Pergunta pro Google!",
  "Eu responderia, mas meu contrato não cobre isso.",
  "Essa pergunta vale um milhão, me paga primeiro!",
  "Resposta em manutenção. Tente novamente nunca.",
  "Sim. Não. Talvez. Vai saber.",
  "A resposta está no seu coração. Literalmente. Vai ao cardiologista!",
  "Se eu tivesse R$1 por resposta engraçada, ainda estaria pobre.",
  "De acordo com estudos que acabei de inventar: sim.",
  "Desculpa, fui abduzido no meio da sua pergunta."
];

// Função que sorteia uma resposta
function gerarResposta(pergunta) {
  let indice = Math.floor(Math.random() * respostasEngracadas.length);
  return respostasEngracadas[indice];
}

// Função que pergunta se o usuário quer continuar
function perguntarNovamente() {
  return prompt("Deseja fazer outra pergunta? (sim/não)").toLowerCase() === "sim";
}

// Loop principal
do {
  let pergunta = prompt("Mande sua pergunta para o Oráculo do Zé:");
  let resposta = gerarResposta(pergunta);
  alert("🔮 O Oráculo diz: " + resposta);
} while (perguntarNovamente());

// Despedida com string manipulada
let despedida = `Até logo, ${nome.toUpperCase()}! Volte quando quiser rir mais!`;
alert(despedida);
