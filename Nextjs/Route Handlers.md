# What are route handlers ?
Route handlers let you to make api calls inside your next js app . Its like mini backend in your nextjs app . Help uou to make post , get , delete , patch requests.
### Example 
  In app/api/todos/route.js
  ```
let todos =[]
  export  async function GET (){
return Response.json(todos)
}
export async function POST (request) {
const body=await request.json()
const newTodo={id : Data.now() , task : body.task}
todos.push(newTodo)
return Response.json(newTodo,{status:201})

}
export async function DELETE (request,{params}) {
const id={params}
todos.filter((t)=>t.id !== Number(id))
return Response.json(message:"todo deleted successfully !"})

export async function PATCH(request,{params}) {
const id={params}
const body = await request.json()
todos.map((t)=>t.id === Number(id) ? {...t ,...body} : t)
return Response.json(message:"todo updated!"})

}
   ```
## caching in route handlers :
No defaut caching for route handlers but default caching can be used only for get requests 
