    T=int(input())
    for test_case in range(1,T+1):
        lst=list(map(str,input().split()))
        sm=0
        mx=0
        mn=1000000
        for i in range(len(lst)):
            sm=0
            for num in lst[i]:
                sm+=int(num)
            mx=max(sm,mx)
            mn=min(sm,mn)
    print(f'#{test_case} {mx} {mn}')