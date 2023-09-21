# Collection Pattern

## Collection Pattern

1. 대부분의 경우, 여러 리소스를 하나의 그룹으로 묶을 수 있다
2. 예를 들어 게시물의 경우, 100개의 게시물을 하나의 게시물 그룹(컬렉션)으로 묶어서 표현하는 게 훨씬 유용하다.

Collection Pattern을 쓰지 않는 경우:

```
/the-first-post  
/test-post
//무의미한 식별자를 사용하고 있음
```

Collection Pattern을 쓰는 경우:

```
/posts //모든 게시물을 하나의 URI로 표현(게시물 목록으로도 활용 가능). 
       //일반적으로 복수형을 사용한다.
/posts/the-first  // [/리렉토리/폴터] ->/posts/1-the-first 이렇게도 가능
/posts/test                        ->/posts/2-test 
/posts/{id} 또는 /posts/:id 등으로 일반적인 형태로 쓸 수 있다.
                            //여기서 {id}를 {post_id}나 {postId} 등으로 표기할 수도 있다. 
                            //{id}는 Post ID라고 부를 예정.
```

{% hint style="warning" %}
#### Post ID는 리소스의 ID가 아님에 주의!Post ID는 리소스의 ID가 아님에 주의!

* 리소스의 ID는 URI(=URL)이다.
* Post ID는 Resource ID를 구성하는 요소 중 하나. posts 그룹 내에서 식별자(ID).
{% endhint %}

#### 그룹명은 복수형으로 사용하기 때문에 collection(items,그룹)이 아니라 element(item,하나)를 지정할 때도 복수형이 쓰인다는 점에 주의.

* /posts/1 -> 복수형으로 그룹명을 지정하고, 그 아래에서 개별 아이템을 지정.
* /post/1 -> 흔히 하는 실수. 반드시 복수형을 써야 하는 건 아니지만, 이렇게 사용하는게 좋음

#### 특정 게시물에 댓글 달리는 상황

```
/posts/{post_id}/comments
// /posts/1/comments ->댓글 목록처럼 활용가능
// /comments?post_id={post_id} 형태로 써줘도 된다 ->comments? post_id가 {post_id}다

/posts/{post_id}/comments/{id}  //특정한 하나를 나타내고싶을때, 여기서 {id}는 {comment_id}를 의미
// [/posts/{post_id}][/comments/{id}] 
```

#### 특정 게시물을 고치는 페이지 표현(수정)

```
/posts/{id}/edit      //“Edit Page”라는 리소스
/edit?post_id={post_id} -> 사용할 수 있지만 지향하지 않음 X
/items, /items/{id} 같은 URL만 쓰도록 제약해도 무방하다.
```



{% hint style="success" %}
컬렉션 패턴 훈련을 많이 해봐야 한다.!!!
{% endhint %}

####
