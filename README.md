<html lang="en">
	<head>
		<title>Stock Average Calculator</title>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		
		<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
		<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
		<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
		
		
		<script>
		function calculateAverage()
		{
			var first_buy_units = parseInt(document.getElementById("first_buy_units").value);
			var first_buy_price = parseInt(document.getElementById("first_buy_price").value);
			
			var second_buy_units = document.getElementById("second_buy_units").value;
			var second_buy_price = document.getElementById("second_buy_price").value;
			
			//total investment
			var first_investment = first_buy_units * first_buy_price;
			var second_investment = second_buy_units * second_buy_price;
			
			var total_investment = first_investment + second_investment;
			var total_units = parseInt(first_buy_units) + parseInt(second_buy_units);
			
			var average_price = parseFloat(total_investment/total_units);
			
			//set these valus back to input fields
			document.getElementById("first_investment").innerHTML= first_investment;
			document.getElementById("second_investment").innerHTML= second_investment
			document.getElementById("total_units").innerHTML= total_units;
			document.getElementById("average_price").innerHTML= average_price;
			document.getElementById("total_amount_invested").innerHTML= total_investment;

		}
		</script>
	</head>
	<body class="text-center">
		<div class="main_header">Stock Average Calculator</div>
		<form name="stockAverageCalculator">
		<div>
			<p>First Buy</p>
			<div>
				<label>Units</label>
				<input type="text" name="first_buy_units" id="first_buy_units" placeholder="Enter First Buy Units">
			</div>
			<div>
				<label>Price</label>
				<input type="text" name="first_buy_price" id="first_buy_price" placeholder="Enter First Buy Price">
			</div>
		</div>
		
		<div>
			<p>Second Buy</p>
			<div>
				<label>Units</label>
				<input type="text" name="second_buy_units" id="second_buy_units" placeholder="Enter Second Buy Units">
			</div>
			<div>
				<label>Price</label>
				<input type="text" name="second_buy_price" id="second_buy_price" placeholder="Enter Second Buy Price">
			</div>
		</div>
		
		<div class="">
			<p>Total Investment</p>
			<label>First Investment = </label> 	
			<label class="text-success" id="first_investment"></label>
			<br/>
			<label>Second Investment = </label>
			<label class="text-success" id="second_investment"></label>
			<br/>
			<label>Total Units = </label> 
			<label class="text-success" id="total_units"></label>
			<br/>
			<label>Average Price = </label> 
			<label class="text-success" id="average_price"></label>
			<br/>
			<label>Total Amount = </label> 
			<label class="text-success" id="total_amount_invested"></label>
			<br/>
		</div>
		
		
		<div>
			<button type="button" onclick="calculateAverage()">Calculate Average</button>
			<button type="clear">Clear Field</button>
		</div>
		</form>
		<div class="footer">Created by TechRevision.in for learning purpose anyone can reuse free </div>
	</body>
</html>
