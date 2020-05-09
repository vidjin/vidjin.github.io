This is a basic blog to implement fuzzy box in the MATLAB.

Software used: Matlab R2010a

Problem Statement: Food Tipping
Tip is decided on the basis of various attributes. Selected member function for attributes is triangular here. Range is selected so that membership functions don’t overlap with each other.

Input Variable:
| S.No. | Attributes | Range |
| :-----| ---------- | -----:|
|1.     | Taste      | [0 3] |
|       | Delicious  | [0 1] |
|       | Normal     | [1 2] |
|       | Rancid     | [2 3] |
|2.     | Ambience   | [0 3] |
|       | Worst      | [0 1] |
|       | Good       | [1 2] |
|       | Excellent  | [2 3] |
|3.     | Service    | [0 3] |
|       | Slow       | [0 1] |
|       | On time    | [1 2] |
|       | Fast       | [2 3] |
|4.     | Price      | [0 2] |
|       | Reasonable | [0 1] |
|       | Costly     | [1 2] |
|5.     | Hygiene    | [0 2] |
|       | Clean      | [0 1] |
|       | Stinky     | [1 2] |


Output Variable:
| S.No. | Attributes | Range    |
| :-----| ---------- | ------:  |
|1.     | Tip        | [0 1]    |
|       | 100        | [0 0.2]  |
|       | 200        | [0.2 0.4]|
|       | 300        | [0.4 0.6]|
|       | 400        | [0.6 0.8]|
|       | 500        | [0.8 1]  |


Steps:

1.Start matlab and type fuzzy in command window. 

![Output](/images/fuzzy1.png "Output Screenshot")

2.A new wizard named FIS Editor will open (Fuzzy Inference System).  

![Output](/images/fuzzy2.png "Output Screenshot")

3.Go on Edit->Add variable->Input. Do this for 4 times as we have five input variables. Change name of the input variable by editing the content of Name.

![Output](/images/fuzzy3.png "Output Screenshot")

4.Similarly edit the name of all five variables and output variable. Now save the work in file first. Go to File->Export-> File. Now save the food_tip.fis file. FIS editor will look like as follows:

![Output](/images/fuzzy4.png "Output Screenshot")

5. Double click on the taste input variable to edit the attributes of taste. Taste has three attributes namely: delicious, normal, rancid. New box will pop up named Membership Function Editor. Go to Edit->Remove All MFs. Then Edit-> Add Mfs. Small box asking for type and no of mf will pop up. Select trimf and 3 as we want to use the triangular member function and no of member function is 3. Click Ok.      

![Output](/images/fuzzy5.png "Output Screenshot")

6.Set range of taste variable as [0 3] (your choice). Edit mf1 name as delicious and its parameters. Parameters in triangular membership function is vertices of triangle. Select [0 0.5 1]. Similarly set all three membership function as required.

![Output](/images/fuzzy6.png "Output Screenshot")

7. Do it for all the variables. Close the membership function editor.

![Output](/images/fuzzy7.png "Output Screenshot")

![Output](/images/fuzzy8.png "Output Screenshot")

![Output](/images/fuzzy9.png "Output Screenshot")

![Output](/images/fuzzy10.png "Output Screenshot")

![Output](/images/fuzzy11.png "Output Screenshot")

8. In FIS Editor, go to Edit-> Rules. A new rule Editor will open. Now add rules one by one. Close when you are done.

![Output](/images/fuzzy12.png "Output Screenshot")

9. Now go to View->Rules. See output by varying inputs. First input is [0.5 2.5 2.5 0.5 0.5] = [taste=delicious ambience=excellent service=fast price=reasonable hygiene=clean] (as range of delicious in taste is [0 1] so 0.5 means delicious, similarly others are done) so the tip value is 0.9 so tip would be 500 (as range of 500 is [0.8 1]).

![Output](/images/fuzzy13.png "Output Screenshot")

10.Similarly, you can try for another inputs.

![Output](/images/fuzzy14.png "Output Screenshot")

Fuzzy toolbox implemented in the Matlab successfully. Thanks for reading!
