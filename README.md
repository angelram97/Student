import java.util.ArrayList;

public class Program{
    public static void main(String[] args){
        System.out.println("Hello there!!!!");
        return;
    }
public class Student{

String Firstname;
String Lastname;
String Middlename;
String studentid;
String email;

Student(){}
Student(String Firstname,String Lastname, String Middlename, String studentid, String email){
    this.Firstname=Firstname;
    this.Lastname=Lastname;
    this.Middlename=Middlename;
    this.studentid=studentid;
    this.email=email;
}
}
public class Course{
    String crn;
    String rubric;
    String section;
    String courseName;
    String instructor;
    String days;
    String time;
    int classSeat;
    ArrayList<Student> students;

    Course(){}

    Course(String crn, String rubric, String section, String courseName, String instructor, String days, String time, int classSeat){
        this.crn = crn;
        this.rubric = rubric;
        this.section = section;
        this.courseName = courseName;
        this.instructor = instructor;
        this.days = days;
        this.time = time;
        this.classSeat = classSeat;
        this.students = new ArrayList<Student>();
    }

    public String GetCourseName(){
        return this.courseName;
    }

    public void AddStudent(Student student){
        if( this.students.size() >= this.classSeat){
            return; 
        }
        this.students.add(student);
    }
}
}
