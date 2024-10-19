Extend the [[MaDUM]] of the base class to generate $MaDUM_{derived}$
- Take the MaDUM of the base class 
- Add a row for each newly defined or re-defined data member in derived 
- Add column for each defined or re-defined function of the derived class 

Retest *inherited attributes* 
 - Check upper right quadrant (quadrant one) of MaDUMderived 
   • We have to ascertain which inherited attributes mandate re-testing $\to$ MaDUMderived can be used for automation 
   • Once these inherited attributes are identified, the test procedure is similar to slice testing in the base class, but uses inherited and new/redefined methods
