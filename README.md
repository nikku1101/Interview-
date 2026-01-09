# Interview-
data science
# Interview-
//data science
//1. Problem

def merge_intervals(intervals):
if not intervals:
return[]

intervals.sort(Key=lambda x:x[0])
merged=[]
current_interval=intervals[0]
merged.append(current_interval)

for next_interval in intervals[1:]:
current_start,current_end=merged[-1]
,next_start,next_end=next_interval

if next_start<=current_end:
merged[-1][1]=max(current_end,next_end)
else:
merged.append(next_intervals)

return merged

input_intervals=[[1,3],[2,6],[8,10],[15,18]]
result=merge_intervals(input_intervals)

for interval in result:
print(f"{interval[0]}{interval[1]}")


//2. Problem

import sys
def solve():
input_data=sys.stdin.read().split()
if not input_data:
return

n=int(input_data[0])
arr=list(map(int,input_data[1:n+1]))
k=int(input_data[n+1])

if k>n:
return


current_sum=sum(arr[:k])
max_sum=current_sum

for i in range(k,n):
current_sum=current_sum+arr[i]-arr[i-k]
if current_sum>max_sum:
max_sum=current_sum


print(max_sum)

if __name__=="__main__":
solve()


//3.problem

import sys
def longest_valid_segment(s):
char_map={}
max_length=0
start=0

for end in range(len(s)):
if s[end] in char_map and char_map[s[end]]>=start:
start=char_map[s[end]]+1

char_map[s[end]]=end
max_length=max(max_length,end-start +1)
return max_length

if __name__=="__main__":
input_data=sys.stdin.read().strip()
result=longest_unique_segment(input_data)
print(result)
