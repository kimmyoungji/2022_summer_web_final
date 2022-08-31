
<script lang="ts">
	// import { Button } from '@src/components/button';
	import {Calculator} from '@src/routes/calculator';
	// const textNumbers: string[] = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0'];
	// let testFunc = function(txt:string)=>{
	// 	txt = txt + "testing";
	// 	alert(txt);
	// }; --> 이게 안되는 이유가 뭘까? html에 바로 스크립트를 적용 할 수없나?
	// 같은 페이지에 정의 되거나, 연결된 스크립트 코드에 정의 된 함수 부를 수 있다.

	// js 함수 정의 방법 두가지
	//1.
	// js function declearation
	// function textFunc2(txt:string){
	// 	txt = txt + "hello world!";
	// 	alert(txt);
	// }
	//2.
	//js function expression declearation
	// const testFunc3 = function func3(txt:string){
	// 	txt = txt + "hello world!333";
	// 	alert(txt);
	// }

	// Ts 함수 정의 방법 두가지
	//3.
	//Ts function declearation
	// function testFunc4(txt:string):string{
	// 	txt = txt + "hello world!4444";
	// 	return txt;
	// }
	//4.
	//Ts function declearation
	// const testFunc5 = function func5(txt:string):string{
	// 	txt = txt + "hello world!55555";
	// 	return txt;
	// }
</script>

<!-- <div class="frame">
	{#each textNumbers as text}
		<Button {text} color="orange" onClick2={(value) => alert(testFunc5(value))} />
	{/each}
	<Calculator/>
</div> -->

<div>
	<h1>Hello Calculator</h1>
	<Calculator/>
</div>

<!-- <style lang="scss">
	.frame {
		width: 240px;
		display: flex;
		flex-wrap: wrap;
	}
</style> -->