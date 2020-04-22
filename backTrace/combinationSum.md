## question



## code

```python
class Solution:
    def combinationSum(self, candidates: List[int], target: int) -> List[List[int]]:
        candidates.sort()
        n = len(candidates)
        res = []
        def backtrack(i, tmp_sum, tmp):
            if tmp_sum == target:
                res.append(tmp)
                return
            for j in range(i,n):
                if tmp_sum + candidates[j]> target:
                    break
                backtrack(j,tmp_sum+candidates[j], tmp+[candidates[j]])
        backtrack(0,0,[])

        return res

```


## analysis