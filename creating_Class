class Book:
    def __init__(self, title="Unknown", author="Unknown", ISBN="Unknown", price=0.0):
        self.title = title
        self.author = author
        self.ISBN = ISBN
        self.price = price
    
    def display_info(self):
        print(f"\nBook Information:")
        print(f"Title: {self.title}")
        print(f"Author: {self.author}")
        print(f"ISBN: {self.ISBN}")
        print(f"Price: ${self.price:.2f}")
    
    def discount_price(self, discount):
        if self.price > 0:
            discounted_price = self.price - (self.price * discount / 100)
            return discounted_price
        return None

def main():
    books = []
    N = int(input("How many books would you like to add? "))
    
    for _ in range(N):
        print("\nLet's add a new book!")
        add_details = input("Would you like to provide details for this book (yes/no)? ").lower()
        
        if add_details == 'yes':
            title = input("Enter the book's title: ")
            author = input("Enter the author's name: ")
            ISBN = input("Enter the ISBN of the book: ")
            price = float(input("Enter the price of the book: $"))
            book = Book(title, author, ISBN, price)
        else:
            book = Book()
        
        books.append(book)
    
    print("\nHere's the list of books you've added:")
    for book in books:
        book.display_info()
        apply_discount = input(f"Would you like to apply a discount to {book.title}? (yes/no): ").lower()
        
        if apply_discount == 'yes':
            discount = float(input(f"Enter the discount percentage for {book.title}: "))
            new_price = book.discount_price(discount)
            if new_price:
                print(f"New discounted price for {book.title}: ${new_price:.2f}")
            else:
                print(f"Sorry, we couldn't apply a discount for {book.title}.")
        else:
            print(f"Great! No discount applied to {book.title}.")
    
    print("\nThank you for using the book catalog!")

if __name__ == "__main__":
    main()
