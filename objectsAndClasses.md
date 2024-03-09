//using System;
//namespace Randomize_Words;
//class Program
//{
//    static void Main(string[] args)
//    {
//        string[] words = Console.ReadLine().Split();
//        string text = Console.ReadLine();
//        Random random = new Random();
//        for (int i = 0; i < words.Length; i++)
//        {
//            int randomIndex = random.Next(words.Length);
//            string word = words[i];
//            string randomIndexWord = words[randomIndex];
//            words[i] = randomIndexWord;
//            words[randomIndex] = word;

//        }
//        Console.WriteLine(string.Join(Environment.NewLine, words));
//    }
//}




//using System;
//using System.Numerics;
//// import the necessary library
//using System.Numerics;
//// create a function to calculate the factorial
//static BigInteger Big_Factorial(int num)
//{
//    // initialize a BigInteger variable to store the result
//    BigInteger result = 1;

//    // loop through the numbers from 1 to the given number
//    for (int i = 1; i <= num; i++)
//    {
//        // multiply the result with the current number
//        result *= i;
//    }

//    // return the result
//    return result;
//}

//int input = int.Parse(Console.ReadLine());

//// call the function to calculate the factorial
//BigInteger factorial = Big_Factorial(input);

//// print the result
//Console.WriteLine(factorial);




//using System;
//namespace Songs;
//class Song
//{
//    //Declaring variables
//    private string typeList;
//    private string name;
//    private string time;
//    //Constructor
//    public Song(string typeList, string name, string time)
//    {
//        this.typeList = typeList;
//        this.name = name;
//        this.time = time;
//    }
//    //Method to get the name of the song
//    public string nGetName()
//    {
//        return name;
//    }
//    //Method to get the type list of the song
//    public string GetTypeList()
//    {
//        return typeList;
//    }
//}
//class Program
//{
//    static void Main()
//    {
//        //Getting the number of songs
//        int n = int.Parse(Console.ReadLine());
//        //Creating an array to hold the songs
//        Song[] songs = new Song[n];
//        //Looping to get the song information
//        for (int i = 0; i < n; i++)
//        {
//            string input = Console.ReadLine();
//            string[] songInfo = input.Split('_');

//            //Creating a new Song object
//            Song song = new Song(songInfo[0], songInfo[1], songInfo[2]);

//            //Adding the song to the array
//            songs[i] = song;
//        }

//        //Getting the type list or "all" command
//        string command = Console.ReadLine();

//        //Checking if the command is "all"
//        if (command == "all")
//        {
//            //Looping through the songs and printing out their names
//            foreach (Song song in songs)
//            {
//                Console.WriteLine(song.nGetName());
//            }
//        }
//        else
//        {
//            //Looping through the songs and checking if their type list matches the given command
//            foreach (Song song in songs)
//            {
//                if (song.GetTypeList() == command)
//                {
//                    Console.WriteLine(song.nGetName());
//                }
//            }
//        }
//    }
//}



//using System;

//namespace StudentInfo
//{
//    class Student
//    {
//        public string firstName;
//        public string lastName;
//        public int age;
//        public string homeTown;

//        public Student(string fName, string lName, int studentAge, string town)
//        {
//            firstName = fName;
//            lastName = lName;
//            age = studentAge;
//            homeTown = town;
//        }
//    }

//    class Program
//    {
//        static void Main(string[] args)
//        {
//            string input = Console.ReadLine();
//            string[] info = input.Split();

//            Student[] students = new Student[10];
//            int index = 0;

//            while (input != "end")
//            {
//                string fName = info[0];
//                string lName = info[1];
//                int studentAge = int.Parse(info[2]);
//                string town = info[3];

//                Student student = new Student(fName, lName, studentAge, town);
//                students[index] = student;
//                index++;

//                input = Console.ReadLine();
//                info = input.Split();
//            }

//            string city = Console.ReadLine();

//            foreach (Student student in students)
//            {
//                if (student != null && student.homeTown == city)
//                {
//                    Console.WriteLine($"{student.firstName} {student.lastName} is {student.age} years old.");
//                }
//            }
//        }
//    }
//}





//using System;
//class Student
//{
//    // properties of the student
//    public string FirstName;
//    public string LastName;
//    public int Age;
//    public string City;

//    // constructor to initialize the student's information
//    public Student(string firstName, string lastName, int age, string city)
//    {
//        FirstName = firstName;
//        LastName = lastName;
//        Age = age;
//        City = city;
//    }
//}

//class Program
//{
//    static void Main()
//    {
//        // create a dictionary to store the students
//        Dictionary<string, Student> students = new Dictionary<string, Student>();

//        // get input from the user
//        string input = Console.ReadLine();

//        // continue getting input until the user enters "end"
//        while (input != "end")
//        {
//            // split the input by spaces
//            string[] studentInfo = input.Split(' ');

//            // check if the student already exists in the dictionary
//            if (students.ContainsKey(studentInfo[0] + " " + studentInfo[1]))
//            {
//                // if yes, overwrite the information with the new input
//                students[studentInfo[0] + " " + studentInfo[1]] = new Student(studentInfo[0], studentInfo[1], int.Parse(studentInfo[2]), studentInfo[3]);
//            }
//            else
//            {
//                // if not, add the new student to the dictionary
//                students.Add(studentInfo[0] + " " + studentInfo[1], new Student(studentInfo[0], studentInfo[1], int.Parse(studentInfo[2]), studentInfo[3]));
//            }

//            input = Console.ReadLine();
//        }

//        // get the city from the user
//        string city = Console.ReadLine();

//        // loop through each student in the dictionary
//        foreach (var student in students)
//        {
//            // check if the student's city matches the input
//            if (student.Value.City == city)
//            {
//                // if yes, print out the student's information
//                Console.WriteLine("{0} {1} is {2} years old.", student.Value.FirstName, student.Value.LastName, student.Value.Age);
//            }
//        }

//        Console.ReadLine();
//    }
//}



//using System;
//using System.Collections.Generic;
//using System.Linq;
//namespace StoreBox
//{
//    class Box
//    {
//        public string SerialNumber { get; set; }
//        public string Item { get; set; }
//        public int quantity { get; set; }
//        public decimal PriceBox { get; set; }
//        public decimal TotalPrice { get; set; }
//    }

//    class Program
//    {
//        static void Main(string[] args)
//        {
//            List<Box> boxes = new List<Box>();
//            string line = Console.ReadLine();
//            while (line != "end")
//            {
//                string[] data = line.Split();
//                string serialNumber = data[0];
//                string itemName = data[1];
//                int itemQuantity = int.Parse(data[2]);
//                decimal itemPrice = decimal.Parse(data[3]);
//                Box box = new Box();
//                box.SerialNumber = serialNumber;
//                box.Item = itemName;
//                box.quantity = itemQuantity;
//                box.PriceBox = itemPrice;
//                box.TotalPrice = itemQuantity * itemPrice;
//                boxes.Add(box);
//                line = Console.ReadLine();
//            }
//            List<Box> sortedBox = boxes.OrderByDescending(boxes => boxes.TotalPrice).ToList();

//            foreach (Box box in sortedBox)
//            {
//                Console.WriteLine($"{box.SerialNumber}");
//                Console.WriteLine($"-- {box.Item} - ${box.PriceBox:f2}: {box.quantity}");
//                Console.WriteLine($"-- ${box.TotalPrice:f2}");
//            }
//        }
//    }
//}



//using System;
//using System.Linq;
//using System.Collections.Generic;

////Class
//namespace VehicleCatalogue
//{
//    class Catalogue
//    {

//        public string Type { get; set; }
//        public string Brand { get; set; }
//        public string Model { get; set; }
//        public double Weight { get; set; }
//        public double HorsePower { get; set; }
//    }
//}


//namespace VehicleCatalogue
//{
//    class Program
//    {
//        static void Main(string[] args)
//        {
//            List<Catalogue> vehicleCatalogue = new List<Catalogue>();
//            int count = 0;

//            while (true)
//            {
//                string command = Console.ReadLine();
//                string[] parts = command.Split("/");

//                if (command == "end")
//                {
//                    break;
//                }

//                string type = parts[0];
//                string brand = parts[1];
//                string model = parts[2];
//                double weight = double.Parse(parts[3]);
//                double horsePower = double.Parse(parts[3]);

//                Catalogue vehicle = new Catalogue();

//                vehicle.Type = type;
//                vehicle.Brand = brand;
//                vehicle.Model = model;
//                vehicle.Weight = weight;
//                vehicle.HorsePower = horsePower;

//                vehicleCatalogue.Add(vehicle);

//            }

//            List<Catalogue> sortedCatalogue = vehicleCatalogue.OrderBy(vehicle => vehicle.Brand).ToList();

//            foreach (Catalogue vehicle in sortedCatalogue)
//            {
//                if (count == 0)
//                {
//                    Console.WriteLine("Cars:");
//                    count++;
//                }

//                if (vehicle.Type == "Car")
//                {
//                    Console.WriteLine($"{vehicle.Brand}: {vehicle.Model} - {vehicle.HorsePower}hp");
//                }
//            }

//            foreach (Catalogue vehicle in sortedCatalogue)
//            {
//                if (count == 1 && vehicle.Type == "Truck")
//                {
//                    Console.WriteLine("Trucks:");
//                    count++;
//                }

//                if (vehicle.Type == "Truck")
//                {
//                    Console.WriteLine($"{vehicle.Brand}: {vehicle.Model} - {vehicle.Weight}kg");
//                }
//            }
//        }
//    }
//}

