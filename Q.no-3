class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        l = 0
        longest = 0
        a = set()
        for i in range(len(s)):
            while s[i] in a:
                a.remove(s[l])
                l+=1
            longest = max(longest,(i-l+1))
            a.add(s[i])
        return longest
            
