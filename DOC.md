# 다시 모임 



## DB schema



### post

id (auto increment, primary key) : int(10)

writer : int(10)

title : varchar(30)

content : text

bad : bool



### user

id (auto increment, primary key) : int(10)

userid : varchar(20)

userpw : varchar(250)

bad : bool



## API



### 회원가입 (POST)

**URL**

[BASE_URL]/signup

**REQUEST PARAMETER**

id : [사용자 id] / pw : [사용자 pw]

**RESPONSE**

```json
{
    code : 200(성공) / 400(실패)
}
```



### 로그인 (POST)

**URL**

[BASE_URL]/signin

**REQUEST PARAMETER**

id : [사용자 id] / pw : [사용자 pw]

**RESPONSE**

```json
{
    code : 200(성공) / 400(실패)
}
```



### 글 저장 (POST)

**URL**

[BASE_URL]/savePost

**REQUEST PARAMETER**

id : [사용자 id] / title : [게시글 제목] / content : [게시글 내용]

**RESPONSE**

```json
{
    code : 200(성공) / 400(실패)
}
```



### 글 목록 불러오기 (GET)

**URL**

[BASE_URL]/getPostList

**REQUEST PARAMETER**

page : [페이지 번호]

**RESPONSE**

```json
{
    code : 200,
    postList : [
        {
            id : int(10)
			writer : int(10)
			title : varchar(30)
			content : text
			bad : bool
        },
		{
            id : int(10)
			writer : int(10)
			title : varchar(30)
			content : text
			bad : bool
        }
    ]
}
```



### 글 불러오기 (GET)

**URL**

[BASE_URL]/getPost

**REQUEST PARAMETER**

id : [게시글id]

**RESPONSE**

```json
{
    code : 200,
    post : {
        id : int(10)
		writer : int(10)
		title : varchar(30)
		content : text
		bad : bool
    }
}
```
