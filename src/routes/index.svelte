<script>
    import "../app.css";
    let userAnswer = "";
    let answer = "ls";
    let feedback = "Desktop Downloads Pictures";
</script>

<div class="hero min-h-screen bg-white">
    <div class="hero-content flex-col lg:flex-row-reverse">
        <div class="text-center lg:text-left">
            <h1 class="text-5xl font-bold">Learn terminal the easy way</h1>
            <p class="py-6">
                On lrn.sh you can easily learn how to use Linux terminal with
                interactive exercises and tutorials.
            </p>
        </div>
            <div class="tooltip" data-tip="Check the directory content">
                <div class="mockup-code bg-primary w-96">
                    <pre data-prefix="$"><code
                            ><input bind:value={userAnswer} type="text" /></code
                        > </pre>

                    <pre class="text-warning">
                        {#if userAnswer == answer}
                            <code><p>{feedback}</p></code>
                        {/if}
            </pre>
                </div>
        </div>
    </div>
</div>

<style>
    input[type="text"] {
        background: rgba(255, 255, 255, 0.2);
        color: white;
        border: none;
        outline: none;
    }
</style>
