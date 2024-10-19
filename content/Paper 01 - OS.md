#### Question 1 
```
binary sem insert = 1 
binary sem dispense = 1
counting sem coin = 0 
counting sem cookie = 0 

Person{ 
while(True){
	PrepareCoin()
	semWait(insert)
	InsertCoin()
	semSignal(insert)
	semSignal(coin)
}
}

Machine{
while(True){

while(True){
	PrepareCookie()
	semWait(coin) // 3 times
	semWait(dispense)
	DispenseCookie()
	semSignal(dispense)
	semSignal(cookie)
}
}

Kid{
	semWait(dispense)
	semWait(cookie)
	GrabCookie()
	semSignal(Dispense)
	EatCookie()
}
```
