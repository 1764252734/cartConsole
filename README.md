# cartConsole
Main RoboCart-Console

# ----------------------journal----------------------- #
#  problem:                                            #
#    1. Can't do it real-time.                         #
#    2. Can't stop automaticly.                        #
#    3. need to excicute two process manually.         #
#    4. ugly.                                          #
#                                                      #
# ---------------------2016.1.31---------------------- #

# ----------------real-time solution------------------ #
#  A. put readline() method into generator(done)       #
#  B. read as many lines as you can at a time          #
# ---------------------------------------------------- #

# ----------------------journal----------------------- #
#  problem:                                            #
#    1. Can't stop automaticly.                        #
#    2. Program will be block when no data send.       #
#    3. Ugly.                                          #
#    4. Need to run it using thread programming.       #
#                                                      #
# ----------------------2016.2.1---------------------- #

# ----------------------journal----------------------- #
#  update:                                             #
#    1. Embedded the plot into Qt5(used to be Tkinter) #
#    2. Woring on complete the function                #
#    3. Thread block problem still unhandled           #
#                                                      #
# ---------------------2016.2.17---------------------- #

# ----------------------journal----------------------- #
#  update:                                             #
#    1. After added timeout=0 arg into serial init th- #
#       e thread block problem finnal solved. but the  #
#       program would still stuck after plotting began #
#    2. The problem above was because when no data re- #
#       ceived program stuck into a endless loop of m- #
#       ethod generatorself.                           #
#    3. working on completing function                 #
#                                                      #
# ---------------------2016.2.18---------------------- #

# -----------------------journal---------------------- #
#  update:                                             #
#    1. Solved many problems which was mentioned above #
#                                                      #
#  problem:                                            #
#    1. Clear function dosen't work correctly.         #
#                                                      #
#  blueprint:                                          #
#    1. Now that we are able to use uart to transport  #
#       data from PC to cart, which means that it is   #
#       possible control cart by PC. It'll including   #
#       these function:                                #
#       (1) use keyboard as a joystick                 #
#       (2) replace keyborad and LCD's function        #
#       (3) make a full use of PC's performance to do  #
#           some adjust work like PID adjustment       #
#       (4) more to think and discuss.                 #
#                                                      #
# ---------------------2016.3.15---------------------- #

# -----------------------journal---------------------- #
#  update:                                             #
#    1. Since I know that uart can do I/O the same t-  #
#       me(almost), developed the control function.    #
#    2. Now using Lowpass filtering to ajust speed fi- #
#       gure and had a great effect.                   #
#    3. Rewrite clear function, now it's good to use   #
#    4. Rewrite axis limits auto-reset function, now   #
#       it will not take a long time to reset bit by   #
#       bit.                                           #
#                                                      #
#  problem:                                            #
#    1. But goRoute function can't work well since ma- #
#       in control program changed, now click goRoute  #
#       button with what click EnmergencyStop button   #
#       to dirve the cart. Need to fix it.             #
#                                                      #
#  blueprint:                                          #
#    1. To make this software more useful. use it at   #
#       an analyse tool to have a speed-up of our dear #
#       cart.                                          #
#                                                      #
# ---------------------2016.4.2----------------------- #

# -----------------------journal---------------------- #
#  updata:                                             #
#    1. Add 4 plots for four wheel rotation.           #
#    2. completed save function(auto generate its      #
#       name)                                          #
#                                                      #
#  blueprint:                                          #
#    Same as one above                                 #
#                                                      #
# ---------------------2016.4.12---------------------- #

# -----------------------journal---------------------- #
#  updata:                                             #
#    1. Remove wheel's rotation plots 'cause it is too #
#       slow to update intime                          #
#    2. Add a useless function to record time node man-#
#       ually, I don't know why there are people who   #
#       wanna go to somewhere by carriage just for     #
#       get their destination faster when a car availa-#
#       ble.                                           #
#                                                      #
#  blueprint:                                          #
#    1. Record cart information automatic.             #
#    2. Demotion plot function as an alternative option#
#                                                      #
# ---------------------2016.4.26---------------------- #
