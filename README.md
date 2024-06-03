This is my code is solving the a LeetCode Problem.

<sub>
class Solution:
    def appendCharacters(self, s: str, t: str) -> int:
        # Initialize pointers for s and t
        i, j = 0, 0
        len_s, len_t = len(s), len(t)
        
        # Traverse through s and t
        while i < len_s and j < len_t:
            if s[i] == t[j]:
                j += 1
            i += 1
        
        # The number of characters to be appended is the remaining length of t
        return len_t - j

solution = Solution()
s1, t1 = "coaching", "coding"
s2, t2 = "abcde", "a"
s3, t3 = "z", "abcde"

print(solution.appendCharacters(s1, t1))  # Output: 4
print(solution.appendCharacters(s2, t2))  # Output: 0
print(solution.appendCharacters(s3, t3))  # Output: 5
</sub>
