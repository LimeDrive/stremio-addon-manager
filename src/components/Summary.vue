<template>
  <section id="features">
    <h2>Why?</h2>
    <p>
      Stremio currently doesn't allow users to change the order that their
      installed addons appear on the home screen. As a work around, it is common
      for users to remove and re-install addons in the order they want them to
      appear. This is a tedious and cumbersome process. This addon uses the
      internal Stremio API to manipulate addon order without having to
      add/remove them.
    </p>
    <p>
      This is a <strong>workaround</strong> and not a <strong>solution</strong>.
      It is not recommended to use this tool unless you are comfortable with the
      risks involved.
      <strong>No support or warranty is given.</strong>
    </p>
    <h3>How?</h3>
    <ol>
      <li>Connect your Stremio account. We support 2 different authentication methods:</li>
      <ul>
        <li>Login using your Stremio account (Facebook login is <strong>not supported</strong>)</li>
        <li>Login using an authentication key</li>
        <ul>
          <li>
            Login to
            <a href="https://web.stremio.com/" target="_blank"
              >https://web.stremio.com/</a
            >
            using your Stremio credentials in your browser.
          </li>
          <li>
            Open the developer console <a href="#faq">(?)</a> and paste the
            follow code snippet:
            <div class="code-container">
              <code>JSON.parse(localStorage.getItem("profile")).auth.key</code>
            </div>
          </li>
          <li>Take the output value and paste it into the form below.</li>
        </ul>
      </ul>
      <li>Click 'Load Addons' to load your profiles addons.</li>
      <li>Re-order your addons as you like.</li>
      <li>
        Click the 'Sync To Stremio' button to sync the changes back to your
        profile.
      </li>
    </ol>
  </section>
</template>

<style scoped>
.code-container {
    overflow-x: auto;
    padding: 10px;
    border-radius: 4px;
}

code {
    white-space: nowrap;
    font-family: monospace;
    font-size: 0.9em;
    color: #b93334;
}

@media (max-width: 600px) {
    .code-container {
        padding: 5px;
    }
    code {
        font-size: 0.8em;
    }
}
</style>
