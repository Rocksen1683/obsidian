```
_Actor Adder{


}


int main(){
	uActor::start();
	for (int r = 0; r < rows; r += 1){
		*new Adder(matrix[r], cols, subtotals[r]) | uActor::startMsg;
	}
	uActor::stop();
}
```