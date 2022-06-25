<script>
  import { onMount } from "svelte";

  let xterm;
  let terminal;
  let fitXterm;

  onMount(async () => {
    let currentLine = "";
    let entries = [];
    xterm = await import("xterm");
    const { FitAddon } = await import("xterm-addon-fit");
    terminal = new xterm.Terminal();
    fitXterm = new FitAddon();

    terminal.loadAddon(fitXterm);

    terminal.open(document.getElementById("terminal"));

    fitXterm.fit();

    terminal.write("$: ");

    terminal.onKey((e) => {
      if (e.key.charCodeAt(0) === 127) {
        if (currentLine) {
          currentLine = currentLine.slice(0, -1);
          terminal.write("\b \b");
          console.log(currentLine);
        }
      } else if (e.key.charCodeAt(0) === 13) {
      } else {
        currentLine += e.key;
        terminal.write(e.key);
      }
    });
  });
</script>

<div id="terminal" />

<style>
  #terminal {
    margin: 40px;
    height: 100%;
    width: 100%;
    border-radius: 15px;
  }
</style>
