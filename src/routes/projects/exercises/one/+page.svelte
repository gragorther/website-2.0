<script lang="ts">
	/**
	 * NALOGA:
	 * 	- Dodaj <input> za vnos števila
	 *  - Definiraj spremenljivko "num" in jo "poveži" z <input> (Nasvet: uporabi bind:value)
	 *  - Če je num sodo, izpiši "Število je sodo", če je liho, izpiši "Število je liho"
	 *
	 * DODATNA NALOGA:
	 *  - Dodaj <button> s tekstom "Random"
	 *  - Po kliku na "Random" naj se num nastavi na naključno število med 1 in 100000000
	 */
  let num: number = $state();
  function isEven(input: number){
    if(input%2==0){
      return "even";
    }
    else{
      return "odd";
    }
  }
</script>

<div class="justiy-center flex flex-col">
	<input type="text" bind:value={num} class="rounded-full text-black p-2" />
	<p>The number is: {isEven(num)}</p>
</div>
