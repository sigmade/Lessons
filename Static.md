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

        // Invoke static method without create instance
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

![LoaderAndGcHeap drawio (3)](https://user-images.githubusercontent.com/55326490/180650856-e3259f12-8d09-4190-9459-5275e8d70d3a.png)


