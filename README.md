# Importing the libraries
import os
import csv
import pandas as pd


# Setting the working directory
#Defining the path
working_directory = r"C:\Users\patme\OneDrive\Desktop\Data_Science\Python\data"

# Changing the path to the new path
os.chdir(working_directory)

# Printing the new path for confirmation 
print( "The new working directory is", os.getcwd())



# Now we have a new csv file called ZodiacChallenge.csv. 
# #We are using the csv module
# Let us open the file

def display_zodiac_csv_file():
            with open('ZodiacChallenge.csv') as file:
                        reader = csv.reader(file, delimiter = ',')
                        for row in reader:
                                    print(row)

#Calling the funtion to diplay the content of the csv file
if __name__ == "__main__":
            display_zodiac_csv_file()


# Showing all the items in column 2,
def display_zodiac_csv_file():
    with open('ZodiacChallenge.csv') as file:
         reader = csv.reader(file, delimiter = ',')
         for row in reader:
            print(row[1])

#Calling the funtion to diplay the content of the csv file
if __name__ == "__main__":
            display_zodiac_csv_file()



# Showing all the items in column 1,2, 3 and 4
def display_zodiac_csv_file():
    with open('ZodiacChallenge.csv') as file:
          reader = csv.reader(file, delimiter = ',')
          for row in reader:
            print(row[0], row[1], row[2], row[3])

#Calling the funtion to diplay the content of the csv file
if __name__ == "__main__":
            display_zodiac_csv_file()



# Reading the keys in each rows that I called as a dictionary where the keys are the cloumn headers and the values are the coreesponding values in the rows 

def display_zodiac_csv_file_dictionary():
    with open('ZodiacChallenge.csv') as file:
        dictionaryReader = csv.DictReader(file, delimiter=',')
        for row in dictionaryReader:
            print("Those whose work is " + row["STATUS"] + " with educational level " + row["EDUCATION"] + ", worked as " + row["PROFESSION"] + ", comes from " + row["NATIVE"] + ", and their zodiac is " + row["ZODIAK"])

if __name__ == "__main__":
    display_zodiac_csv_file_dictionary()



# Using the Pandas Library to read the ZodiacChallenge.csv file

def display_zodiac_csv_pandas():
     data = pd.read_csv('ZodiacChallenge.csv', encoding='latin1')
     print(data)
if __name__ == "__main__":
    display_zodiac_csv_pandas()






