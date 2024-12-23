# Matplotlib2

## 1 Problem 1 : Matplotlib	Line Chart in Matplotlib	(https://www.geeksforgeeks.org/line-chart-in-matplotlib-python/	)
importing the required libraries
import matplotlib.pyplot as plt
import numpy as np

define data values
x = np.array([1, 2, 3, 4])  # X-axis points
y = x*2  # Y-axis points

plt.plot(x, y)  # Plot the chart
plt.show()  # display
import matplotlib.pyplot as plt
import numpy as np


Define X and Y variable data
x = np.array([1, 2, 3, 4])
y = x*2

plt.plot(x, y)
plt.xlabel("X-axis")  # add X-axis label
plt.ylabel("Y-axis")  # add Y-axis label
plt.title("Any suitable title")  # add title
plt.show()
import matplotlib.pyplot as plt

Sample data
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

Create a line chart
plt.figure(figsize=(8, 6))
plt.plot(x, y, marker='o', linestyle='-')

Add annotations
for i, (xi, yi) in enumerate(zip(x, y)):
    plt.annotate(f'({xi}, {yi})', (xi, yi), textcoords="offset points", xytext=(0, 10), ha='center')

Add title and labels
plt.title('Line Chart with Annotations')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')

Display grid
plt.grid(True)

Show the plot
plt.show()
import matplotlib.pyplot as plt
import numpy as np


x = np.array([1, 2, 3, 4])
y = x*2

plt.plot(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Any suitable title")
plt.show()  # show first chart

The figure() function helps in creating a
new figure that can hold a new chart in it.
plt.figure()
x1 = [2, 4, 6, 8]
y1 = [3, 5, 7, 9]
plt.plot(x1, y1, '-.')

Show another chart with '-' dotted line
plt.show()
import matplotlib.pyplot as plt
import numpy as np

x = np.array([1, 2, 3, 4])
y = x*2

plt.plot(x, y)

x1 = [2, 4, 6, 8]
y1 = [3, 5, 7, 9]

plt.plot(x, y1, '-.')
plt.xlabel("X-axis data")
plt.ylabel("Y-axis data")
plt.title('multiple plots')

plt.fill_between(x, y, y1, color='green', alpha=0.5)
plt.show()



## 2 Problem 2 : Matplotlib	Histogram in Matplotlib	(https://www.geeksforgeeks.org/plotting-histogram-in-python-using-matplotlib/	)
import matplotlib.pyplot as plt
import numpy as np

Generate random data for the histogram
data = np.random.randn(1000)

Plotting a basic histogram
plt.hist(data, bins=30, color='skyblue', edgecolor='black')

Adding labels and title
plt.xlabel('Values')
plt.ylabel('Frequency')
plt.title('Basic Histogram')

Display the plot
plt.show()



## 3 Problem 3 : Matplotlib	Scatterplot in Matplotlib	(	https://www.geeksforgeeks.org/matplotlib-pyplot-scatter-in-python/)
import matplotlib.pyplot as plt
import numpy as np

x = np.array([12, 45, 7, 32, 89, 54, 23, 67, 14, 91])
y = np.array([99, 31, 72, 56, 19, 88, 43, 61, 35, 77])

plt.scatter(x, y)
plt.show()
import matplotlib.pyplot as plt
import numpy as np

x1 = np.array([160, 165, 170, 175, 180, 185, 190, 195, 200, 205])
y1 = np.array([55, 58, 60, 62, 64, 66, 68, 70, 72, 74])

x2 = np.array([150, 155, 160, 165, 170, 175, 180, 195, 200, 205])
y2 = np.array([50, 52, 54, 56, 58, 64, 66, 68, 70, 72])

plt.scatter(x1, y1, color='blue', label='Group 1')
plt.scatter(x2, y2, color='red', label='Group 2')

plt.xlabel('Height (cm)')
plt.ylabel('Weight (kg)')
plt.title('Comparison of Height vs Weight between two groups')

plt.legend()
plt.show()
import matplotlib.pyplot as plt
import numpy as np

x = np.array([3, 12, 9, 20, 5, 18, 22, 11, 27, 16, 8, 24, 15])
y = np.array([95, 55, 63, 77, 89, 50, 41, 70, 58, 83, 61, 52, 68])
plt.scatter(x, y, color='#23d4e8') 

x = np.array([1, 6, 14, 17, 3, 13, 10, 8, 19, 21, 2, 16, 23, 25])
y = np.array([80, 60, 72, 90, 68, 55, 74, 79, 66, 81, 58, 67, 62, 85])
plt.scatter(x, y, color='#32cd68')

plt.show()
import matplotlib.pyplot as plt

Data
x_values = [1, 2, 3, 4, 5]
y_values = [2, 3, 5, 7, 11]
bubble_sizes = [30, 80, 150, 200, 300]

Create a bubble chart with customization
plt.scatter(x_values, y_values, s=bubble_sizes, alpha=0.6, edgecolors='b', linewidths=2)

Add title and axis labels
plt.title("Bubble Chart with Transparency")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")

Display the plot
plt.show()

## 4 Problem 4 : Matplotlib	Pie Chart in Matplotlib	(	https://www.geeksforgeeks.org/plot-a-pie-chart-in-python-using-matplotlib/		)
Import libraries
from matplotlib import pyplot as plt
import numpy as np


Creating dataset
cars = ['AUDI', 'BMW', 'FORD',
        'TESLA', 'JAGUAR', 'MERCEDES']

data = [23, 17, 35, 29, 12, 41]

Creating plot
fig = plt.figure(figsize=(10, 7))
plt.pie(data, labels=cars)

show plot
plt.show()

Import libraries
import numpy as np
import matplotlib.pyplot as plt


Creating dataset
cars = ['AUDI', 'BMW', 'FORD',
        'TESLA', 'JAGUAR', 'MERCEDES']

data = [23, 17, 35, 29, 12, 41]


Creating explode data
explode = (0.1, 0.0, 0.2, 0.3, 0.0, 0.0)

Creating color parameters
colors = ("orange", "cyan", "brown",
          "grey", "indigo", "beige")

Wedge properties
wp = {'linewidth': 1, 'edgecolor': "green"}

Creating autocpt arguments


def func(pct, allvalues):
    absolute = int(pct / 100.*np.sum(allvalues))
    return "{:.1f}%\n({:d} g)".format(pct, absolute)


Creating plot
fig, ax = plt.subplots(figsize=(10, 7))
wedges, texts, autotexts = ax.pie(data,
                                  autopct=lambda pct: func(pct, data),
                                  explode=explode,
                                  labels=cars,
                                  shadow=True,
                                  colors=colors,
                                  startangle=90,
                                  wedgeprops=wp,
                                  textprops=dict(color="magenta"))

Adding legend
ax.legend(wedges, cars,
          title="Cars",
          loc="center left",
          bbox_to_anchor=(1, 0, 0.5, 1))

plt.setp(autotexts, size=8, weight="bold")
ax.set_title("Customizing pie chart")

show plot
plt.show()
Import libraries
from matplotlib import pyplot as plt
import numpy as np


Creating dataset
size = 6
cars = ['AUDI', 'BMW', 'FORD',
        'TESLA', 'JAGUAR', 'MERCEDES']

data = np.array([[23, 16], [17, 23],
                 [35, 11], [29, 33],
                 [12, 27], [41, 42]])

normalizing data to 2 pi
norm = data / np.sum(data)*2 * np.pi

obtaining ordinates of bar edges
left = np.cumsum(np.append(0,
                           norm.flatten()[:-1])).reshape(data.shape)

Creating color scale
cmap = plt.get_cmap("tab20c")
outer_colors = cmap(np.arange(6)*4)
inner_colors = cmap(np.array([1, 2, 5, 6, 9,
                              10, 12, 13, 15,
                              17, 18, 20]))

Creating plot
fig, ax = plt.subplots(figsize=(10, 7),
                       subplot_kw=dict(polar=True))

ax.bar(x=left[:, 0],
       width=norm.sum(axis=1),
       bottom=1-size,
       height=size,
       color=outer_colors,
       edgecolor='w',
       linewidth=1,
       align="edge")

ax.bar(x=left.flatten(),
       width=norm.flatten(),
       bottom=1-2 * size,
       height=size,
       color=inner_colors,
       edgecolor='w',
       linewidth=1,
       align="edge")

ax.set(title="Nested pie chart")
ax.set_axis_off()

show plot
plt.show()
