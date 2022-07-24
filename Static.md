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

![LoaderAndGcHeap drawio (2)](https://user-images.githubusercontent.com/55326490/180650750-8ca93164-d7cd-4251-8df9-282451a063e8.png)


