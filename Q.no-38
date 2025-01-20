class Solution:
    def countAndSay(self, n: int) -> str:
        def rec(n, ans, i):
            if i > n:
                return ans
            elif i == 1:
                return rec(n, "1", i + 1)
            else:
                newAns = ""
                count = 1
                for j in range(1, len(ans)):
                    if ans[j] == ans[j - 1]:
                        count += 1
                    else:
                        newAns += str(count) + ans[j - 1]
                        count = 1
                newAns += str(count) + ans[-1]
                return rec(n, newAns, i + 1)
        return rec(n, "", 1)
