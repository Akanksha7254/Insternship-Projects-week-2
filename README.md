# Insternship-Projects-week-2
# A Unit Converter application in Python.

📌 In this project, I created a GUI-based Unit Converter with different conversion factors

🧐 Here's a quick breakdown of the code:
- Prompt the user to enter a value and select the source and target units for conversion.
- Perform the conversion and display the result.
- Implement error handling to handle invalid inputs (e.g., non-numeric values, unsupported units).


Tkinter is the most commonly used method for performing GUI applications.It is a standard Python interface to the Tk GUI toolkit shipped with Python
 Python with tkinter is the fastest and easiest way to create the GUI applications. Creating a GUI using tkinter is an easy task.
 To create a tkinter app: Importing the module – tkinter

There are two main methods used which the user needs to remember while creating the Python application with GUI.

Tk(screenName=None,  baseName=None,  className=’Tk’,  useTk=1):

To create a main window, tkinter offers a method ‘Tk(screenName=None,  baseName=None,  className=’Tk’,  useTk=1)’. To change the name of the window, you can change the className to the desired one.

The basic code used to create the main window of the application is:

m=tkinter.Tk() # where m is the name of the main window object

mainloop():

There is a method known by the name mainloop() is used when your application is ready to run. mainloop() is an infinite loop used to run the application, wait for an event to occur and process the event as long as the window is not closed.

m.mainloop()

# Importing tkinter modules

      import tkinter as tk

  # Function to perform unit conversion
  The def keyword is used to create, (or define) a function

      def convert_units(): 
   # user input
          try:
           value=float(input_entry.get())  
           from_unit = from_unit_var.get()
           to_unit = to_unit_var.get()
       

        
  # defining conversion factors

        conversion_factors={
            "Meters to Feet" : 3.28084,     
            "Meters to Inches" : 39.3701,
            "Feet to Meters" : 0.3048,
            "Feet to Inches" : 12,
            "Inches to Meters" : 0.0254,
            "Inches tO Feet" : 0.0833
            }
        result = value * conversion_factors[f"{from_unit} to {to_unit}"]
        result_label.config(text=f"Result: {result:.2f} {to_unit}")
    except ValueError:
        result_label.config(text="Invalid input. Please enter a number.")

# create the main window,where root is the name of the main window object.
After importing, setup the application object by calling the Tk() function. This will create a top-level window (root) having a frame with a title bar, control box with the minimize and close buttons, and a client area to hold other widgets.


      root = tk.Tk() 
      root.title("Unit Converter")

 # set window size and background color
 The geometry() method defines the width, height and coordinates of the top left corner of the frame as below (all values are in pixels): window.geometry("widthxheight+XPOS+YPOS")

 
      root.geometry("750x750")
      root.configure(bg="lightblue")

 # create and configure widgets and set background color.
 LABEL WIDGET:
 A label can be created in the UI in Python using the Label class. The Label constructor requires the top-level window object and options parameters.
   text : caption of the button
   bg : background colour
   fg : foreground colour
   font : font name and size
   image : to be displayed instead of text
   command : function to be called when clicked
 
ENTRY WIDGET:

This widget renders a single-line text box for accepting the user input. For multi-line text input use the Text widget. Apart from the properties already mentioned, the Entry class constructor accepts the following:

bd : border size of the text box; default is 2 pixels.
show : to convert the text box into a password field, set show property to "*".
The following code adds the text field.

txtfld=Entry(window, text="This is Entry Widget", bg='black',fg='white', bd=5)



         input_label = tk.Label(root,text="Enter Value:", bg="lightblue")  
         input_label.grid(row=0, column=0,padx=10, pady=5)
         input_entry = tk.Entry(root)
         input_entry.grid(row=0, column=1, padx=10, pady=50)

         from_unit_var = tk.StringVar()
         from_unit_var.set("Meters")
         from_unit_label = tk.Label(root, text="From Unit:", bg="lightblue")
         from_unit_label.grid(row=1, column=0, padx=10, pady=50)
         from_unit_menu = tk. OptionMenu(root, from_unit_var,"Meters", "Feet", "Inches")
         from_unit_menu.grid(row=1, column=1, padx=10, pady=50)

         to_unit_var = tk.StringVar()
         to_unit_var.set("Feet")
         to_unit_label = tk.Label(root, text="To Unit:", bg="lightblue")
         to_unit_label.grid(row=2, column=0, padx=10, pady=5)
         to_unit_menu = tk. OptionMenu(root, to_unit_var,"Meters", "Feet", "Inches")
         to_unit_menu.grid(row=2, column=1, padx=10, pady=50)

         convert_button = tk.Button(root, text="convert",command=convert_units, bg="green", fg="white")
         convert_button.grid(row=3, column=0, columnspan=2, padx=10, pady=5)
         result_label = tk.Label(root, text="Result:", bg="lightblue")
         result_label.grid(row=4, column=0, columnspan=2, padx=10, pady=5)

 



# start the main loop


    root.mainloop()


# OUTPUT
 
![Screenshot 2023-10-18 212959](https://github.com/Akanksha7254/Insternship-Projects-week-2/assets/146561059/ee7e50f7-8516-4bc1-8353-2fcff4d21474)
![Screenshot 2023-10-18 213349](https://github.com/Akanksha7254/Insternship-Projects-week-2/assets/146561059/034f986b-1231-46a7-ab02-a2d823355af7)

