``` C#
public class InMemoryData
    {
        //The static field will be available to all instances
        private static List<int> NumbersInType = new List<int>();
        // The non-static field will be available to the current instance
        private List<int> NumbersInInstance = new List<int>();

        public List<int> GetNumbersFromType()
        {
            return NumbersInType;
        }

        // Invoke static method without create instance. Only for static field
        public static List<int> StGetNumbersFromType()
        {
            return NumbersInType;
        }

        public List<int> GetNumbersFromInstance()
        {
            return NumbersInInstance;
        }

        public void AddNew(int num)
        {
            //The added element will be available to all instances
            NumbersInType.Add(num);
            //The added element will be available to the current instance
            NumbersInInstance.Add(num);
        }
    }
```

![LoaderAndGcHeap drawio (4)](https://user-images.githubusercontent.com/55326490/180656129-3a4c8892-8fd9-4905-83d8-f6c06d16f52f.png)


