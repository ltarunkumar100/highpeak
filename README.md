def maxProfit(jobs):
    n = len(jobs)
    jobs.sort(key=lambda x: x[1])
    total_profit = 0
    job_count = 0
    end_time = -1
    for i in range(n):
        if jobs[i][0] >= end_time:
            job_count += 1
            end_time = jobs[i][1]
            total_profit += jobs[i][2]
    return (job_count, total_profit)
jobs = [(1300, 1400, 100), (1300, 1500, 150), (1200, 1800, 170)]
print("Tasks and earnings remain")
print(maxProfit(jobs)) 
# input values 
# jobs=3
# values 
# (1300, 1400, 100), (1300, 1500, 150), (1200, 1800, 170)
