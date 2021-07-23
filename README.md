# Voter-Machine-Using-MATLAB
In this project, a demo software program using MATLAB based graphical user interface (GUI) to demonstrate the working of an EVM is presented. GUIDE is used to develop the GUI for this demo project, with components like "Static Text" to display Party Name, Votes, Votes Percentage, and "Push Button" components are used as Vote, Result and Reset Buttons. The logic is this demo project is very simple, for each party we have created a global variable, which is declared and initialized. So some of the additional feature of this project are as follows:  Voters who's names and Id's are present in Database can only vote. Duplicate Voting is not allowed. Voting Percentage is also calculated. So with the above mentioned features one can create a more robust and professional system. To create database, Microsoft Excel is used and names of voters and there voting id's are written in two different columns. For this project a sample database of 20 voters is created. We have the database now, and then in system we have to load this data, and based on the ID's we have to take action whether a voter can vote or not. Whenever someone presses the voting button, system will asks for its voting id and then search the voting id in its database. 
After the addition of database in the system now we can see various changes in the GUI. Whenever a voter will cast his/her vote he has to enter his Voting ID only then he/she will be able to cast his/her vote. Also, if he tries to vote again, the system will display,”You cannot vote multiple times.” And when a wrong ID is entered the system displays,”No user found!”

 # ALGORITHM OF THE PROGRAM:

Step 1 : Create the EVM display using GUI Options on GUIDE's Tools menu."GUI allows only one instance to run (singleton)".
Step 2: Start the Initialisation code.
               Assign gui_Singleton to 1;
              Create a function called gui_State and assign the structure within        
               I t('gui_Name',       mfilename, ...








Step 3 : Declare the number of voters and their usernames within the function EVM_OpeningFcn(hObject, eventdata, handles, varargin).
Names will be declared in global variable. For example.. [global Kavya;] and will be assigned as 0 initially.
 Step 4 : Calling of function varargout = EVM_OutputFcn(hObject, eventdata, handles) under which will call out the CALLBACK function of every individuals assigned earlier.
Step 5 : Import Database into our MATLAB code(we have created an excel database od 20 people with voting id and name).
Step 6 : To initialize a beeping sound after casting the vote. So to create such, we need to add the following statement :
 i.e. load chirp.mat; (MAT-files  in MATLAB stores various sounds with the signal vector in a variable y and the frequency Fs, so these MAT-files includes chirp, splat, train,etc type of generalized sounds..here we have used the chirp.MAT)





Step 7 : Calling of function RESULTS_Callback(hObject, eventdata, handles)
Here will declare the assigned names in global variable and also will assign the set of function handle of every individual to evaluate the mathematical expressions over a range of values.
For example:
[set(handles.Kri,'String',Krity);] - returns content of Kri as text
 [set(handles.Krs1,'String',100*Krishno/(Kavya+Krity+Krishno+Kaustab+Raj));] - percentage of total number of votes for Kavya.
Step 8 : Will assign the background colour and other textures of the EVM system of individual parties using CreateFcn function and also will assign the  
total_CALLback function to declare the total votes of all parties and the texture design using total_CreateFcn function.
