# Optional-Java-8

Optional is Final Class, which is inside this class when we check static methods.

Customer customer = new Customer(101,  "john",  null,  Arrays.asList("123","321");    --> Here email field is null.

1. empty --> It returns an empty Optional instance.

   Optional<Object> emptyOptional = Optional.empty();
   System.out.println(emptyOptional);

   Returns -> Optional.empty.

2. of(T value)  --> it return an Optional with specified present non-null values.

   Optional<String> emailOptional = Optional.of(Customer.getEmail());    ---> it will return NullPointerException.
   System.out.println(emailOptional);

   Note:

   To avoid this null pointer exception, we have another method : ofNullable();

3. ofNullable( T value)  -->  it returns a specified value, if non-null otherwise returns an empty Optional.

   Optional<String> ofNullableOption = Optional.ofNullable(customer.getEmail());
   System.out.println(ofNullableOption);  --> output : Optional.empty

   if we have email id -> then we are getting -> Optional[ABC]

   How to get exact value --> ofNullableOption.get()  --> if no value we are getting NoSuchElementException : No value present.

   We should not call directly to get the method. We will do it as below.

   if(ofNullableOption.isPresent()){
     System.out.println(ofNullableOption.get()));
   }

   --> You will get nothing if you run the above code.

   Extra Methods :

   Customer customer = new Customer(101,  "john",  null,  Arrays.asList("123","321");    --> Here email field is null.
   
   ofNullableOption.orElse("default@email.com");

   ofNullableOption.orElseThrow("() -> new IllegalArgumentException("email not present"));
   
   findAny()....
   findFirst()....
   
   
