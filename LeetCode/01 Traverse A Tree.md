##Binary Tree Preorder Traversal
* Linkedlist 사용한 답
```kotlin
import java.util.*
class Solution {
    fun preorderTraversal(root: TreeNode?): List<Int> {
        val preorderList = mutableListOf<Int>()
        val stack = LinkedList<TreeNode?>()
        stack.push(root)
        while(!stack.isEmpty()) {
            val currentNode = stack.pop()
            if(currentNode != null){
                preorderList.add(currentNode.`val`)
                stack.push(currentNode.right)
                stack.push(currentNode.left)
            }
        } 
        
        return preorderList
    }
}
```
코틀린에선 자체 linkedlist가 없어서 자바 콜렉션을 사용해아 한다.

