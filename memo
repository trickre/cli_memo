#!/usr/bin/python
#-*- coding: utf-8 -*-

#function make num to same length
#ex) digits_num(3) return 03

def digits_num(num):
	
	return '%02d' %num 

import csv
import datetime

with open('memo.csv','a') as f:
	memo = raw_input('memo:'),

	d = datetime.datetime.today()
	date =(str(d.year)+str(digits_num(d.month))+str(digits_num(d.day)))
	writer = csv.writer(f)
	row = [date,memo[0]]
	writer.writerow(row)

f.close()
