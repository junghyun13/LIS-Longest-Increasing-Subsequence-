# LIS-Longest-Increasing-Subsequence-
# c 
첫째줄에 수열의 크기 둘째줄에 수열의 있는 값을 입력하고 주어진수열에서 가장 긴 증가하는 부분 수열의 길이를 구하는 프로그램을 작성해보자!

-LIS의 개념은 단어 그대로 가장 긴 증가하는 부분 수열을 구하는 것이다. 
-어떠한 수열이 주어질 때, 그 수열에서 일부 원소를 뽑아내어 새로 만든 수열을 '부분 수열'이라고 하고 이 수열이 오름차순을 유지하면 '증가하는 부분 수열'이 되는 것이다. 
-그러므로 어떤 수열에서 만들 수 있는 부분 수열 중에서 가장 길면서 오름차순을 유지하는 수열이 LIS이다.

DP (Dynamic Programming) 알고리즘을 이용해보자!


#include <stdio.h>
#include <stdlib.h> 


void main(){
	int n,max,i,j;
	int dp[1000]={0, };
	int sequence[1000]={0, };
	scanf("%d",&n);
	max=0;
	for(i=1;i<=n;i++){
		scanf("%d",&sequence[i]);
		for(j=0;j<i;j++){
			if(sequence[i]>sequence[j]){
				if(dp[j]+1 > dp[i]){
					dp[i]=dp[j]+1;
					if(max < dp[i]){
						max=dp[i];}}} }
	printf("%d",max); }
