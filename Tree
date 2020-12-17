class TreeNode:
    def __init__(self, data):
        self.data = data
        self.children = []
        self.parent = None

    def add_child(self, child):
        child.parent = self
        self.children.append(child)
    
    def get_level(self):
        level = 0
        p = self.parent
        while p:
            level += 1
            p = p.parent

        return level
  
    def print_tree(self):
        spaces = ' ' * self.get_level() * 3
        prefix = spaces + "|__" if self.parent else ""
        print(prefix + self.data)
        if self.children:
            for child in self.children:
                child.print_tree()

   

def build_product_tree():
    root = TreeNode("Kendaraan")

    darat = TreeNode("darat")
    darat.add_child(TreeNode("mobil"))
    darat.add_child(TreeNode("motor"))
    darat.add_child(TreeNode("sepeda"))

    laut = TreeNode("laut")
    laut.add_child(TreeNode("kapal"))
    laut.add_child(TreeNode("Jetski"))

    udara = TreeNode("udara")
    udara.add_child(TreeNode("pesawat"))
    udara.add_child(TreeNode("balon udara"))

    sepeda = TreeNode("sepeda")
    sepeda.add_child(TreeNode("Lipat"))
    sepeda.add_child(TreeNode("MTB"))

    kapal = TreeNode("kapal")
    kapal.add_child(TreeNode("pinisi"))
    kapal.add_child(TreeNode("boat"))


    root.add_child(darat)
    root.add_child(laut)
    root.add_child(udara)
    darat.add_child(sepeda)
    laut.add_child(kapal)

    
    root.print_tree()

if __name__ == '__main__':
    build_product_tree()
