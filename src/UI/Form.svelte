<script>
  export let title = "";
  export let titleColor = "";
  export let buttonColor = "";
  export let buttonText = "";
  export let buttonTextColor = "";
</script>

<div>
  {#if title}
    <h3 style="color:{titleColor};">{title}</h3>
  {/if}
  <form>
    <input type="text" placeholder="Enter name..." />
    <input type="email" placeholder="Enter email..." />
    <input type="tel" placeholder="Enter phone..." />
    <p for="contact-type">I am a:</p>
    <div>
      <input
        type="radio"
        name="contact-type"
        value="Physician"
        id="physician" />
      <label for="contact-type">Physician</label>
    </div>
    <div>
      <input
        type="radio"
        name="contact-type"
        value="Care Provider"
        id="provider" />
      <label for="contact-type">Care Provider</label>
    </div>
    <div>
      <input type="radio" name="contact-type" value="Patient" id="patient" />
      <label for="contact-type">Patient</label>
    </div>
    <textarea placeholder="Enter message..." />
    <button
      style="background:{buttonColor};color:{buttonTextColor};">{buttonText}</button>
  </form>
</div>

<style>
  h3 {
    margin: 1em;
    text-align: center;
  }
  form {
    display: flex;
    flex-direction: column;
    width: 500px;
    margin: 0 auto 4em;
    padding: 2em;
    background: linear-gradient(to top, #c80007, gold);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.24);
    color: white;
    font-weight: bold;
  }
  input,
  textarea,
  button {
    margin: 0.5em 0;
    padding: 1em;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.24);
    border: none;
    outline: none;
  }
  textarea {
    margin-top: 1em;
    min-height: 8em;
  }
  button {
    box-sizing: border-box;
    outline: none;
    border: none;
    font-weight: bold;
  }
  form div {
    display: flex;
    align-items: center;
    margin-left: 1em;
  }
  label {
    padding-left: 1em;
  }
  form p {
    margin-top: 1em;
    margin-bottom: 0.25em;
  }
</style>
