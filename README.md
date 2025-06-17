import matplotlib.pyplot as plt

# Data: Age groups and their percentage of total population
age_groups = ['0-14', '15-24', '25-54', '55-64', '65+']
population_percent = [25, 18, 41, 8, 8]

# Plotting the bar chart
plt.figure(figsize=(15, 9))
bars=plt.bar(age_groups, population_percent, color='blue', edgecolor='pink')

# Title and axis labels
plt.title("India's Population Distribution by Age (2022)", fontsize=12)
plt.xlabel("Age Groups")
plt.ylabel("Percentage of Population")

# Adding percentage labels on top of each bar
for bar in bars:
    value = bar.get_height()
    x=bar.get_x() + bar.get_width()/2
    y=value+0.5
    plt.text(x,y,f'{value}%',ha='center') 

# Grid and layout
plt.grid(axis='y', linestyle='--')
plt.tight_layout()
plt.show()   
