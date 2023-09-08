#note #algorithm 

```python
def merge_OR(postings_1, postings_2):
	result = []
	p1, p2 = 0
	while p1 < len(postings_1) and p2 < len(postings_2):
		if postings_1[p1] == postings_2[p2]:
			result.append(postings_1[p1])
			p1+=1
			p2+=1
		elif postings_1[p1] < postings_2[p2]:
			result.append(postings_1[p1])
			p1+=1
		else:
			result.append(postings_2[p2])
			p2+=1
	return result
```
