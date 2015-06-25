import os, sys
import Image, ImageGrab, ImageOps
import time, random
from random import randrange
import win32api, win32con
from numpy import *


#Globals
#----------------------------

x_pad = 781
y_pad = 831


#End Globals
#-------------------------------------


def grab():
    box = (x_pad + 1,y_pad+1,x_pad+10,y_pad+8)
    im = ImageGrab.grab(box)
    im.save(os.getcwd() + '\\Grab001.png', 'PNG')
    return im

def F5 (*args):
    win32api.keybd_event(0x74[i], 0,0,0)
    time.sleep(.05)
    win32api.keybd_event(0x74[i],0 ,win32con.KEYEVENTF_KEYUP ,0)

def getButton():
    
    im = ImageOps.grayscale(ImageGrab.grab
                            ((xPad+1,yPad+1,xPad+9,yPad+7)))
    a = array(im.getcolors())
##    im.save(os.getcwd() + '\\getButton1.png', 'PNG')
    print 'table 1 bubble = %d' % a.sum()
    return a.sum()

def buyFood ():
    
    if s.getpixel(783, 833) != (190, 217, 191):
            time.sleep(.1)
    else:
            F5 (*args)
            time.sleep(1)
            buyFood ()


def main():
    grab()
##    print 'Ran Main()'
##    while True:
##        getButton()
    


if __name__ == '__main__':
    main()
