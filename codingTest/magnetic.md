    def count(arr):
        result=0
        for lst in arr:
            cnt=0
            for i in range(len(arr)):
                if lst[i]==1:
                    cnt+=1
                if lst[i]==2:
                    cnt+=2
                if cnt==3:
                    cnt=0
                result+=1
    return result

    T=10
    for test_case in range(1,T+1):
        N=int(input())
        arr=[list(map(int, input().split())) for _ in range(N)]
        arr_t=list(map(list,zip(*arr)))
        ans = count(arr_t)
    print(f'#{test_case} {ans}')
