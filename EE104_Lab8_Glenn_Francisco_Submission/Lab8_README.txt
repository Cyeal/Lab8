Name: Glenn Francisco
ID:   014953380
Date: 05-7-2023
EE104
============================================================================================================================================================
YouTube Links: 
OpenAI File Q&A: https://youtu.be/ixcMeMQpy1c
OpenAI Web Crawl Q&A: https://youtu.be/9QZb43DPiH0
Simple Traffic Controller: Part 2, Hardware: 

============================================================================================================================================================
Github Link for ALL: 

============================================================================================================================================================
References: 
OpenAI Quickstart tutorial: https://platform.openai.com/docs/quickstart
OpenAI API reference: https://platform.openai.com/docs/api-reference/introduction
Pinecone website: https://www.pinecone.io/
Pinecone API documentation: https://docs.pinecone.io/
GitHub repository for the OpenAI Cookbook: https://github.com/openai/openai-cookbook
Node.js website: https://nodejs.org/en/
npm website: https://www.npmjs.com/
Next.js website: https://nextjs.org/
Flask website: https://flask.palletsprojects.com/en/2.1.x/
Python documentation: https://docs.python.org/3/
Official Python bindings for OpenAI: https://pypi.org/project/openai/
WebCrawlQ&A: https://github.com/openai/openai-cookbook/tree/main/apps/web-crawl-q-and-a
One Piece: https://en.wikipedia.org/wiki/One_Piece
============================================================================================================================================================
OpenAI File Q&A

Description: 
OpenAI File Q&A is a client-server front-end application that uses OpenAI chatbot to answer questions related to the files stored in a specific 
directory. The application requires users to upload files to the server, and the chatbot will use the contents of those files to provide answers 
to user queries. The application is designed to be user-friendly and can be easily set up with the help of the instructions provided below.
The file outlines the necessary steps and prerequisites to set up a web server to host the ChatGPT service that can answer questions 
related to files that are uploaded to the web server. The following are the steps:

1) Pre-requisites: Install Python (version between 7 and 10) and set up an OpenAI API key by visiting the API Keys page to retrieve the key.
Also, set up a Pinecone API key and index name by creating an account and index.

Example:
OPENAI_API_KEY = "YOUR_OPENAI_API_KEY"
YOUR OPENAI ORG KEY = "YOUR_PINECONE_API_KEY"
PINECONE_API_KEY="YOUR_PINECONE_API_KEY"
PINECONE_ENV="Your_environment"

2) Trial run on Google Colab to validate Pinecone account is working properly by running a Google Colab notebook that has already been created for 
this purpose.

3) Download the source code by going to the openai-cookbook GitHub repository and downloading the openai-cookbook-main.zip file.

4) Store your OPEN_API_KEY in the .env file that you need to create in the directory where you will run the application. You will use Notepad++ or 
any text editor that allows you to save in the format ".env" to create the file. 

5) Once you have created the .env file, you can verify that it is working properly by running the application and checking that the environment 
variables are being read correctly. You can do this by opening a command prompt or terminal in the directory where you saved the application 
and running the command: python app.py

If the application starts without errors and you see messages in the console indicating that the environment variables have been read, then everything
should be working correctly.

Inputted the statement $env:OPENAI_API_KEY = "OPENAI_API_KEY" into the Powershell Prompt in order to tell the program that this was the OPENAI API Key.
============================================================================================================================================================
OpenAI Web Crawl Q&A

Description: OpenAI Web Crawl Q&A is a virtual chat bot that uses the information from the files scraped from a website to answer questions related 
to that website. This application is designed to guide users to the correct information they are looking for on a website. It is a client-server 
front-end application that uses the OpenAI API to provide accurate and relevant responses to users' questions. To use the application, you need to 
download the source code from the OpenAI Cookbook GitHub repository and follow the instructions provided in the README file to set up the necessary 
prerequisites and run the application. 

Prerequisite: 
Walk through the quickstart tutorial
https://platform.openai.com/docs/quickstart
In this step, you should install Python with a version between version 7 to version 10. Note that this tutorial assumes you have basic knowledge 
of Python programming, including how to install Python packages using pip.

Set up an OpenAI API key:
https://platform.openai.com/docs/api-reference/introduction

a. Open a PowerShell window (as an administrator if you can). You will see the PS C:> prompt.

b. Install the official Python bindings by running the following command:
PS C:> pip install openai

c. Visit your API Keys page to retrieve the API key you'll use in your requests. 
NOTE: Remember that your API key is a secret! Do not share it with others or expose it in any client-side code (browsers, apps).
https://platform.openai.com/account/api-keys

d. Create a folder for this project, and name it "web-crawl-q-and-a" using the Linux command "md" (make directory):
PS C:>md web-crawl-q-and-a

e. Use the "cd" (change directory) to go inside the directory:
PS C:> cd .\web-crawl-q-and-a

f. Create a ".env" file using Notepad++ or any text editor that allows you to save in the format ".env" and type this line below, then 
save the file as "all type" with file name ".env":
OPENAI_API_KEY = "YOUR_OPENAI_API_KEY"

Where to download the code: 
https://github.com/openai/openai-cookbook/tree/main/apps/web-crawl-q-and-a


PREPARE THE ENVIRONMENT:

Open PowerShell and navigate to the directory where you cloned the code.
PS C:> cd .\web-crawl-q-and-a\

Create a virtual environment:
PS C:\web-crawl-q-and-a> python install virtualenv (or c:\python310\Python install virtualenv if you have to use the absolute path)
PS C:\web-crawl-q-and-a> python -m venv env

Activate the virtual environment:
PS C:\web-crawl-q-and-a> .\env\Scripts\activate

Note: If you do not get the (env) prompt shown as (env) PS C:\web-crawl-q-and-a>, you need to run the command below in the PowerShell window:
PS C:\OpenAI\web-crawl-q-and-a> Get-ExecutionPolicy -List
PS C:\OpenAI\web-crawl-q-and-a> Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser
PS C:\OpenAI\web-crawl-q-and-a> Get-ExecutionPolicy -List

Now that you have successfully set up the environment. Run the application: 
PS C:\web-crawl-q-and-a> pip install -r requirements.txt
PS C:\web-crawl-q-and-a> python web-qa.py

1) Install necessary packages:
tiktoken
pandas
openai
python-dotenv
bs4 (BeautifulSoup)
matplotlib
plotly
scipy
sklearn

2) Import all the necessary libraries by copying the provided code into the web-qa.py file.

3) Modify the crawl(url) function so that it will not stop if a file does not exist.

4) Build the CSV file by running the web-qa.py file:

5) Run the command python web-qa.py in the terminal.
This will crawl the website and build the CSV file. It will take some time to complete.
After the CSV file is built, you can start querying information from the website.
Use the Q&A system by modifying the code in Step 13 of the web-qa.py file:

Example:
print(answer_question(df, question="Where is SJSU?", debug=False))
print(answer_question(df, question="Information about the Welcome Center?"))
print(answer_question(df, question="What is EE104?"))
while (True):
prompt = input("\nEnter your question: \n")
print(answer_question(df, question=prompt))
Improve productivity by using the vector database solution (optional):

This will start the Flask application on http://localhost:5000/.
You can now access the web application from a web browser or through the Powershell Prompt.The web page should have an input field and a button. 
Enter a question in the input field and click on the button. The application will search for the answer to the question on your website and 
return the answer.
Inputted the statement $env:OPENAI_API_KEY = "OPENAI_API_KEY" into the Powershell Prompt in order to tell the program that this was the OPENAI API Key.
============================================================================================================================================================
Simple Traffic Controller: Part 2, Hardware

Description: In Simple Traffic Controller: Part 2 – Hardware, the task is to replace the previously implemented Finite State Machine 
using flip flops with a software Finite State Machine. The traffic control system is such that East Santa Clara Street has the priority, 
and the green light is always on for it, while pedestrian walkways along E. Santa Clara St. are always allowed except for the times when
there is a request for pedestrian crossing from the 7th Street or a car coming from 7th Street.

The following steps can be followed to implement the software FSM:
1) Choose a programming language: The first step is to choose a programming language that is appropriate for the project. 
For this project, we can use any programming language that supports the necessary features for implementing the FSM.

2) Define the states: We need to define the different states that the system can be in. In this case, we can define three states:
 Green, Yellow, and Red. Each state will have its own set of conditions and actions.

3) Define the transitions: We need to define the conditions that cause the system to transition from one state to another. 
For example, the system should transition from Green to Yellow after a fixed amount of time, and from Yellow to Red after 
another fixed amount of time.

4) Define the actions: We need to define the actions that should be taken in each state. For example, in the Green state, 
the traffic light for the corresponding direction should be turned on, while in the Red state, all traffic lights should be 
turned off.

5) Implement the FSM: We can now implement the FSM using the programming language we chose in Step 1. This will involve writing 
code that defines the states, transitions, and actions of the system.The Finite State Machine design will be implemented using 
the Python programming language embedded in the KRIA board. The KRIA board will interface with the existing breadboard via the 
PMOD interface. The design can be a combination of Mealy and Moore FSM. The circuit design can be refreshed using old notes from 
previous courses or by referring to online resources showing a 4-state Mealy FSM implementation. Instead of using flip flops to 
implement the FSM, the Python program will implement the FSM.

Clock: 
Clock generation will be done using the 555 chipset in astable mode, which will be used to run the circuit. For the 7-segment circuit, 
a one-digit display can be implemented using the combination of clock, decade counter, BCD-to-7 segment decoder, and the 7-segment 
display. However, for a two-digit display, additional components like a second decade counter will be required. Alternatively, the 
74LS193 up/down counter can also be used.

Components: 
The hardware components provided for the implementation are LEDs for traffic signals, a 7-segment display for a countdown pedestrian 
signal along 7th Street, a push-button to accept pedestrian requests, a BCD-to-7 segment decoder, a binary up/down counter with clear, 
a decade counter, a 555 timer for clock generation, and resistors and capacitors for connecting components. The breadboard from the 
previous courses will be reused.

6) Test the FSM: We should test the FSM to ensure that it is working properly. We can do this by running the code and observing 
the behavior of the traffic lights.


============================================================================================================================================================