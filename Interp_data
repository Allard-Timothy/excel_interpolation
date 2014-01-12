import scipy.interpolate
import xlrd
import re
from xlrd import open_workbook, cellname
from datetime import datetime, timedelta
import numpy as np
import matplotlib.pyplot as plt


wb = open_workbook('/Users/User_name/Documents/Base_data1.xls')
sh = wb.sheet_by_index(0)   


key_list = sh.col(1)[1:]

time_list = [] 
for item in key_list: 
    datetime_value = datetime(*xlrd.xldate_as_tuple(item.value, 0))
    time_list.append(datetime_value)
   # new_string = re.sub(r'^.+\s(\d+):\d+$', r'\1',str(datetime_value))
    #time_slot = datetime.strptime(new_string, "%Y-%m-%d %H:%M:%S")
    #time_list.append(new_string)

keys = time_list

values = sh.col(2)[1:]

#print values
new_values = []
for log_entry in values:
    log_entry = int(float())
    new_values.append(log_entry)
    #print log_entry

#Log_dict = dict(zip(keys,values))
#print keys
#print values
#print Log_dict

x = keys[:] 
y = new_values[:]

f = scipy.interpolate.interp1d(x,y)
f2 = scipy.interpolate.interp1d(x,y,kind='linear')
xnew = np.linspace(100,100)

plt.plot(x,y)
plt.show()
