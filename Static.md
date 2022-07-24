``` C#
public class InMemoryDataProvider
    {
        private static List<int> NumbersInType = new List<int>();
        // Only instance field without static
        private List<int> NumbersInInstance = new List<int>();

        public List<int> GetNumbersFromType()
        {
            return NumbersInType;
        }
        // Invoke method without create instance
        public static List<int> GetNumbersFromTypeStatic()
        {
            return NumbersInType;
        }

        public List<int> GetNumbersFromInstance()
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
