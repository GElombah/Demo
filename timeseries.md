import  pandas


#import pandas
from bokeh.plotting import figure, output_file, show

df = pandas.read_csv("adbe.csv", parse_dates= ["Date"])

p = figure(width=500, height= 250, x_axis_type="datetime", sizing_mode="scale_both")

p.line(df["Date"], df["Close"], color = "Orange", alpha = 0.5)

output_file ("Timeseries.html")

show(p)
