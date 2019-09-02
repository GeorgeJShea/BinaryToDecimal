#-----------------------------------------#
# Created By George Shea a ßeta product OPEN SOURCE: enjoy and use have a great day
# date created 27/8/2019
# update date 29/8/2019 version 2.32
# The Fake Binary Project
# does binary math converts and emulutes some work
# can do binary fractions
#-----------------------------------------#

# This Converts the binary into a fraction binary
def ConvertionFrac():
    global ResultPowerb
    global ResultPower
    global bin1
    global bin2

    if len(binFrac1) > 0:  # not neccery just lets me hide information
        power1 = 0
        if len(binFrac1) > 0:
            if "1" in binFrac1[0]:
                power1 = .5
        power2 = 0
        if len(binFrac1) > 1:
            if "1" in binFrac1[1]:
                power2 = .25
        power3 = 0
        if len(binFrac1) > 2:
            if "1" in binFrac1[2]:
                power3 = .125
        power4 = 0
        if len(binFrac1) > 3:
            if "1" in binFrac1[3]:
                power4 = .0625
        power5 = 0
        if len(binFrac1) > 4:
            if "1" in binFrac1[4]:
                power5 = .03125
        power6 = 0
        if len(binFrac1) > 5:
            if "1" in binFrac1[5]:
                power6 = .015625
        power7 = 0
        if len(binFrac1) > 6:
            if "1" in binFrac1[6]:
                power7 = .0078125
        power8 = 0
        if len(binFrac1) > 7:
            if "1" in binFrac1[7]:
                power8 = .00390625
    ResultPower = power1 + power2 + power3 + power4 + power5 + power6 + power7 + power8

    if len(binFrac2) > 0:  # not neccery just lets me hide information
        power1b = 0
        if len(binFrac2) > 0:
            if "1" in binFrac2[0]:
                power1b = .5
        power2b = 0
        if len(binFrac2) > 1:
            if "1" in binFrac2[1]:
                power2b = .25
        power3b = 0
        if len(binFrac2) > 2:
            if "1" in binFrac2[2]:
                power3b = .125
        power4b = 0
        if len(binFrac2) > 3:
            if "1" in binFrac2[3]:
                power4b = .0625
        power5b = 0
        if len(binFrac2) > 4:
            if "1" in binFrac2[4]:
                power5b = .03125
        power6b = 0
        if len(binFrac2) > 5:
            if "1" in binFrac2[5]:
                power6b = .015625
        power7b = 0
        if len(binFrac2) > 6:
            if "1" in binFrac2[6]:
                power7b = .0078125
        power8b = 0
        if len(binFrac2) > 7:
            if "1" in binFrac2[7]:
                power8b = .00390625
    ResultPowerb = power1b + power2b + power3b + power4b + power5b + power6b + power7b + power8b
# this convert it back
def ConvertionBin():
    global overflow
    global strFakeBin
    global strFakeBin2
    global resultPowerComb2
    resultPowerComb2 = (ResultPowerb + ResultPower)

    strresultPowerComb = str(resultPowerComb2)
    if "1" in strresultPowerComb[0]:  # takes out overflow to be put into addtion else do nothing
        resultPowerComb2 = resultPowerComb2 - 1
        overflow = "1"
    else:
        resultPowerComb2 + 0  # so if no overflow it doesnt just error out
        overflow = "0"

    # --------------------------#  produces a fake binary number to be displayed
    decback = resultPowerComb2
    fakeBin = 0
    if decback >= .5:
        decback = decback - .5
        fakeBin = fakeBin + 10000000  # 7 zeros
    if decback >= .25:
        decback = decback - .25
        fakeBin = fakeBin + 1000000  # 6 zeros
    if decback >= .125:
        decback = decback - .125
        fakeBin = fakeBin + 100000  # 5 zeros
    if decback >= .0625:
        decback = decback - .0625
        fakeBin = fakeBin + 10000  # 4 zeros
    if decback >= .03125:
        decback = decback - .03125
        fakeBin = fakeBin + 1000  # 3 zeros
    if decback >= .015625:
        decback = decback - .015625
        fakeBin = fakeBin + 100  # 2 zeros
    if decback >= .0078125:
        decback = decback - .0078125
        fakeBin = fakeBin + 10  # 1 zeros
    if decback >= .00390625:
        decback = decback - .00390625
        fakeBin = fakeBin + 1  # 0 zeros
    # -----------------------------# Lops off extra zeros on the fake binary
    strFakeBin = str(fakeBin)
    strLength = len(strFakeBin)

    if "0" in strFakeBin[strLength - 1]:
        strFakeBin = int(strFakeBin)  # converts string into int to do math
        strFakeBin = strFakeBin // 10
        strFakeBin2 = str(strFakeBin)
        strLength = len(strFakeBin2)


def Calc():
    print("1 Addition")
    print("2 Subtraction")
    print("3 multiplaction")
    print("4 division")
    choose = int(input("Enter Dir Number"))
    def Addition():     # also a converter
        global binFrac1
        global binFrac2
        print("Binary Adder")
        print()
        bin1 = str(input("Please enter first Binary Number: "))
        if 1 == 1:          # using this to hide information in the ide
            if bin1 == "quit":
                Calc()
            else:
                a = 1   # so it just donst run calc
        bin2 = str(input("Please enter second Binary Number: "))
        # --------------------------------------------------------#
        bin1, binFrac1 = bin1.split(".", 1)
        bin2, binFrac2 = bin2.split(".", 1)
        power1 = 0
        ConvertionFrac()
        ConvertionBin()

        addsol = bin(int(bin1, 2) + int(bin2, 2) + int(overflow, 2))    # does the adding for main number
        if binFrac1 == "1" and binFrac2 == "1":
            addsol = int(addsol, 2)
            addsol = addsol -1
            addsol = bin(addsol)
            addsolDec = int(addsol, 2)
            print()
            print("First Number Dec:", int(bin1, 2), "Second Number Dec:", int(bin2, 2))    # converts it to dec to make it easy to understand
            print("First Number Dec Fraction:",ResultPower, "Second Number Dec Fraction",ResultPowerb)       #fractions
            print("Binary Answer:", addsol,".", strFakeBin2, "Decimal Answer:", addsolDec,".", resultPowerComb2)                   # finale result booth in dec and and in bin
            print()
            Addition()
        else:
            addsolDec = int(addsol, 2)
            print()
            print("First Number Dec:", int(bin1, 2), "Second Number Dec:", int(bin2, 2))    # converts it to dec to make it easy to understand
            print("First Number Dec Fraction:",ResultPower, "Second Number Dec Fraction",ResultPowerb)       #fractions
            print("Binary Answer:", addsol,".", strFakeBin2, "Decimal Answer:", addsolDec,".", resultPowerComb2)                   # finale result booth in dec and and in bin
            print()
            Addition()

    if choose == 1:     # Addition Math
        Addition()

    def Subtraction():
        global binFrac1
        global binFrac2
        print("Binary Subtracter")
        print()
        bin1 = str(input("Please enter first Binary Number: "))
        if 1 == 1:          # using this to hide information in the ide
            if bin1 == "quit":
                Calc()
            else:
                a = 1   # so it just donst run calc
        bin2 = str(input("Please enter second Binary Number: "))
        #---#
        bin1, binFrac1 = bin1.split(".", 1)
        bin2, binFrac2 = bin2.split(".", 1)

        power1 = 0

        ConvertionFrac()
        ConvertionBin()

        #---# the full binary numbers
  # does the adding for main number
        if binFrac1 == "1" and binFrac2 == "1":
            addsol = bin(int(bin1, 2) - int(bin2, 2) + int(overflow, 2))
            addsol = int(addsol, 2)
            addsol = addsol -1
            addsol = bin(addsol)
            addsolDec = int(addsol, 2)
            print()
            print("First Number Dec:", int(bin1, 2), "Second Number Dec:", int(bin2, 2))    # converts it to dec to make it easy to understand
            print("First Number Dec Fraction:",ResultPower, "Second Number Dec Fraction",ResultPowerb)       #fractions
            print("Binary Answer:", addsol,".", strFakeBin2, "Decimal Answer:", addsolDec,".", resultPowerComb2)                   # finale result booth in dec and and in bin
            print()
            Addition()
        else:
            addsol = bin(int(bin1, 2) - int(bin2, 2))
            addsolDec = int(addsol, 2)
            print()
            print("First Number Dec:", int(bin1, 2), "Second Number Dec:", int(bin2, 2))    # converts it to dec to make it easy to understand
            print("First Number Dec Fraction:",ResultPower, "Second Number Dec Fraction",ResultPowerb)       #fractions
            print("Binary Answer:", addsol,".", strFakeBin2, "Decimal Answer:", addsolDec,".", resultPowerComb2)                   # finale result booth in dec and and in bin
            print()
            Addition()

        Subtraction()

    if choose == 2:
        Subtraction()

    def Mutiplaction():
        global binFrac1
        global binFrac2

        print("Binary Mutiplyer")
        print()
        bin1 = str(input("Please enter first Binary Number: "))
        if 1 == 1:          # using this to hide information in the ide
            if bin1 == "quit":
                Calc()
            else:
                a = 1   # so it just donst run calc
        bin2 = str(input("Please enter second Binary Number: "))

        bin1, binFrac1 = bin1.split(".", 1)
        bin2, binFrac2 = bin2.split(".", 1)
        ConvertionFrac()

        bin1 = int(bin1, base = 2)              # turns booth binaries into floats then adds the decimals to mutlitply later
        bin1 = bin1 + ResultPower
        bin2 = int(bin2, base=2)
        bin1 = bin1 + ResultPowerb

        addsolDec = bin1  * bin2

        addsola = addsolDec
        addsola, addsolb = divmod(addsola, 1)
        addsola = int(addsola)
        addsola = bin(addsola)
        # FakeBinary Maker
        ConvertionBin()
        addsol = 1
        print()
        print("First Number Dec: ",bin1 - ResultPower, "Second Number Dec",bin2 + ResultPowerb)    # converts it to dec to make it easy to understand
        print("First Number Dec Fraction:", ResultPower, "Second Number Dec Fraction", ResultPowerb)  # fractions
        print ("Binary Answer:", addsola, strFakeBin2 , "Decimal Answer:", addsolDec)                   # finale result booth in dec and and in bin
        print()
        Mutiplaction()

    if choose == 3:
        Mutiplaction()

    def Divider():      # diffrent of the bunch
        global binFrac1
        global binFrac2
        print("Binary Diveder")
        print()
        bin1 = str(input("Please enter first Binary Number: "))
        if 1 == 1:          # using this to hide information in the ide
            if bin1 == "quit":
                Calc()
            else:
                a = 1   # so it just donst run calc
        bin2 = str(input("Please enter second Binary Number: "))
        bin1, binFrac1 = bin1.split(".", 1)
        bin2, binFrac2 = bin2.split(".", 1)

        ConvertionFrac()
        bin1 = int(bin1, base = 2)              # turns booth binaries into floats then adds the decimals to mutlitply later
        bin1 = bin1 + ResultPower
        bin2 = int(bin2, base=2)
        bin1 = bin1 + ResultPowerb

        addsolDec = bin1 /bin2

        addsola = addsolDec
        addsola, addsolb = divmod(addsola, 1)
        addsola = int(addsola)
        addsola = bin(addsola)
        # FakeBinary Maker
        ConvertionBin()
        addsol = 1
        print()
        print("First Number Dec: ",bin1 - ResultPower, "Second Number Dec",bin2 + ResultPower)    # converts it to dec to make it easy to understand
        print("First Number Dec Fraction:", ResultPowerb, "Second Number Dec Fraction", ResultPower)  # fractions
        print ("Binary Answer:", addsola, strFakeBin2, "Decimal Answer:", addsolDec)                   # finale result booth in dec and and in bin
        print()
        Divider()

    if choose == 4:
        Divider()
    if choose >= 5:
        print()
        Calc()

Calc()
