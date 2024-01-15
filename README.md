# TREE-BALANCED-TREE-python-
Daniel Suardy Putra (50422381) 2IA26
class Node:
    def __init__(self, key):
        self.key = key
        self.left = None
        self.right = None

def is_balanced(root):
    if root is None:
        return True

    lh = height(root.left)
    rh = height(root.right)

    if abs(lh - rh) <= 1 and is_balanced(root.left) and is_balanced(root.right):
        return True

    return False

def height(node):
    if node is None:
        return 0
    return 1 + max(height(node.left), height(node.right))
