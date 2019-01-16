
<!doctype html>
<html>
<head>
	<script type="text/javascript">
		function validateForm()
		{
			var name = document.getElementById("name");
			if(name.value == "")
			{
				alert("Please enter your name.");
				name.focus();
				return false;
			}
			else
			{
				var regExpName = /^[A-Z][a-z]{2,}\s[A-Z][a-z]+([\s\-][A-Z][a-z]+)*$/;
				if(!regExpName.test(name.value))
				{
					alert("Please enter your name in the correct form. Example: Petar Petrovic.");
					name.focus();
					return false;
				}
			}
			var city = document.getElementById("city");
			if(city.value == "")
			{
				alert("Please enter a city");
				city.focus();
				return false;
			}
			else
			{
				var regExpCity = /^[A-Z][a-z]+(\s[A-Z][a-z]+)*$/;
				if(!regExpCity.test(city.value))
				{
					alert("Please enter a city in a valid form.");
					city.focus();
					return false;
				}
			}
			var zip = document.getElementById("zip");
			if(zip.value == "")
			{
				alert("Please enter your ZIP code.");
				zip.focus();
				return false;
			}
			else
			{
				var regExpZip = /^[1-7][0-9]{4}$/;
				if(!regExpZip.test(zip.value))
				{
					alert("Please enter zip code between 10000-79999.");
					zip.focus();
					return false;
				}
			}
			var address = document.getElementById("address");
			if(address.value == "")
			{
				alert("Please enter your address");
				address.focus();
				return false;
			}
			else
			{
				var regExpAddress = /^[A-Z][a-z]+(\s[A-Z][a-z]+)*\s[1-9][0-9]{0,2}[a-z]?$/;
				if(!regExpAddress.test(address.value))
				{
					alert("Please enter address in the correct form. Example: Milesavska 9a.");
					address.focus();
					return false;
				}
			}
			var birthdate = document.getElementById("birthdate");
			if(birthdate.value == "")
			{
				alert("Please enter your date of birth.");
				birthdate.focus();
				return false;
			}
			else
			{
				var regExpBirthdate = /^((19[0-9][0-9])|(20((0[0-9])|1[0-8])))[\/]((0[1-9])|(1[0-2]))[\/](([0-2][1-9])|(3[01]))$/;
				if(!regExpBirthdate.test(birthdate.value))
				{
					alert("Please enter the date of your flight in the correct yyyy/mm/dd format.");
					birthdate.focus();
					return false;
				}
			}
			var passnum = document.getElementById("passnum");
			if(passnum.value == "")
			{
				alert("Please enter your passport number");
				passnum.focus();
				return false;
			}
			else
			{
				var regExpPassnum = /^[0-9]{3}([A-Za-z0-9]){6}$/
				if(!regExpPassnum.test(passnum.value))
				{
					alert("Please enter your passport number in the correct form. Example: 000xxxxxx.");
					passnum.focus();
					return false;
				}
			}
			var flyingfrom = document.getElementById("flyingfrom");
			if(flyingfrom.value == "")
			{
				alert("Please enter where you are flying from.");
				flyingfrom.focus();
				return false;
			}
			else
			{
				var regExpFlyingfrom = /^[A-Z][a-z]+(\s[A-Z][a-z]+)*$/;
				if(!regExpFlyingfrom.test(flyingfrom.value))
				{
					alert("Please enter where you are flying from in the correct format.");
					flyingfrom.focus();
					return false;
				}
			}
			var destination = document.getElementById("destination");
			if(destination.value == "")
			{
				alert("Please enter where your destination.");
				destination.focus();
				return false;
			}
			else
			{
				var regExpDestination = /^[A-Z][a-z]+(\s[A-Z][a-z]+)*$/;
				if(!regExpDestination.test(destination.value))
				{
					alert("Please enter where your destination in the correct format.");
					destination.focus();
					return false;
				}
			}
			var flightdate = document.getElementById("flightdate");
			if(flightdate.value == "")
			{
				alert("Please enter the date of your flight.");
				flightdate.focus();
				return false;
			}
			else
			{
				var regExpFlightdate = /^20((1[89])|([2-9]{2}))[\/]((0[1-9])|(1[0-2]))[\/](([0-2][1-9])|(3[01]))$/;
				if(!regExpFlightdate.test(flightdate.value))
				{
					alert("Please enter the date of your flight in the correct yyyy/mm/dd form.");
					flightdate.focus();
					return false;
				}
			}
			if(document.getElementById("returnflight").checked)
			{
				if(document.getElementById("returnflightdate").value == "")
				{
					alert("Please enter the date of your return flight.");
					returnflightdate.focus();
					return false;
				}
				else
				{
				var regExpReturnflightdate = /^20((1[89])|([2-9]{2}))[\/]((0[1-9])|(1[12]))[\/](([0-2][1-9])|(3[01]))$/;
				if(!regExpReturnflightdate.test(document.getElementById("returnflightdate").value))
				{
					alert("Please enter the date of your return flight in the correct yyyy/mm/dd form.");
					returnflightdate.focus();
					return false;
				}
				}
			}
			if(document.getElementById("airline").value == "-1")
			{
				alert("Please select an airline company");
				airline.focus()
				return false;
			}
			if(document.getElementById("firstclass").checked && document.getElementById("lunchmenu").value == "-1")
			{
					alert("Please select a lunch menu option");
					lunchmenu.focus();
					return false;
			}
			if(document.getElementById("cctype").value == "-1")
			{
				alert("Please select a credit card type for payment.");
				cctype.focus();
				return false;
			}
			var ccnum = document.getElementById("ccnum");
			if(ccnum.value == "")
			{
				alert("Please enter your credit card number.");
				ccnum.focus();
				return false;
			}
			else
			{
				var regExpCCnum = /^[0-9]{4}[\s\-][0-9]{4}[\s\-][0-9]{4}[\s\-][0-9]{4}$/;
				if(!regExpCCnum.test(ccnum.value))
				{
					alert("Please enter your credit card number in the correct form.");
					ccnum.focus();
					return false;
				}
			}
			var ccseccode = document.getElementById("ccseccode");
			if(ccseccode.value == "")
			{
				alert("Please enter your credit card security ccode.");
				ccseccode.focus();
				return false;
			}
			else
			{
				var regExpCCseccode = /^[0-9]{3}$/;
				if(!regExpCCseccode.test(ccseccode.value))
				{
					alert("Please enter the 3-digit credit card security code");
					ccseccode.focus();
					return false;
				}
			}
			var ccexpdate = document.getElementById("ccexpdate");
			if(ccexpdate.value == "")
			{
				alert("Please enter your credit card's expiry date.");
				ccexpdate.focus();
				return false;
			}
			else
			{
				var regExpCCexpdate = /^((0[1-9])|(1[0-2]))[\/]((1[89])|([2-9][0-9]))$/;
				if(!regExpCCexpdate.test(ccexpdate.value))
				{
					alert("Please enter your credit card's expiry date in the mm/yy form.");
					ccexpdate.focus();
					return false;
				}
			}
		}
		function Checkreturndate()
		{
			if(document.getElementById("returnflight").checked)
			{
				document.getElementById("returnflightdate").disabled = false;
			}
			else
			{
				document.getElementById("returnflightdate").disabled = true;
			}
		}
		function Checkmenu()
		{
			if(document.getElementById("firstclass").checked)
			{
				document.getElementById("lunchmenu").disabled = false;
			}
			else
			{
				document.getElementById("lunchmenu").disabled = true;
			}
		}
		function CheckCC()
		{
			if(document.getElementById("cctype").value == "-1")
			{
				document.getElementById("ccnum").disabled = true;
				document.getElementById("ccseccode").disabled = true;
				document.getElementById("ccexpdate").disabled = true;
			}
			else
			{
				document.getElementById("ccnum").disabled = false;
				document.getElementById("ccseccode").disabled = false;
				document.getElementById("ccexpdate").disabled = false;
			}
		}
	</script>
</head>
<header>

</header>
<body>
	<form name="daform" id="daform" action="/action.php" method="POST" onsubmit="return validateForm()">
		<table cellspacing="2" cellpadding="2" border="1">
			<tr>
				<th colspan="2">Passenger details.</th>
			</tr>
			<tr>
				<td>Name</td>
				<td><input type="text" id="name"></td>
			</tr>
			<tr>
				<td>City</td>
				<td><input type="text" id="city"></td>
			</tr>
			<tr>
				<td>ZIP</td>
				<td><input type="text" id="zip"></td>
			</tr>
			<tr>
				<td>Address</td>
				<td><input type="text" id="address"></td>
			</tr>
			<tr>
				<td>Date of Birth</td>
				<td><input type="text" id="birthdate"></td>
			</tr>
			<tr>
				<td>Passport Number</td>
				<td><input type="text" id="passnum"></td>
			</tr>
			<tr>
				<th colspan="2">Fllight details.</th>
			</tr>
			<tr>
				<td>Flying from.</td>
				<td><input type="text" id="flyingfrom"></td>
			</tr>
			<tr>
				<td>Destination</td>
				<td><input type="text" id="destination"></td>
			</tr>
			<tr>
				<td>Flight Date</td>
				<td><input type="text" id="flightdate"></td>
			</tr>
			<tr>
				<td>Return Flight</td>
				<td><input type="checkbox" id="returnflight" onchange="Checkreturndate()">Yes</td>
			</tr>
			<tr>
				<td>Return Flight Date</td>
				<td><input type="text" id="returnflightdate" disabled></td>
			</tr>
			<tr>
				<td>Airline Company</td>
				<td>
					<select id="airline">
						<option value="-1"></option>
						<option value="1">AirSerbia</option>
						<option value="2">Lufthansa</option>
						<option value="3">British Airways</option>
					</select>
				</td>
			</tr>
			<tr>
				<td>First Class</td>
				<td><input type="checkbox" id="firstclass" onchange="Checkmenu()">Yes</td>
			</tr>
			<tr>
				<td>Lunch Menu</td>
				<td>
					<select id="lunchmenu" disabled>
						<option value="-1"></option>
						<option value="1">Vegetarian</option>
						<option value="2">Meat</option>
						<option value="3">Fish</option>
					</select>
				</td>
			</tr>
			<tr>
				<th colspan="2">Payment	details.</th>
			</tr>
			<tr>
				<td>Credit Card Type</td>
				<td>
					<select id="cctype" onchange="CheckCC()">
						<option value="-1" selected></option>
						<option value="1">Visa</option>
						<option value="2">Master</option>
						<option value="3">American Express</option>
					</select>
				</td>
			</tr>
			<tr>
				<td>Credit Card Number</td>
				<td><input type="text" id="ccnum" disabled></td>
			</tr>
			<tr>
				<td>Credit Card Security code</td>
				<td><input type="text" id="ccseccode" disabled></td>
			</tr>
			<tr>
				<td>Credit Card Expiry Date</td>
				<td><input type="text" id="ccexpdate" disabled></td>
			</tr>
			<tr>
				<td>Submit form</td>
				<td><input type="submit" value="submit form"></td>
			</tr>
			<tr>
				<td>Reset form</td>
				<td><input type="reset" value="reset form"></td>
			</tr>
		</table>
	</form>
</body>
<footer>

</footer>
</html>
