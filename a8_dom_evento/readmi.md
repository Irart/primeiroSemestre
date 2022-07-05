Na homepage (página principal) do seu site, ao carregá-la pelo navegador, usando EVENTO do JavaScript, mostre uma saudação ao usuário com caixa de diálogo, com os seguintes dados na caixa:

*Seu nome completo.

*Cidade/curso – nome da Universidade.

*E, de acordo com a hora do dia, apresente nesta linha: “Bom Dia!”, ou “Boa Tarde!”, 
ou “Boa Noite!”, mais(+) “Hoje é + dia da semana”.


*Cada informação da caixa de diálogo no JavaScript deve estar em uma linha diferente.



<script> 
  const greetingMessage = () => { 
   let h = new Date().toLocaleTimeString('pt-BR', { hour: 'numeric', hour12: false }); 
   let d = new Date().toLocaleDateString('pt-BR', { weekday: 'long' }); 
   if (h <= 5) return 'Boa madrugada, hoje é ' + d; 
   if (h < 12) return 'Bom dia, hoje é ' + d; 
   if (h < 18) return 'Boa tarde, hoje é ' + d; 
   return 'Boa noite, hoje é ' + d; 
  } 
 
  function exibeAlert() { 
   alert((greetingMessage()) + "\n\nSeu Nome\nCidade que mora\nEstudante de Análise e Desenvolvimento pela Mackenzie!"); 
  } 
 </script>
 inserir o alerta 



Colocar o onclick=exibeAlert() no HTML em algum lugar de sua preferência.