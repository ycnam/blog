+++
date = "2011-05-15T12:50:27+00:00"
draft = false
tags = ["Ruby", "Exercise", "Function", "ascending sort", "descending sort", "essay"]
title = "Ruby Exercise 04. ascending/descending sort"
+++
<p>오름차순, 내림차순 정렬 실습.</p>&#13;
<pre><code class="ruby">&#13;
$num = Array.new&#13;
&#13;
def input()&#13;
	for i in 0..4&#13;
		print "\n비교를 원하는 수를 5개를 입력하세요. (현재 ", 5-i, "개 남음) : "&#13;
		inp = gets.to_i&#13;
		$num.push(inp)&#13;
	end&#13;
	print "\n입력이 완료되었습니다. 입력된 수는 "&#13;
	for i in 0..4&#13;
		if i == 4&#13;
			print $num[i]&#13;
		else&#13;
			print $num[i], ", "&#13;
		end&#13;
	end&#13;
	puts "입니다."&#13;
end&#13;
&#13;
def ascent(num)&#13;
	ascendingSort = Array.new&#13;
	ascendingSort.push(num[0])&#13;
	for i in 1..num.size-1&#13;
		notBiggest = false&#13;
		for j in 0..i-1&#13;
			if ascendingSort[j] &gt; num[i]&#13;
				ascendingSort.insert(j, num[i])&#13;
				notBiggest = true&#13;
				break&#13;
			end&#13;
		end&#13;
		if notBiggest == false&#13;
			ascendingSort.push(num[i])&#13;
		end&#13;
	end&#13;
	print "\n오름차순 : ", ascendingSort.inspect, "\n"&#13;
end&#13;
&#13;
def descent(num)&#13;
	descendingSort = Array.new&#13;
	descendingSort.push(num[0])&#13;
	for i in 1..num.size-1&#13;
		notSmallest = false&#13;
		for j in 0..i-1&#13;
			if descendingSort[j] &lt; num[i]&#13;
				descendingSort.insert(j, num[i])&#13;
				notSmallest = true&#13;
				break&#13;
			end&#13;
		end&#13;
		if notSmallest == false&#13;
			descendingSort.push(num[i])&#13;
		end&#13;
	end&#13;
	print "내림차순 : ", descendingSort.inspect, "\n\n"&#13;
end&#13;
&#13;
input()&#13;
ascent($num)&#13;
descent($num)&#13;
</code></pre> 