<script>
// my pure function from my assignment // 

const jpy1 = 0.01;
const usd1 = 1.38;
const yuan1 = 0.20;
const rupee1 = 0.017;
const euro1 = 1.46;

const foreignCurrencyConverterToCad = function (country, amount) {
  return country * amount;
}

let amount = 0;
let fromCurrency = "";
let toCurrency = "";

const calculateConversion = function () {
  const convertedAmount = foreignCurrencyConverterToCad(fromCurrency,amount) / toCurrency;
  return convertedAmount.toFixed(2);
}
</script>


<!-- created a class tag to wrap everything and use a flex box -->
<div class="container1">

  <!-- title -->
<h1>Currency Converter</h1>

<!-- Amount label and than used the bind value to bind the amount  -->
<label for="amount"> Amount:</label>
<input type="number" id="amount" bind:value={amount}>

<!-- From label and than used the bind value to bind the fromCurrency  -->
<label for="fromCurrency"> From: </label>
<select id="from-currency" bind:value={fromCurrency}>

  <!-- The fromCurrency is the parent component, and the  values below are the childs-->
  <option value="{jpy1}"> JPY</option>
  <option value="{usd1}"> USD</option>
  <option value="{yuan1}"> YUAN</option>
  <option value="{rupee1}"> RUPEE</option>
  <option value="{euro1}"> EURO</option>
</select>



<label for="to-currency"> To:</label>
<select id="to-currency" bind:value={toCurrency}>
  
  <!-- The toCurrency is the parent component, and the values below are the childs-->
<option value= {jpy1}> JPY</option>
<option value= {usd1}> USD</option>
<option value= {yuan1}> YUAN</option>
<option value= {rupee1}> RUPEE</option>
<option value= {euro1}> EURO</option>
</select>


<!-- used a class to give some space between the above forms/inputs and this would provide the end result output-->
<div class="bottom"> Converted Amount: {calculateConversion()}</div>

</div>

<style>

 /* felx box and linear gradient */
.container1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(#ff9a9e, #fad0c4);
}

/* spacing between html elements */
.bottom {
  margin: 30px;
}

/* spacing between html elements */
h1 {
  margin: 50px;
}

/* spacing between html elements */
label {
  margin: 10px;
}

</style>