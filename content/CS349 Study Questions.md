
## Question 26
``` TypeScript
return mx >= x && mx <= x + w && my >= y && my <= y + h
```

## Question 27

``` TypeScript

insideRectangle = mx >= x && mx <= x + w && my >= y && my <= y + h;
outsideRectangle = mx >= x - s/2 && mx <= x + w + s/2 && my <= y - s/2 && my >= y + h + s/2; 

return outsideRectangle && !insideRectangle;
```

## Question 39 
``` tsx
type HexColourProps = { value: string; onChange:(newValue: string) => void; }; 

function HexColour({value, onChange }: HexColourProps) {
	const [invalid, setValid] = useState(isValid(value))
	const [val, setVal] = useState(value)

	function handle(e: Event) { 
	const v =(e.currentTarget as HTMLInputElement).value;
	setVal(v);
	if isValid(v){
		setValid(true);
		if(onChange){
			onChange(v);
		}}
	else{
		setValid(false)
	}
	}
}
	return (
	<>
	<input
	type = "text"
	value = {val}
	class = {!isValid(value) ? "invalid" : ""}
	onInput = {handle}
	{!isValid && <p> Invalid </p>}
	</>
	)
}
```

## Question 40 
```tsx 
type PhoneInputProps =
{phoneNumber? : number;
 onChange : (p : number) => void
}

function PhoneInput({value: initialValue, onChange }: PhoneInputProps) {
	const [invalid, setValid] useState(initialValue? isValidPhone(initialValue) : False);

	function handleOnInput(e: Event) {
	const num = (e.currentTarget as HTMLInputElement).value;
	if (isValid(num)){
		if(onChange){
			onChange(num);
		}}
	else{
		setValid(false)
	}
	}

	return (
	 <input 
	 type = "text"
	 value = {value}
	class = {!isValid(value) ? "invalid" : ""}
	onInput = {handle}>
	{!isValid && <p> Invalid </p>}
	 >
	)
}
```

## Question 41 
``` tsx 
function App(){
	const [count, setCount] = useState(0);

	function onChange(v: number) => {
		setCount(v);
	}
	return (
	<>
	<CountButton value=count onChange=onChange type="increase">
	<CountButton value=count onChange=onChange type="decrease">
	</>
	)
}

type CountButtonProps = {
value: number;
onChange: (v: number) => void;
type: string
}

function CountButton({value, onChange, type}: CountButtonProps){

	return(
	<>
	{type=="increase"? 
	<button onClick={onChange(value + 1)}>Increase</button>:
	<button onClick={onChange(value -1)}>Decrease</button>}
	</>
	)
}
```

## Question 42 
```tsx
type CanvasProps = {
width: number;
height: number;
x: number;
y: number
}
```

```tsx
function Canvas({width, height, x, y}: CanvasProps){
	const canvasRef = useRef<HTMLCanvasElement>(null)

	useLayoutEffect(() => {
		const gc = canvasRef.current?.getContext("2d");
		if(gc){
			draw(gc)
		}
	}, [])

	function draw(gc: CanvasRenderingContext2D){
		gc.fillRect(x, y, 50, 50);
		gc.translate(x + 25, y + 25);
	}

	return (
	<canvas ref={canvasRef} width={width} height={height}/>
		)
}
```
