#Spring Boot WebFlux Mongo Reactive

#Mono<Blog> create(@RequestBody Blog blog)
POST  http://localhost:8090/api/v1/blog

{
	"title":"testTitle",
	"content":"testcontent",
	"author":"testauthor"
}

#Flux<Blog> findAll()
GET     http://localhost:8090/api/v1/blog

#Mono<Blog> findOne(@PathVariable String id)
GET     http://localhost:8090/api/v1/blog/5dbc25e6d9bdf8061816bb1d

#Flux<Blog> findByTitle(@RequestParam String blogTitle)
GET     http://localhost:8090/api/v1/blog?blogTitle=testTitle

#Mono<Blog> updateBlog(@RequestBody Blog blog, @PathVariable String id)
PUT     http://localhost:8090/api/v1/blog/5dbc25e6d9bdf8061816bb1d

{
	"title":"test",
	"content":"test",
	"author":"test"
}


#Mono<Boolean> delete(@PathVariable String id)
DELETE  http://localhost:8090/api/v1/blog/5dbc25e6d9bdf8061816bb1d