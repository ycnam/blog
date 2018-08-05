+++
date = "2011-04-29T19:21:19+00:00"
draft = false
tags = ["essay"]
title = "Ruby Exercise 02. Nx9 (Column style)"
+++
<p><pre><code class="ruby">&#13;
count = 0&#13;
num = 0&#13;
print "\nInput number 1 : "&#13;
num1 = gets.to_i&#13;
print "Input number 2 : "&#13;
num2 = gets.to_i&#13;
print "How many columns do you want? : "&#13;
column = gets.to_i&#13;
print "\n"&#13;
&#13;
if num1 &gt; num2&#13;
	num = num1; num1 = num2; num2 = num&#13;
end&#13;
&#13;
for i in num1..num2&#13;
	if count == column&#13;
		count = 0&#13;
	elsif count != 0&#13;
		count += 1&#13;
		next&#13;
	end&#13;
	for j in 1..9&#13;
		for k in 0..(column-1)&#13;
			if i+k &lt;= num2&#13;
				print i+k, " x ", j, " = ", i*j, "\t"&#13;
			end&#13;
		end&#13;
		print "\n"&#13;
	end&#13;
	print "\n"&#13;
	count += 1&#13;
end&#13;
</code></pre> </p>