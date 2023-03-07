<script>
  const responses = [
    "It is certain.",
    "It is decidedly so.",
    "Without a doubt.",
    "Yes - definitely.",
    "You may rely on it.",
    "As I see it, yes.",
    "Most likely.",
    "Outlook good.",
    "Yes.",
    "Signs point to yes.",
    "Reply hazy, try again.",
    "Ask again later.",
    "Better not tell you now.",
    "Cannot predict now.",
    "Concentrate and ask again.",
    "Don't count on it.",
    "Outlook not so good.",
    "My sources say no.",
    "Very doubtful."
  ];

  let response = "";
  
  function getResponse() {
    const index = Math.floor(Math.random() * responses.length);
    response = responses[index];
  }
</script>

<style>

  .magic-8-ball {
    width: 500px;
    height: 500px;
    border-radius: 50%;
    background-color: black;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    user-select: none;
  }

  .magic-8-ball .inner-ball {
    width: 40%;
    height: 40%;
    border-radius: 50%;
    background-color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 90%;
    font-weight: bold;
    color: black;
		text-align:center;
		font-family: 'Amiri', serif;
  }
</style>

<div class="magic-8-ball" on:click={getResponse}>
  <div class="inner-ball">{response ? response : "?"}</div>
</div>

<svelte:head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Amiri&display=swap">
</svelte:head>