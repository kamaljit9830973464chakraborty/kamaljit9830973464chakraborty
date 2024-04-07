- 👋 Hi, I’m @kamaljit9830973464chakraborty
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
kamaljit9830973464chakraborty/kamaljit9830973464chakraborty is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->








THIS IS KAMALJIT CHAKRABORTY  ...  
I AM WORKING IN AN AIRPLANE MANUFACTURING COMPANY , UNITED STATES  OF AMERICA ... [
THE BOEING COMPANY , 100 NORTH RIVER SIDE PLAZA , ILLIONOS , CHICAGO , 60606 , 
Phone : +12536579813 , Email Address : ipm@boeing.com ...
EMPLOYEE ID : 6881HL74231152G ] 

IATA ADMINISTRATION  [ AIRLINES.IATA.ORG ]
I WORKED FROM MYSELF HOUSE THROUGH INTERNET SERVICE ... 
I DID MYSELF BE ENGINEERING DEGREE IN COMPUTER SCIENCE FROM 
MASSACHUSETTS INSTITUTE CSAIL,  UNITED STATES OF AMERICA 
[ 77 Massachusetts Avenue, Room 11-400 
Cambridge, MA 02139-4307
Email Address: newsoffice@mit.edu
Phone: 617-253-2700
Fax: 617-258-8762 ] ... I COMPLETE THESE DEGREE FROM MYSELF HOUSE THROUGH ONLINE 
COURSE STUDIES ...
BEMSID : 1H982839zaQ☆
MEMSID : H264
PhD. COURSE ID : P033:T-7B-10HF [ FLYGHT CONTROLLER SYSTEM ]


CERTIFICATION DETAILS ... ... ... 

FOUNDATION ENTRANCE FOR BE COURSE PAPERS AND MARKS OBTAIN FOR CSE ADMISSION ... 
MASSACHUSETTS INSTITUTE OF TECHNOLOGY CSAIL RESEARCH UNIT FOUNDATION COURSE NUMBERS ...  
PR - 63005 - 69 ... 
BIOLOGY  15 / 20 ,  
PHYSICS : 16 / 20 , 
CHEMISTRY : 12 / 20 , 
MATH : 11 / 20 , 
ENGLISH : 14 / 20 , 
COMPUTER : 17 / 20 ... 
TOTAL : 65% 


BE COURSE PAPERS AND MARKS OBTAIN FOR CSE ... 


COMPUTER ARCHITECTURE AND DESIGN 42 / 60 ... 
OPERATING SYSTEM 45 / 60 ... 
ALGORITHMS 38 / 50  ... 
COMPUTER NETWORKING 35 / 50 ... 
MATH FOR COMPUTER SCIENCE 25 / 40 ...


ME COURSE PAPERS AND MARKS OBTAIN FOR CSE ... 

PROGRAMMING LANGUAGE [ 2 ] ... THIS PART NO MARKS OBTAIN ... 

COMPUTER ARCHITECTURE AND DESIGN ... AGILITY ... 
PAPER COMPLETED 4 ... EACH PAPER MARK 6 OUT OF 8 ... TOTAL ... 24

ALGORITHMS AND DATA STRUCTURE ... CREATIVITIES ... 
PAPER COMPLETED 1 ...  PAPER MARK 5 OUT OF 8 ... TOTAL ... 5
 

OPERATING SYSTEM ... COLLABORATION ... 
PAPER COMPLETED 2 ...  EACH PAPER MARK 5 OUT OF 8 ... TOTAL ... 10
  

COMPUTER NETWORKING AND DISTRIBUTED SYSTEM ... EMPLOYEE SATISFACTION ... 
PAPER COMPLETED 3 ...  EACH PAPER MARK 3 OUT OF 8 ... TOTAL ... 9 [ POOR AND CONSIDERATION ]


DATABASE ... INITIAL SOCIALIZATION ... 
PAPER COMPLETED 1 ...   PAPER MARK 5 OUT OF 8 ... TOTAL ... 5


MATH FOR COMPUTER SCIENCE  [ OPTIONAL FOR FOUNDATION ] ONGOING TEAM TRUST ... 
PAPER COMPLETED 4 ...  EACH PAPER MARK 3 OUT OF 8 ... TOTAL ... 12 [ POOR AND CONSIDERATION ]


15 PAPERS ... TOTAL MARKS OBTAIN 67 NUMBER ... OUT OF 120 NUMBER ... 
15 PAPERS ... TOTAL MARKS OBTAIN 67%  [80.4 ] NUMBER ... OUT OF 120 NUMBER ... 









import sys, math 
from tkinter import * 
from PIL.ImageTk import PhotoImage 
from viewer_thumbs import makeThumbs, ViewOne 

def viewer(imgdir, kind=Toplevel, cols=None):    
    """    
custom version that lays out with fixed-size buttons    
    """    
    win = kind()    
    win.title('Viewer: ' + imgdir)    
    thumbs = makeThumbs(imgdir)    
    if not cols:        
    
    cols = int(math.ceil(math.sqrt(len(thumbs))))      # fixed or N x N    
    savephotos = []    
    while thumbs:        
        thumbsrow, thumbs = thumbs[:cols], thumbs[cols:]        
        row = Frame(win)        
        row.pack(fill=BOTH)        
        for (imgfile, imgobj) in thumbsrow:            
        size    = max(imgobj.size)                     # width, height            
        photo   = PhotoImage(imgobj)            
        link    = Button(row, image=photo)
        handler = lambda savefile=imgfile: ViewOne(imgdir, savefile)            
        link.config(command=handler, width=size, height=size)            
        link.pack(side=LEFT, expand=YES)            
        savephotos.append(photo)    
        
     Button(win, text='Quit', command=win.quit, bg='beige').pack(fill=X)    
     return win, savephotos 
if __name__ == '__main__':    
    imgdir = (len(sys.argv) > 1 and sys.argv[1]) or 'images'    
    main, save = viewer(imgdir, kind=Tk)    
    main.mainloop()
