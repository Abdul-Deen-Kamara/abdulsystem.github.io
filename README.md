import random

class StudentIDCard:
    def __init__(self, student_name, student_id):
        self.student_name = student_name
        self.student_id = student_id

    def generate_card(self):
        card_info = f"Student ID Card\n\nName: {self.student_name}\nID: {self.student_id}"
        return card_info

def generate_student_id():
    # Generate a random 6-digit student ID
    return ''.join(random.choices('0123456789', k=6))

def main():
    # Get student details
    student_name = input("Enter student name: ")

    # Generate student ID
    student_id = generate_student_id()

    # Create StudentIDCard object
    student_card = StudentIDCard(student_name, student_id)

    # Generate and print the student ID card
    print(student_card.generate_card())

if __name__ == "__main__":
    main()
