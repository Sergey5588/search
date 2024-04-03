# search
search

n = int(input())
mxOst0 = 0
mxOst1 = 0
mx2Ost1 = 0
mxOst2 = 0
mx2Ost2 = 0
for i in range(n):
    x = int(input())

    if mxOst0 < x and x%3==0:
        mxOst0 = x
    elif mxOst1 <= x and x%3==1:
        mx2Ost1 = mxOst1
        mxOst1 = x
    elif mxOst2 <= x and x%3==2:
        mx2Ost2 = mxOst2
        mxOst2 = x
    
    if mx2Ost1 < n and mxOst1 > n:
        mx2Ost1 = n
    if mx2Ost2 < n and mxOst2 > n:
        mx2Ost2 = n
    

sum1 = mxOst0+mxOst1
sum2 = mxOst2+mxOst0
sum11 = mxOst1 + mx2Ost1
sum22 = mx2Ost2 + mxOst2



print(mxOst0, mxOst1,mx2Ost1, mxOst2)
print(sum1,sum2, sum11)
print(max(sum1,sum2, sum11, sum22))
