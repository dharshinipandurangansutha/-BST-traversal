# -BST-traversal
Practical program 
class Node:
    def __init__(self, data):
        self.left = None
        self.right = None
        self.data = data


def inorder(root):
    if root:
        inorder(root.left)
        print(root.data, end=" ")
        inorder(root.right)


def preorder(root):
    if root:
        print(root.data, end=" ")
        preorder(root.left)
        preorder(root.right)


def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.data, end=" ")


root = Node(50)
root.left = Node(30)
root.right = Node(70)
root.left.left = Node(20)
root.left.right = Node(40)
root.right.left = Node(60)
root.right.right = Node(80)

print("Inorder Traversal:")
inorder(root)

print("\nPreorder Traversal:")
preorder(root)

print("\nPostorder Traversal:")
postorder(root)
Inorder Traversal:
20 30 40 50 60 70 80

Preorder Traversal:
50 30 20 40 70 60 80

Postorder Traversal:
20 40 30 60 80 70 50
