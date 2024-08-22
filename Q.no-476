class Solution:
    def findComplement(self, num: int) -> int:
        def ntb(n):
            b1 = ""
            while n != 0:
                b1 = str(n % 2) + b1 
                n = n // 2
            return b1

        def comp(b):

            comp_b = ""
            for i in b:
                if i == '0':
                    comp_b += '1'
                else:
                    comp_b += '0'
            return comp_b

        def bti(b):
            final = 0

            for i in range(len(b)):
                final += int(b[-(i + 1)]) * (2 ** i)
            return final
        return bti(comp(ntb(num)))
