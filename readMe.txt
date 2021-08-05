[요소 중복사용에 대한 주의사항]

CSS에서
header, footer, main으로만 선택자를
지정하여 사용하면
중복현상이 발생하여
추후 원인파악이 어려운 문제가 발생할 수 있음

보기.

<div#wrap>

   <header#header>

   </header>    =>   header {   ...   }  (X)
                               ! 아래 main의 header와
                                 중복 문제 발생
                             header#header { ... } (O)
   ....

   <main#main>
       <header#mainHeader>
       </header>     
   </main>

</div>



마이그레이션(migration)
=> 타사에서 진행한 작업을
     우리회사의 작업에 맞도록 수정하는 것
