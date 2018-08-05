+++
date = "2011-04-29T19:17:00+00:00"
draft = false
tags = ["essay"]
title = "Ruby Exercise 01. 9x9"
+++
<p><pre><code class="ruby">&#13;
total = 0&#13;
storage = 0&#13;
&#13;
print "시작할 숫자를 입력하세요 : "&#13;
smallNum = gets.to_i&#13;
print "마지막 숫자를 입력하세요 : "&#13;
largeNum = gets.to_i&#13;
&#13;
if smallNum &gt; largeNum&#13;
	storage = smallNum&#13;
	smallNum = largeNum&#13;
	largeNum = storage&#13;
end&#13;
&#13;
for i in smallNum..largeNum&#13;
	for j in 1..9&#13;
		print i, " x ", j, " = ", i*j, "\n"&#13;
		total += i*j&#13;
	end&#13;
	print "\n"&#13;
end&#13;
&#13;
print "\n"&#13;
print "총합 : ", total, "\n"&#13;
</code></pre> </p>