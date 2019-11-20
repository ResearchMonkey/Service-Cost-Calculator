# import required functions
import calendar


# --------------------------- Define user variables --------------------------------------------------------------

# name of the service
service = 'netflix'

# cost in dollars paid each cycle
ser_cost_per_cycle = 14.88

# length of billing cycle
billing_cycle = 30

# date bill is due
due_date = 15

# number of time used in current billing cycle
times_used_cur_cyc = 10

# number of time used per recorded billing cycle
historic_use = {'jan19': 10, 'feb19': 3, 'mar19': 6}

# -------------------------- Define calculable values ------------------------------------------------------------

# current cost of service by times used
'''divides the cost per cycle by the number of times used in the cycle '''
cost_per_use_current_cycle = round(ser_cost_per_cycle / times_used_cur_cyc, 2)

# times used in past cycles
'''adds the historic use values together'''
historic_use_total = 0
for key, value in historic_use.items():
    historic_use_total += value

historic_cost = 0

# total number of time used
'''adds the number of times used this cycle and the historic total'''
times_used_total = times_used_cur_cyc + historic_use_total

# total cost of use over time
'''add the count of times_used_per_each_cycle plus the times_used_cur_cyc divided by ser_cost_per_cycle'''
ser_cost_total = round(ser_cost_per_cycle * times_used_total, 2)

# last cost per trip
last_cost_per_use = ser_cost_per_cycle/(times_used_cur_cyc - 1)

# difference in cost with each use in a current cycle
'''start with LAST COST PER USE and subtract cost_per_use_current_cycle'''
ser_diff_cur_cycle = round(last_cost_per_use - cost_per_use_current_cycle, 2)

# cost of each use over the course of teh service
total_use_cost = round(ser_cost_per_cycle/times_used_total, 2)


print('You pay ${} every {} days for the {}.'.format(ser_cost_per_cycle, billing_cycle, service.title()))
print("Because you used to the {} {} times this cycle each use only cost ${} per use.".format(service.title(), times_used_cur_cyc, cost_per_use_current_cycle))
print("Each use cost ${} less then before this cycle".format(ser_diff_cur_cycle))
print('You have used the {} {} times total, {} in this cycle. '.format(service, times_used_total, times_used_cur_cyc))
print('You have spent ${} on the {}. With each use costing about ${}'.format(ser_cost_total, service.title(), total_use_cost))
# TODO IF you want the service to cost X you need to use it X number of times

# core functions
