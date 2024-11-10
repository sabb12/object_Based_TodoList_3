## Project Introduction(프로젝트 소개)
##### ▪ Object로 만든 Todo List
<br/>

## What I've learned(배운 점)
#### [프론트엔드] 
##### 1. [장점]: 간단하고 빠르게 개발 가능하며 instance(인스턴스)가 하나만 생성되기 때문에 Heap 메모리에 할당이 적어 성능이 가벼움
##### 2. [단점]: 프로젝트가 커질수록 복잡해서 관리가 어려워지고, 객체간 공통 기능 정의하기 어렵고, 유지보수가 어려움 
##### [코드 예시]:
```Javascript
const input = document.getElementById('todoInput');
const button = document.getElementById('addBtn');

let newTodo = [];
button.addEventListener('click', () => {
    newTodo.push({ title: input.value, done: false });
    console.log(newTodo);
});
```
##### [결과]: newTodo에 계속 새로 push하면 newTodo라는 instance(인스턴트) 하나만 생성된다.
```Javascript
let newTodo = [
    { title: "1", done: false },
    { title: "2", done: true },
    { title: "3", done: false }
];
```
<br/>

## Key Feature(주요 기능)
### 1. 할 일 추가 기능
##### ▪ 사용자가 입력창(.input)에 텍스트를 입력하고 Enter 키를 누르거나, addBtn 버튼을 클릭하면 새로운 할 일(todo) 항목이 추가됨.
##### ▪ handleCreateTodo() 함수는 새로운 할 일을 newTodo에 추가하고, HTML 요소로 변환한 후 DOM에 추가함.
<br/>

### 2. 할 일 삭제 기능
##### ▪ 각 할 일에는 삭제 버튼이 포함되어 있으며, 사용자가 이 버튼을 클릭하면 해당 항목이 newArray 배열에서 제거되고 DOM에서도 삭제됨.
##### ▪ 이벤트 위임을 사용하여 deleteButton 클래스를 가진 요소를 클릭했을 때 삭제 기능을 수행함.
<br/>

### 3. 완료 체크박스 기능
##### ▪ 사용자가 체크박스를 클릭하면 할 일의 checked 상태가 업데이트되며, 해당 항목이 "To Do" 목록에서 "Done" 목록으로 이동합니다(또는 반대로 이동).
<br/>

### 4. 할 일 수정 기능
##### ▪ 새로운 ToDo 항목 추가 시 input은 disabled=false로 시작합니다.
##### ▪ 수정 버튼 클릭 시 버튼이 "저장"으로 바뀌고, input은 disabled=true로 변경됩니다.
##### ▪ 저장 후 버튼이 "수정"으로 돌아가고, input은 다시 disabled=false로 돌아갑니다.
<br/>

## Stacks(사용 스택)
### - Environment

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-007ACC?style=for-the-badge&logo=Visual%20Studio%20Code&logoColor=white)
<br/>

### - Development
- Languages

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=Javascript&logoColor=white)
<br/>

## Project View(화면 구성)
![image](https://github.com/user-attachments/assets/9e029fc2-c461-4c7d-a5f9-83238a925576)


## Project Structure(프로젝트 구조)
```markdown
object_Based_TodoList_3
├── index.css
├── index.html
├── index.js
├── README.md
```
