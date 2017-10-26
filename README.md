# Keystone Matplotlib Style Sheet
Settings file to configure matplotlib plots to follow keystone template

# Installation Instructions
The file must be uploaded into the stylelib folder in your Matplotlib Configdir, if the stylelib folder does not exist it should be created.

To determine where the Matplotlib Configdir is run the following in the python shell

```
import matplotlib
matplotlib.get_configdir()
```

# Use Instructions

Use the following code to test the style sheet

```
import numpy as np
import matplotlib.pyplot as plt

%matplotlib inline

def plot():
    fig, ax = plt.subplots()
    ax.set_title("Plot Title")
    ax.set_xlabel("x axis")
    ax.set_ylabel("y axis")
    t1 = np.arange(0.1, 5.1, 0.05)
    plt.plot(t1, np.sin(2*np.pi*t1), '-o')
    plt.plot(t1, np.sin(-2*np.pi*t1), '-o')

#Plot using default style
plot()

#Plot using keystone style
plt.style.use('keystone')

plot()
```

![](/images/DefaultPlot.jpg)
![](/images/KeystonePlot.jpg)

More information here: https://matplotlib.org/users/style_sheets.html
