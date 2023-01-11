# toyproject1-fromVue

![끝말잇기,구구단](https://user-images.githubusercontent.com/113073242/211707278-88a52bce-9f90-41b2-9e8e-1e87b43cd93f.png)


Vue 를 처음 배우고 나서 Vue를 활용해서 간단하게 제작해본 끝말잇기와 구구단 연습하기 입니다.

Vue3 cdn 을 활용하였습니다. 

끝말잇기의 경우 첫 제시된 `카메라`부터 시작합니다.

if 구문을 활용해서 

제시된 단어 혹은 다음 단어의 마지막 글자와 
인풋창에 입력한 단어의 첫글자가 동일하면 정답입니다를 출력하고
틀린 경우엔 오답입니다를 출력하게 하였습니다.


        if (this.laWorld[this.laWorld.length - 1] == this.laWorld2[0]) {
          this.result = '정답입니다.';
          this.laWorld = this.laWorld2;
        } else {
          return this.result = '오답입니다.'
        }
        
        
구구단 연습하기 역시 if 구문을 활용하였습니다.

        if (parseInt(this.numRe) === this.num1 * this.num2) {
          this.gugure = '정답입니다.';
          this.num1 = Math.round(Math.random() * 9);
          this.num2 = Math.round(Math.random() * 9);
          this.numRe = ''
        } else {
          this.gugure = '오답입니다.'
          this.numRe = ''
        }
        
        
        
        
무작위로 숫자를 두개 뽑아 곱한 결과값이 맞을경우엔 정답입니다를 출력하고 새로 숫자 두개를 무작위로 다시 뽑게하였으며,
오답인 경우엔 입력창을 다시 비우게 하여 재 입력하게 만들었습니다.
