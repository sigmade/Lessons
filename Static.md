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

![LoaderAndGcHeap drawio (1)](https://user-images.githubusercontent.com/55326490/180648135-b551d5bc-f212-4c45-8573-bc724e17da17.png)


