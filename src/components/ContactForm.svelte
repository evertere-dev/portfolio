<script>
  let status = "";
  const handleSubmit = async data => {
    status = 'sending...'
    const formData = new FormData(data.currentTarget)
    const object = Object.fromEntries(formData);
    const json = JSON.stringify(object);
  
    const response = await fetch("https://api.web3forms.com/submit", {
        method: "POST",
        headers: {
            "Content-Type": "application/json",
            Accept: "application/json",
        },
        body: json
    });
    const result = await response.json();
    if (result.success) {
        status = result.message || "Success"
    }
  }
  </script>

<form id="contactform" on:submit|preventDefault={handleSubmit}>
  <h1>contact</h1>
  <input type="hidden" name="access_key" value="2b501a73-1115-46f0-ac09-cb0f25cecc5c">
  <div class="col-wrap">
    <input type="text" placeholder="name" name="name" id="name" required>
    <input type="email" placeholder="email" name="email" id="email" required>
  </div>
  <div class="col-wrap">
    <input type="text" placeholder="subject" name="subject" id="subject" required>
  </div>
  <textarea placeholder="your request" name="text" id="text" required></textarea>
  <input type="submit" value="send">
</form>

<div>{status}</div>

<style>
  #contactform {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 87%;
    max-width: 640px;
    padding: 18px 25px;
    border-radius: 18px;
    background: #111111;
    border: 2px solid #555555;
  }

  #contactform > h1 {
    color: #fff;
  }

  .col-wrap {
    display: flex;
    flex-direction: column;
    padding: 0 0 10px;
    gap: 10px;
  }

  @media screen and (min-width: 840px) {

    .col-wrap {
      flex-direction: row;
      padding: 0 0 15px;
      gap: 0;
      justify-content: space-between;
    }

    .col-wrap > * {
    width: 48.83%;
  }

  }
</style>