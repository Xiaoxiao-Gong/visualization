class 4 code notes:

Libraries Used:
NumPy, Matplotlib, Requests, PIL, and io were used.

NumPy for creating data arrays.
Matplotlib for plotting visualizations.
Requests for downloading images from the web.
PIL (from Pillow) for handling image processing.
io for working with binary data streams.
Subplots and Axes:
Created subplots using plt.subplots() to set up the figure and axis. Added new axes using fig.add_axes() to overlay additional elements (e.g., images) on top of existing plots.

Line Plot:
Plotted a line chart to visualize the data using ax.plot(), making it easier to see changes or trends in values. The line color was customized for better visualization.

Error Bars:
Added error bars to the line plot using ax.errorbar().

Error bars were set up using the standard deviation of the data to indicate the variability.
Customized error bars by adjusting attributes like ecolor, elinewidth, capsize, and capthick for better readability and aesthetics.
Used the errorevery parameter to display error bars at specified intervals.
Image from the Internet:
Downloaded an image from the web using requests.get() and handled the binary content using BytesIO(). Opened the image using PIL.Image.open() to prepare it for embedding into the plot.

Embedding an Image:
Added an image to the plot using a new axis (ax_image). Used ax_image.imshow() to display the image and turned off axis labels and ticks using ax_image.axis('off') to keep the visualization clean.

Styling and Layout:
Adjusted figure size with figsize to make the chart and image visually balanced. Positioned the image precisely within the plot by defining coordinates and dimensions for the added axis (add_axes()).

Key Takeaways:

Practiced using multiple libraries for data manipulation, plotting, and image processing.
Created a line plot with error bars to understand data variability, and learned how to customize the appearance of these error bars.
Downloaded and embedded images from the internet into a plot using requests, BytesIO, and PIL, enhancing the storytelling aspect of the visualization.
Learned how to create additional axes in a figure for adding extra content, like images, to support the main plot visually.
Improved skills in customizing plot appearance (e.g., error bars, axis labels, figure size) to make the final output clearer and more informative.
