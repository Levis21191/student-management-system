abstract class Person {

    private String name;

    public Person(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public abstract void displayDetails();
}

class Student extends Person {

    private int studentId;
    private String course;
    private int marks;

    public Student(int studentId, String name, String course, int marks) {
        super(name);
        this.studentId = studentId;
        this.course = course;
        this.marks = marks;
    }

    public String getGrade() {
        if (marks >= 70)
            return "A";
        if (marks >= 60)
            return "B";
        if (marks >= 50)
            return "C";
        if (marks >= 40)
            return "D";
        return "Fail";
    }

    public void displayDetails() {
        System.out.println("Student ID: " + studentId);
        System.out.println("Name: " + getName());
        System.out.println("Course: " + course);
        System.out.println("Marks: " + marks);
        System.out.println("Grade: " + getGrade());
    }
}

public class Main {

    public static void main(String[] args) {

        Student student1 = new Student(21191, "ndulele", "Information Technology", 90);

        System.out.println("STUDENT DETAILS");
        student1.displayDetails();
    }
}

