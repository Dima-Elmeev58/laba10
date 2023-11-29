# laba10
Student student1 = new Student("Строгий А.Ю", 2015, "Ул Дунина д84", 89674567027, 3, "Программирование");
Student student2 = new Student("Алдыр М.О", 2016, "Ул Пушкина д137", 89886720917, 2, "Монтажник");
Student student3 = new Student("Давыдов И.Д", 2017, "Ул Московская д15", 89378670909, 4, "Электрик");
Student[] mass = new Student[] { student1, student2, student3 };
for(int i = 0; i < mass.Length; i++)
{
    Console.WriteLine($"ФИО студента: {mass[i].fio}");
}
Console.WriteLine("Введите факультет: Программирование, Монтажник или Электрик");
string ? facul = Console.ReadLine();
for (int i = 0; i < mass.Length; i++)
{
    if (mass[i].faculty == facul)
    {
        Console.WriteLine($"Студент заданного факультета {mass[i].fio}");
    }
}
Console.WriteLine("Введите год");
int data = Convert.ToInt32( Console.ReadLine() );
for (int i = 0; i < mass.Length; i++)
{
    if (mass[i].data > data)
    {
        Console.WriteLine($"Студент, поступивший после заданного года:{mass[i].fio}");
    }
}
class Student
{
    private string FIO;
    private int Data;
    private string Address;
    private long PhoneNumber;
    private int Course;
    private string Faculty;
    public Student(string fIO, int data, string address, long phoneNumber, int course, string faculty)
    {
        this.FIO = fIO;
        this.Data = data;
        this.Address = address;
        this.PhoneNumber = phoneNumber;
        this.Course = course;
        this.Faculty = faculty;
    }
    public string fio
    {
        get { return FIO; }
        set { FIO = value; }
    }
    public int data
    {
        get { return Data; }
        set { Data = value; }
    }
    public string address
    {
        get { return Address; }
    }
    public long phonenumber
    {
        get { return PhoneNumber; }
        set { PhoneNumber = value; }
    }
    public int course
    {
        set { Course = value; }
    }
    public string facalty
    {
        get { return Faculty; }
    }
}
