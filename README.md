void main()

{
List<String> inventory ['apple', 'banana', 'carrot', 'dates'];
print('Initial Inventory: $inventory');

while(true)
{
stdout.write('\n\nPlease select an Operation to do: ');
stdout.write('\n[1] Add New Product in the inventory');
stdout.write('\n[2] Remove a Product from the inventory');
stdout.write('\n[3] Display the total number of items in the inventory');
stdout.write('\n[4] Allow the user to search for an item and display if it is available or not');
stdout.write('\n[5] Sort the inventory list Alphabetically');
stdout.write('\n[6] Exit');
stdout.write('\nYou have selected: ');
int option int.parse(stdin.readLineSync()!);

if(option==1)
{ addProduct(inventory, "");
}
else if(option==2)
{ removeProduct(inventory, "");
}
else if(option--3)
int total getTotalItems(inventory);
print("Total number of items in inventory: $total");
}
else if(option--4)
{
stdout.write("Enter a product to search: ");
String? searchProduct stdin.readLineSync();
bool isAvailable=isProductAvailable(Inventory, "");
if(!isAvailable==searchProduct
{
print("$searchProduct is not available in the inventory");
}
else{
print("$searchProduct is available in the inventory");
}

}else if(option==5)
sortInventory(inventory);
}
else if(option==6)
{
break;
}
else{ print("Invalid Input");
}
}
}
void addProduct(List<String> inventory, String product)
{
stdout.write("Enter a product to add: '); String? newProduct stdin.readLineSync(); if(newProduct I-null && nesProduct.isNotEmpty)
{
 inventory.add(new Product);
print("Updated Inventory: $inventory");
}
}
void removeProduct(List<String>inventory, String product)
{
stdout.write("Enter a product to remove: '); String? removeProduct stdin.readLineSync();
if (removeProduct I-null && inventory.contains (removeProduct))
{ inventory.remove (remove Product);
}
print("Updated inventory after removal: $inventory");
else{
print("SremoveProduct not found in the inventory");
}
}
int getTotalItems(List<String>inventory)
}
return inventory.length;
}
bool isProductAvailable(List<String>inventory, String product)
return inventory.contains(product);
}
void sortInventory(List<String> inventory)
Inventory.sort(); print("Sorted inventory: $inventory");
old removeProduct(List<String>inventory, String product) inventory.remove(removeProduct); print("Updated inventory after removal: Sinventory");
else{ print("SremoveProduct not found in the inventory");
}
}
int getTotalItems(List<String>inventory)
{
}
return inventory.length;
bool isProductAvailable(List<String>inventory, String product)
{
return inventory.contains(product);
}
void sortInventory(List<String> inventory)
{
inventory.sort();
print("Sorted inventory: $inventory");
}
