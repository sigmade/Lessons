###Interfaces for DI

1. Upcasting object to Interface

``` C#
internal class Program
    {
        static void Main(string[] args)
        {
            // Upcasting InMemoryData object to IDataProvider
            IDataProvider data = new InMemoryData();

            // Conshole show "InMemoryData"
            data.GetAll();

            // Before upcasting SomeMethod not available
            data.SomeMethod();

            Console.ReadKey();
        }

        public interface IDataProvider
        {
            void GetAll();
        }

        public class InMemoryData : IDataProvider
        {
            public void GetAll() => Console.WriteLine("InMemoryData");

            // This method not contained in IDataProvider
            public void SomeMethod() => Console.WriteLine("SomeMethod");
        }

        public class FileData : IDataProvider
        {
            public void GetAll() => Console.WriteLine("FileData");
        }
    }
```

![image](https://user-images.githubusercontent.com/55326490/181919293-fdc472b5-3b63-4a1d-b055-435c16f0587c.png)

