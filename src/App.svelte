<script>
  let value;
  let result;

  let objValues = {
    one: "value 1",
    two: "value 2",
    dang: "that's delicious"
  };

  $: result = {
    ...objValues
  }[value] || "default";

  const submit = () => {
    console.log("\n", "value:", value, "\n", "result:", result);
  };
</script>

<section>

	<h2>A fresh look at switch statements</h2>
	<p>Type a value in the input</p>
	
	<pre>{JSON.stringify(objValues, null, 2)}</pre>
	
	<input type="text" bind:value />
	<button on:click={()=> submit()}>click</button>
	
	<p>value: {value}</p>
	<p>result: {result}</p>
	
</section>

<style>
	section {
		max-width: 960px;
		margin: 0 auto;
		padding: 0 36px;
	}
</style>