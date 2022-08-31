<script lang="ts">
	export let text: string;
	export let onClick2: (value: string) => void; //함수명 : (매개변수) => 반환값
	export let color: 'orange' | 'grey' | 'dark-grey';
</script>

<div class="button" data-color={color} on:click={() => onClick2(text)}>{text}</div>
<!-- index.svelte에서 이 컴포넌트가 사용 될 때, 태그의 속성값으로 대입되는 값들이 {변수}의 값으로 할당된다 -->
<!--on:click={()=>onClick(text)}가 의미하는 것은, button의 on:click 이벤트가 발생 했을 때, onClick(text)메소드
를 실행시킨다는 의미이다. 그런데, 이 함수표현식을 담는 onClick 식별자가 {} 안에 있으므로
index.svelte에서 (onClick 식별자가 상징하는) 변수에 대한 값이 할당되어야 함을 의미한다. 
index.svelte에서 여기에 값을 할당 할때, 일반 값을 저장하는 변수와 달리 함수표현식을 할당할 때는 
여기서 선언한 함수표현식변수의 식별자를 속성값의 이름으로 사용한다  (!!이 해석이 맞을까??)-->

<style lang="scss">
	.button {
		width: 80px;
		height: 80px;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 24px;
		font-weight: 600;
		&[data-color='orange'] {   //& nested selector //ex) .button[data-color = 'orange'] === .button{&[data-color = 'orange']}
			background-color: orange;
		}
		&[data-color='grey'] {
			background-color: grey;
		}
		&[data-color='dark-grey'] {
			background-color: darkgrey;
		}
	}
</style>