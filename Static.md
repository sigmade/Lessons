``` C#
public class InMemoryData
    {
        private static List<int> NumbersInType = new List<int>();
        // Only instance field without static
        private List<int> NumbersInInstance = new List<int>();

        public List<int> NumbersFromType()
        {
            return NumbersInType;
        }
        // Invoke method without create instance
        public static List<int> NumbersFromTypeStatic()
        {
            return NumbersInType;
        }

        public List<int> NumbersFromInstance()
        {
            return NumbersInInstance;
        }

        public void AddNew(int num)
        {
            NumbersInType.Add(num);
            NumbersInInstance.Add(num);
        }
    }
```

![LoaderAndGcHeap drawio (3)](https://user-images.githubusercontent.com/55326490/180650856-e3259f12-8d09-4190-9459-5275e8d70d3a.png)


