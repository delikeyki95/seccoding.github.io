---
layout: post
title:  "Angular 완성 압축 파일"
---

### Angular 실습 완성 파일 링크
<a href="https://github.com/seccoding/seccoding.github.io/blob/master/files/Angular_DONE.zip?raw=true">Angular_DONE.zip</a>

### FormGrouop & FormConrol
FormValidate 예제에서 FormGroup & FormControl 예제를 수행하기 위해서는 위 두 객체를 가지고 있는
ReactiveFormsModule이 반드시 필요합니다.

@angular/forms 에 포함되어 있는 객체이므로 다른 설치작업은 필요가 없습니다.

FormControl은 Template 의 Form Element를 Component에서 제어하기 위해 사용되며
FormGroup은 FormControl을 하나로 묶으려 할 때 사용됩니다.

이때, Component에서 지정한 FormGroup의 이름은 Form의 formGroup 명과 일치해야 하며
FormConrol의 이름 또한 Form 의 formContol 명과 일치해야 합니다.

FormGroup / FormControl은 무작정 사용하시기 보다, Custom Validation Check Logic 이 필요할 때 유용하게 사용할 수 있습니다.
