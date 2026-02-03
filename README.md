<script>
function sendMessage() {
  const input = document.getElementById("userInput");
  const chatBox = document.getElementById("chatBox");
  const userText = input.value.toLowerCase();

  if (userText === "") return;

  chatBox.innerHTML += `<div class="user">You: ${input.value}</div>`;

  let reply = "Mee rasi, career, love, money gurinchi adugandi 🔮";

  if (userText.includes("rasi")) {
    reply = "Mee rasi gurinchi cheppadaniki mee date of birth cheppandi 🌙";
  } 
  else if (userText.includes("career")) {
    reply = "Career lo meeku tech, business leka government field suit avuthundhi 📈";
  }
  else if (userText.includes("love")) {
    reply = "Love life slow ga start ayi strong ga untundhi ❤️";
  }
  else if (userText.includes("money")) {
    reply = "Money flow gradual ga periguthundhi, savings important 💰";
  }

  chatBox.innerHTML += `<div class="bot">Bot: ${reply}</div>`;
  input.value = "";
  chatBox.scrollTop = chatBox.scrollHeight;
}
</script>
