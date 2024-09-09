import 'dart:io';
void main(){
  List<String>inventory=['apple', 'banana', 'carrot','dates'];
  print("Initial Iventory: $inventory");
  
  while(true)
  {
     print('Please Select an Operation to do:');
     print('[1] Add new Product in the inventory');
     print('[2] Remove a Product from the inventory');
     print('[3] Display the total number of items in the inventory');
     print('[4] Allow the user to search for an item and display if its available or not');
     print('[5] Sort the inventory list Alphabetically');
     print('[6] Exit ');
     print('You have selected:');
      int option = int.parse(stdin.readLineSync()!);
      
      if (option ==1){
          addProduct(inventory);
      } else if(option ==2) {
          removeProduct(inventory);
      } else if (option ==3){
          int total = getTotalItems(inventory);
          print("Total number of Items in inventory: $total");
      } else if (option ==4){
          stdout.write("Enter a Product to search: ");
          String? searchProduct = stdin.readLineSync();
          bool isAvailable = isProductAvailable(inventory, searchProduct);
          if(!isAvailable) {
              print("$searchProduct is not available in the inventory");
          } else {
              print("$searchProduct is avalable in the inventory");
          }
      } else if (option ==5){
          sortInventory(inventory);
      } else if (option ==6){
          break;
      } else {
          print ("Invalid Product");
      }
  }
}

void addProduct(List<String>inventory){
    stdout.write("Enter a product to add: ");
    String? newProduct = stdin.readLineSync();
    if(newProduct != null && newProduct.isNotEmpty){1
        inventory.add(newProduct);
        print("Updated Inventory: $inventory");
    }
}

void removeProduct(List<String> inventory){
    stdout.write("Enter a Product to Remove: ");
    String? removeProduct = stdin.readLineSync();
    if(removeProduct != null && inventory.contains(removeProduct)){
        inventory.remove(removeProduct);
        print("Updated inventory after removal: $inventory");
    } else {
        print("$removeProduct not found in the inventory");
    }
}
int getTotalItems(List<String>inventory){
    return inventory.length;
} bool isProductAvailable(List<String>inventory, String? product){
    return product!= null && inventory.contains(product);
}

void sortInventory(List<String> inventory){
    inventory.sort();
    print("Sort inventory: $inventory");
}
