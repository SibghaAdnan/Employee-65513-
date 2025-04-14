class Employee {
    String name;
    double salary;

    // Constructor
    public Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }

    // Method to display employee details
    public void displayEmployeeDetails() {
        System.out.println("Employee Name: " + name);
        System.out.println("Salary: $" + salary);
    }
}

// Derived class: Manager
class Manager extends Employee {
    String department;

    // Constructor
    public Manager(String name, double salary, String department) {
        super(name, salary); // Call the constructor of Employee
        this.department = department;
    }

    // Method to display manager details
    public void displayManagerDetails() {
        // Reuse employee detail display method
        displayEmployeeDetails();
        System.out.println("Department: " + department);
    }
}

// Main class
public class InheritanceExample {
    public static void main(String[] args) {
        // Create an Employee
        Employee emp = new Employee("John Doe", 45000.00);
        System.out.println("=== Employee Details ===");
        emp.displayEmployeeDetails();

        System.out.println();

        // Create a Manager
        Manager mgr = new Manager("Alice Smith", 75000.00, "Sales");
        System.out.println("=== Manager Details ===");
        mgr.displayManagerDetails();
    }
}
