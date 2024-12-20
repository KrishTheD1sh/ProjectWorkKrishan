class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        self.data = {
            "January": {"behavior": "Inelligible", "attendance": "Unkown"},
            "February": {"behavior": "Inelligible", "attendance": "Unkown"},
            "March": {"behavior": "Inelligible", "attendance": "Unkown"},
            "April": {"behavior": "Inelligible", "attendance": "Unkown"},
            "May": {"behavior": "Inelligible", "attendance": "Unkown"},
            "June": {"behavior": "Inelligible", "attendance": "Unkown"},
            "July": {"behavior": "Inelligible", "attendance": "Unkown"},
            "August": {"behavior": "Inelligible", "attendance": "Unkown"},
            "September": {"behavior": "Excellent", "attendance": "100%"},
            "October": {"behavior": "Good", "attendance": "100%"},
            "November": {"behavior": "Good", "attendance": "100%"},
            "December": {"behavior": "Excellent", "attendance": "100%"},
            "Overall": {"behavior": "Excellent", "attendance": "100%"},
        }

    def get_monthly_report(self, month):
        month_data = self.data.get(month)
        if month_data:
            print(f"Report for {self.name} ({month}):")
            print(f"  Behavior: {month_data['behavior']}")
            print(f"  Attendance: {month_data['attendance']}")
        else:
            print(f"No data available for {month}.")


def main():
    print("Welcome to the Student Management System")
    student = Student(name="Krishan Sharma", age=16)

    while True:
        print("\nOptions:")
        print("1. View Monthly Report")
        print("2. Exit")
        choice = input("Enter your choice (1/2): ")

        if choice == "1":
            month = input("Enter the month (e.g. January): ")
            student.get_monthly_report(month)
        elif choice == "2":
            print("Exiting the system. Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")


if __name__ == "__main__":
    main()
