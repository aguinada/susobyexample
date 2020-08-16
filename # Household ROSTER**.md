# Household ROSTER

## Paper questionnaire roster
This example is intended to show how a tyoical questionnaire roster is designed in [Survey Solutions](https://mysurvey.solutions/). In this examples the roster captures and validates information for each houshold member.

Below is the layout of a roster on a paper questionnaire  used to capture the main data on household members.

![Paper questionnaire ROSTER](ht/../images/E1.paperform.jpg)
 
## Questionnaire designed in Survey Solution
The image presents how this roster is designed in SuSo.

![](ht../../images/E1.susu.designer.jpg)

If you have access to the SuSo Designer, you can go to the previous questionnaire [Got to Suso Designer](https://webtester.mysurvey.solutions/WebTester/Interview/ca6d1e51427945738f2189e69c25b65d/Section/7fa7e4e509e9cf60f8139c9879a456cc_1)
You also can [download PDF] (ht/../pdf/SSBE-Household ROSTER.pdf)

## Questionnaire exceution and memory objects 

In our design **hhmembers** object is List type field and **RMEMBERS** roster type linked to hhmembers list. 

When executing the questionnaire, as the user enters the names of the household members, the **hhmembers** memory object obtains its values. Note that the hhmembers object has two columns, the **Item1** stores the identifying number of each member and the **item2** stores the text entered by the user.

This screen is presented in SuSo to capture household members names (hhmembers list)

![](ht/../images/E1.suso.hhmemebers.jpg)

The object hhmembers in memory stores member names in column **Item2** and assigne a secuential number to each one in column **Item1**

![](ht/../images/E1.mem.hhmembers.jpg)

This screen captures information for each member (RMEMBERS roster)

![](ht/../images/E1.suso.RMEMBERS.jpg)

In memory, the object RMEMBERS stores each field in form of a column.

![](ht/../images/E1.mem.RMEMBERS.jpg)

```
!MEMBERS.Any( p=> IsAnswered(p.coworkers) &&  
  p.coworkers.Any( o=>!MEMBERS[o[0]].
      coworkers.Any( m=>m[0]==p.@rowcode))
)
```
