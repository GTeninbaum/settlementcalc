<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">

<html>
<head>
<title>Settlement Scenario</title>
</head>
<body>

<form name="Trump" method=post>
<table border=1>
<tr>
<td><div align=center>Total Settlement($):</div></td>
<td><div align=center>Attorney's Fee(%):</div></td>
<td><div align=center>Case Expenses($):</div></td>
<td><div align=center>Total Liens($):</div></td>
<td><div align=center>Net to Client($):</div></td>

</tr>
<tr>
<td><input type=text name="Gross" size=10 onFocus="this.form.Gross.value=''"></td>
<td><input type=text name="Fees" size=10 onFocus="this.form.Fees.value=''"></td>
<td><input type=text name="Expenses" size=10 ></td>
<td><input type=text name="Lien" size=10 ></td>
<td><input type=text name="Net" size=10 disabled=disabled ></td>
</tr>
<tr>
<td><div align=center>Increment ($)</div></td>
<td><input type=text name="Increment" size=10 ></td>
</td>
<tr>
<td><input type=text name="Gross1" size=10 disabled=disabled td>
<td><input type=text name="Fees1" size=10 disabled=disabled></td>
<td><input type=text name="Expenses1" disabled=disabled ></td>
<td><input type=text name="Lien1" disabled=disabled ></td>
<td><input type=text name="Net1" size=10 disabled=disabled ></td>
</tr>

<tr>
<td><input type=text name="Gross2" size=10 disabled=disabled td>
<td><input type=text name="Fees2" size=10 disabled=disabled></td>
<td><input type=text name="Expenses2" disabled=disabled ></td>
<td><input type=text name="Lien2" disabled=disabled ></td>
<td><input type=text name="Net2" size=10 disabled=disabled ></td>
</tr>
<tr>
<td><input type=text name="Gross3" size=10 disabled=disabled td>
<td><input type=text name="Fees3" size=10 disabled=disabled></td>
<td><input type=text name="Expenses3" disabled=disabled ></td>
<td><input type=text name="Lien3" disabled=disabled ></td>
<td><input type=text name="Net3" size=10 disabled=disabled ></td>
</tr>

<tr>
<td><input type=text name="Gross4" size=10 disabled=disabled td>
<td><input type=text name="Fees4" size=10 disabled=disabled></td>
<td><input type=text name="Expenses4" disabled=disabled ></td>
<td><input type=text name="Lien4" disabled=disabled ></td>
<td><input type=text name="Net4" size=10 disabled=disabled ></td>
</tr>
<p>
<input type="button" value="Let's see" onClick="computeform(this.form)">
<input type="reset"  value="Reset" onClick="ClearForm(this.form)">
</form>

<script type="text/javascript">

function ClearForm(form){

    form.Gross.value = "";
    form.Fees.value = "";
    form.Expenses.value = "";
    form.Lien.value = "";
	form.Net.value = "";

}

function checkform(form) {

       if (form.Gross.value==null||form.Gross.value.length==0){
            alert("\nPlease complete the form first");
            return false;
       }
       return true;

}

function computeform(form) {

       if (checkform(form)) {

       yourNet=form.Gross.value-(form.Gross.value*form.Fees.value/100)-form.Expenses.value-form.Lien.value
       form.Net.value=yourNet; 
	   
	   form.Gross1.value=1*form.Gross.value+1*form.Increment.value
       yourNet1=form.Gross1.value-(form.Gross1.value*form.Fees.value/100)-form.Expenses.value-form.Lien.value
       form.Net1.value=yourNet1;
	   
	   form.Gross2.value=1*form.Gross.value+1*form.Increment.value+1*form.Increment.value
	   yourNet2=form.Gross2.value-(form.Gross2.value*form.Fees.value/100)-form.Expenses.value-form.Lien.value
       form.Net2.value=yourNet2;
	   
	   form.Gross3.value=1*form.Gross.value+1*form.Increment.value+1*form.Increment.value+1*form.Increment.value
       yourNet3=form.Gross1.value-(form.Gross1.value*form.Fees.value/100)-form.Expenses.value-form.Lien.value
       form.Net3.value=yourNet3;
	   
	   form.Gross4.value=1*form.Gross.value+1*form.Increment.value+1*form.Increment.value+1*form.Increment.value+1*form.Increment.value
	   yourNet4=form.Gross2.value-(form.Gross3.value*form.Fees.value/100)-form.Expenses.value-form.Lien.value
       form.Net4.value=yourNet4;
	   }
       return;
}
 
</script>
</body>
</html>

                                          
