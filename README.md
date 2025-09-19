<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Jokenpô Console</title>
</head>
<body>
  <script>
    let pontos = 0;
    let opcoes = ["pedra", "papel", "tesoura"];
    let continuar = true;

    while (continuar) {
      let escolha = prompt("Escolha: pedra, papel ou tesoura").toLowerCase();
      if (!opcoes.includes(escolha)) {
        alert("Escolha inválida!");
        continue;
      }

      let maquina = opcoes[Math.floor(Math.random() * 3)];
      alert("A máquina escolheu: " + maquina);

      if (escolha === maquina) {
        alert("Empate! Jogue novamente.");
      } 
      else if (
        (escolha === "pedra" && maquina === "tesoura") ||
        (escolha === "papel" && maquina === "pedra") ||
        (escolha === "tesoura" && maquina === "papel")
      ) {
        pontos++;
        alert("Você venceu! Pontos: " + pontos);
      } 
      else {
        alert("Você perdeu! 😢 Pontuação final: " + pontos);
        continuar = false;
      }
    }
  </script>
</body>
</html>
