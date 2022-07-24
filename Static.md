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

![LoaderAndGcHeap drawio (5)](https://user-images.githubusercontent.com/55326490/180656222-1b075fa8-f83b-4f17-8375-6c87afbbc32b.png)


