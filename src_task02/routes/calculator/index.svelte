<script lang="ts">
    import { Button } from '@src/components/button';
    //import { NULL } from 'node-sass';
    const textNumbers: string[] = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0'];
    const textSymbols: string[] = ['+','-','='];
    
    //variables
    let inputEx:string[]=[];
    let inputPostfixed:string[]=[];
    let operands:string[]=[];
    let top:number = 0;
    let result:number;

    // //infix to postfix
    // const toPostfix = function toPostfix(inputStr:string[]){
    //     //operands stack
    //     for(let i = 0 ; i < inputStr.length ; i++ ){
    //         if( !isNaN(Number(inputStr[i])) ){
    //             inputPostfixed[inputPostfixed.length] = inputStr[i];
    //         }else{
    //             operands[top] = inputStr[i];
    //             ++top;
    //             // if(operands.length === 0){
    //             //     top=0;
    //             //     operands[top] = inputStr[i];
    //             // }else{
    //             //     for(let j = 0 ; j < operands.length ; j++){
    //             //         if( getOprRank(operands[top]) > getOprRank(inputStr[i]) ){
    //             //             ++top;
    //             //             operands[top] = inputStr[i];
    //             //             break;
    //             //         }else{
    //             //             inputPostfixed[inputPostfixed.length]=operands[top];
    //             //             operands.pop();
    //             //             --top;
    //             //         }
    //             //     }
    //             // }
    //         }       
    //     }
    // }

    //ordering operands
    const getOprRank = function getOprandRank(opr:string):number{
        if(opr === '*'||opr==='/'){
            return 1;
        }
        else if(opr === '+'||opr==='-'){
            return 2;
        }
        else if(opr === "="){
            return 3;
        }
        else{
            console.log(`the operand ${opr} not defined`);
            return NaN;
        }
    }

    // get input
    const getExpression = function getEx(newInput:string){
        inputEx[inputEx.length] = newInput;
        console.log(inputEx);
        if(newInput === "="){
            //toPostfix(inputEx);
            //console.log(inputPostfixed);
        }
    }
</script>


<div>
    <div class="frame">
        {#each textNumbers as text}
            <Button {text} color="orange" onClick2={(value) => getExpression(value)} />
        {/each}
        {#each textSymbols as text}
            <Button {text} color="grey" onClick2={(value) => getExpression(value)}/>
        {/each}
    </div>
</div>


<style lang="scss">
	.frame {
		width: 240px;
		display: flex;
		flex-wrap: wrap;
	}
</style>