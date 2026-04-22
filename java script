import java.util.*;

class Product {
    int id;
    String name;
    int price;

    Product(int id, String name, int price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }

    void display() {
        System.out.println(id + " - " + name + " - ₹" + price);
    }
}

class Cart {
    List<Product> items = new ArrayList<>();

    void addProduct(Product p) {
        items.add(p);
        System.out.println(p.name + " added to cart!");
    }

    void showCart() {
        if (items.isEmpty()) {
            System.out.println("Cart is empty");
            return;
        }

        int total = 0;
        System.out.println("Cart Items:");
        for (Product p : items) {
            p.display();
            total += p.price;
        }
        System.out.println("Total = ₹" + total);
    }
}

public class FlipkartClone {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Products
        Product p1 = new Product(1, "Mobile", 10000);
        Product p2 = new Product(2, "Laptop", 50000);
        Product p3 = new Product(3, "Shoes", 2000);

        Cart cart = new Cart();

        while (true) {
            System.out.println("\n--- Flipkart Menu ---");
            System.out.println("1. View Products");
            System.out.println("2. Add to Cart");
            System.out.println("3. View Cart");
            System.out.println("4. Exit");

            int choice = sc.nextInt();

            switch (choice) {
                case 1:
                    p1.display();
                    p2.display();
                    p3.display();
                    break;

                case 2:
                    System.out.println("Enter product id:");
                    int id = sc.nextInt();

                    if (id == 1) cart.addProduct(p1);
                    else if (id == 2) cart.addProduct(p2);
                    else if (id == 3) cart.addProduct(p3);
                    else System.out.println("Invalid ID");
                    break;

                case 3:
                    cart.showCart();
                    break;

                case 4:
                    System.out.println("Thank you!");
                    return;

                default:
                    System.out.println("Invalid choice");
            }
        }
    }
}
