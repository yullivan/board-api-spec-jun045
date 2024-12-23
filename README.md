# <게시판>
## 1.생성
POST /boards
- 게시판 이름 String
- 게시판 설명 String
- 생성자 id / 비밀번호 생성
- PathVariable

## 2.조회
<게시판 목록 조회>
GET/boards
-게시판 이름
-게시글 내용
-RequestParam

## 3.수정
PUT/boards/{boardId}
-생성자id, 비밀번호 입력, 비교 후 수정 가능
-PathVariable
-RequestBody

## 4.삭제
DELETE /boards/{boardId}
-생성자id, 비밀번호 비교 후 삭제 가능
-PathVariable

# <게시글>
## 1.생성(작성)
POST /boards/{boardId}/posts
-게시글 제목
-작성자 닉네임 또는 ID, 비밀번호 입력
-게시일자
-PathVariable

## 2.조회
GET /boards/{boardId}/posts/{postId}
- 게시글 제목
- 게시글 내용
-RequestParam

## 3.수정
PUT /boards/{boardId}/posts/{postId}
- 생성자id / 비밀번호 입력, 비교 후 수정 가능
- RequestParam

## 4. 삭제
DELETE /boards/{boardId}/posts/{postId}
- 생성자id, 비밀번호 비교 후 삭제 가능
- RequestParam

# <댓글>
## 1. 생성
POST /boards/{boardId}/post/{postId}/comments
- 생성자 id, 비밀번호 
- 내용
- PathVariable

## 2. 조회
GET /boards/{boardId}/posts/{postId}/comments
- 댓글 목록 조회
- 호출할때 게시판id와 게시글id 지정
- RequestParam

## 3. 수정
PUT /boards/{boardId}/posts/{postId}/comments/{commentId}
- 생성자ID, 비밀번호 비교 후 삭제 가능
- RequestParam

## 4. 삭제
DELETE /boards/{boardId}/posts/{postId}/comments/{commentId}
-id, 비밀번호 비교 후 삭제 가능
- RequestParam

