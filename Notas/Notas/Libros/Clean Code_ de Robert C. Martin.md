Claro, aquí tienes ejemplos tanto sencillos como avanzados para complementar las notas de cada capítulo del libro "Clean Code":

---

# Clean Code - Notas

## Introducción
- **Autor**: Robert C. Martin (Uncle Bob)
- **Tema**: Mejores prácticas para escribir código limpio y mantenible.
- **Objetivo**: Enseñar a los desarrolladores a escribir código legible, fácil de mantener y libre de errores.

## Capítulo 1: Limpieza de Código
- **Código Limpio**:
  - Claro y directo.
  - Fácil de leer y entender.
  - Facilidad para hacer cambios sin introducir errores.
- **Código sucio**:
  - Difícil de leer y entender.
  - Propenso a errores cuando se modifica.
- **Ejemplo Sencillo**:
  ```java
  // Código limpio
  public List<Employee> getEmployees() {
      return employeeRepository.findAll();
  }

  // Código sucio
  public List<Employee> getEmp() {
      List<Employee> emps = new ArrayList<>();
      for (Employee e : employeeRepository.findAll()) {
          emps.add(e);
      }
      return emps;
  }
  ```

## Capítulo 2: Nombres Significativos
- **Importancia de los nombres**:
  - Los nombres deben revelar intención.
  - Usar nombres precisos y específicos.
- **Reglas para buenos nombres**:
  - Nombrar variables, funciones y clases de manera que describan su propósito.
  - Evitar abreviaciones y nombres crípticos.
  - Usar terminología del dominio del problema.
- **Ejemplo Sencillo**:
  ```java
  // Nombres significativos
  int elapsedTimeInDays;
  int daysSinceCreation;
  int fileAgeInDays;

  // Nombres poco claros
  int d;
  int elapsed;
  int fileAge;
  ```
- **Ejemplo Avanzado**:
  ```java
  // Nombres significativos en una función avanzada
  public class OrderProcessor {
      public void processOrder(Order order) {
          if (order.isPaid() && !order.isShipped()) {
              shipOrder(order);
          }
      }

      private void shipOrder(Order order) {
          // lógica de envío
      }
  }

  // Nombres poco claros en una función avanzada
  public class OrderProcessor {
      public void proc(Order o) {
          if (o.paid() && !o.ship()) {
              ship(o);
          }
      }

      private void ship(Order o) {
          // lógica de envío
      }
  }
  ```

## Capítulo 3: Funciones
- **Funciones pequeñas**:
  - Idealmente de 2-4 líneas.
  - Hacer una sola cosa y hacerlo bien.
- **Nombres claros y descriptivos**:
  - El nombre de la función debe describir su propósito y comportamiento.
- **Evitar efectos secundarios**:
  - Las funciones deben tener un comportamiento predecible.
- **Ejemplo Sencillo**:
  ```java
  // Función pequeña y clara
  public int calculateSum(int a, int b) {
      return a + b;
  }

  // Función grande y confusa
  public int performOperations(int a, int b) {
      int sum = a + b;
      System.out.println("Sum: " + sum);
      if (a > b) {
          sum += a - b;
      }
      return sum;
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Función pequeña y clara en una clase avanzada
  public class InvoiceCalculator {
      public double calculateTotal(Invoice invoice) {
          return calculateSubtotal(invoice) + calculateTax(invoice);
      }

      private double calculateSubtotal(Invoice invoice) {
          double subtotal = 0;
          for (Item item : invoice.getItems()) {
              subtotal += item.getPrice();
          }
          return subtotal;
      }

      private double calculateTax(Invoice invoice) {
          return calculateSubtotal(invoice) * 0.08;
      }
  }

  // Función grande y confusa en una clase avanzada
  public class InvoiceCalculator {
      public double calculateTotal(Invoice invoice) {
          double subtotal = 0;
          for (Item item : invoice.getItems()) {
              subtotal += item.getPrice();
          }
          double tax = subtotal * 0.08;
          return subtotal + tax;
      }
  }
  ```

## Capítulo 4: Comentarios
- **Comentarios útiles**:
  - Explicar por qué se tomó una decisión, no qué hace el código.
- **Comentarios dañinos**:
  - Comentarios obvios o redundantes con el código.
  - Comentarios desactualizados o incorrectos.
- **Ejemplo Sencillo**:
  ```java
  // Comentario útil
  // Este método calcula el total de ventas con descuentos aplicados
  public double calculateTotalSales(List<Sale> sales) {
      double total = 0;
      for (Sale sale : sales) {
          total += sale.getAmount() * (1 - sale.getDiscount());
      }
      return total;
  }

  // Comentario dañino
  // Suma los montos de las ventas
  public double sumSales(List<Sale> sales) {
      double total = 0;
      for (Sale sale : sales) {
          total += sale.getAmount();
      }
      return total;
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Comentario útil en un método avanzado
  // Este método envía una notificación de confirmación de pedido al cliente
  public void sendOrderConfirmation(Order order) {
      // Lógica para enviar notificación
      Notification notification = createNotification(order);
      notificationService.send(notification);
  }

  // Comentario dañino en un método avanzado
  // Enviar notificación
  public void sendNotification(Order order) {
      Notification notification = createNotification(order);
      notificationService.send(notification);
  }
  ```

## Capítulo 5: Formateo
- **Consistencia**:
  - Código consistentemente formateado facilita la lectura y mantenimiento.
- **Espacios y sangrías**:
  - Usar espacios y sangrías de manera coherente para mostrar la estructura lógica.
- **Agrupación**:
  - Agrupar líneas de código relacionadas para facilitar la comprensión.
- **Ejemplo Sencillo**:
  ```java
  // Formato consistente y claro
  public class Customer {
      private String name;
      private int age;

      public Customer(String name, int age) {
          this.name = name;
          this.age = age;
      }

      public String getName() {
          return name;
      }

      public int getAge() {
          return age;
      }
  }

  // Formato inconsistente y confuso
  public class Customer { private String name; private int age; public Customer(String name,int age) {this.name=name; this.age=age;} public String getName(){return name;} public int getAge(){return age;}}
  ```
- **Ejemplo Avanzado**:
  ```java
  // Formato consistente y claro en una clase avanzada
  public class OrderProcessor {
      private OrderRepository orderRepository;

      public OrderProcessor(OrderRepository orderRepository) {
          this.orderRepository = orderRepository;
      }

      public void process(Order order) {
          if (order.isPaid()) {
              ship(order);
          }
      }

      private void ship(Order order) {
          // lógica de envío
      }
  }

  // Formato inconsistente y confuso en una clase avanzada
  public class OrderProcessor { private OrderRepository orderRepository; public OrderProcessor(OrderRepository orderRepository) { this.orderRepository = orderRepository; } public void process(Order order) { if (order.isPaid()) { ship(order); } } private void ship(Order order) { // lógica de envío } }
  ```

## Capítulo 6: Objetos y Estructuras de Datos
- **Encapsulamiento**:
  - Mantener los datos privados y exponer solo lo necesario.
- **Objetos vs. Estructuras de Datos**:
  - Objetos combinan datos y comportamiento.
  - Estructuras de datos solo contienen datos.
- **Ejemplo Sencillo**:
  ```java
  // Objeto con encapsulamiento
  public class Rectangle {
      private double length;
      private double width;

      public Rectangle(double length, double width) {
          this.length = length;
          this.width = width;
      }

      public double getArea() {
          return length * width;
      }
  }

  // Estructura de datos sin encapsulamiento
  public class RectangleData {
      public double length;
      public double width;
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Objeto con encapsulamiento avanzado
  public class BankAccount {
      private String accountNumber;
      private double balance;

      public BankAccount(String accountNumber) {
          this.accountNumber = accountNumber;
          this.balance = 0;
      }

      public void deposit(double amount) {
          if (amount > 0) {
              balance += amount;
          }
      }

      public void withdraw(double amount) {
          if (amount > 0 && amount <= balance) {
              balance -= amount;
          }
      }

      public double getBalance() {
          return balance;
      }
  }

  // Estructura de datos sin encapsulamiento avanzado
  public class BankAccountData {
      public String accountNumber;
      public double balance;
  }
  ```

## Capítulo 7: Manejo de

 Errores
- **Excepciones vs. Códigos de error**:
  - Preferir el uso de excepciones en lugar de códigos de error.
- **Principio de Separación**:
  - Separar la lógica de manejo de errores de la lógica de negocios.
- **Clarity**:
  - Las excepciones deben ser claras y específicas.
- **Ejemplo Sencillo**:
  ```java
  // Uso de excepciones
  public void openFile(String filename) throws FileNotFoundException {
      File file = new File(filename);
      if (!file.exists()) {
          throw new FileNotFoundException("File not found: " + filename);
      }
      // lógica para abrir el archivo
  }

  // Uso de códigos de error
  public int openFile(String filename) {
      File file = new File(filename);
      if (!file.exists()) {
          return -1; // Error: archivo no encontrado
      }
      // lógica para abrir el archivo
      return 0; // Éxito
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Manejo de errores con excepciones avanzadas
  public class PaymentProcessor {
      public void processPayment(Payment payment) throws InsufficientFundsException, PaymentFailedException {
          if (payment.getAmount() > payment.getAccount().getBalance()) {
              throw new InsufficientFundsException("Insufficient funds for payment.");
          }

          // lógica para procesar el pago

          if (paymentFailed()) {
              throw new PaymentFailedException("Payment processing failed.");
          }
      }

      private boolean paymentFailed() {
          // lógica para determinar si el pago falló
          return false;
      }
  }

  // Manejo de errores con códigos de error avanzados
  public class PaymentProcessor {
      public int processPayment(Payment payment) {
          if (payment.getAmount() > payment.getAccount().getBalance()) {
              return -1; // Error: fondos insuficientes
          }

          // lógica para procesar el pago

          if (paymentFailed()) {
              return -2; // Error: procesamiento de pago fallido
          }

          return 0; // Éxito
      }

      private boolean paymentFailed() {
          // lógica para determinar si el pago falló
          return false;
      }
  }
  ```

## Capítulo 8: Límites
- **Interfaces de terceros**:
  - Encapsular el uso de bibliotecas de terceros para facilitar cambios futuros.
- **Pruebas**:
  - Escribir pruebas que simulen el comportamiento de componentes externos.
- **Ejemplo Sencillo**:
  ```java
  // Encapsulación de una biblioteca de terceros
  public class EmailService {
      private ThirdPartyEmailLibrary emailLibrary;

      public EmailService() {
          emailLibrary = new ThirdPartyEmailLibrary();
      }

      public void sendEmail(String to, String subject, String body) {
          emailLibrary.send(to, subject, body);
      }
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Encapsulación avanzada de una biblioteca de terceros
  public class PaymentGateway {
      private ThirdPartyPaymentProcessor paymentProcessor;

      public PaymentGateway() {
          paymentProcessor = new ThirdPartyPaymentProcessor();
      }

      public PaymentResponse processPayment(PaymentRequest request) {
          return paymentProcessor.process(request);
      }
  }
  ```

## Capítulo 9: Pruebas Unitarias
- **Importancia de las pruebas unitarias**:
  - Asegurar que el código funciona correctamente.
  - Facilitar la refactorización segura.
- **Principios de buenas pruebas**:
  - Rápidas, independientes, repetibles y automáticas.
- **Ejemplo Sencillo**:
  ```java
  @Test
  public void testCalculateSum() {
      Calculator calculator = new Calculator();
      int result = calculator.calculateSum(2, 3);
      assertEquals(5, result);
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  @Test
  public void testProcessPayment() {
      PaymentProcessor paymentProcessor = new PaymentProcessor();
      Payment payment = new Payment(100, new Account(200));

      try {
          paymentProcessor.processPayment(payment);
      } catch (Exception e) {
          fail("Payment processing should not throw an exception");
      }

      assertEquals(100, payment.getAccount().getBalance(), 0);
  }
  ```

## Capítulo 10: Clases
- **Principio de Responsabilidad Única**:
  - Una clase debe tener una sola responsabilidad.
- **Encapsulación**:
  - Mantener los detalles internos de la clase ocultos.
- **Cohesión**:
  - Los métodos de una clase deben estar relacionados y trabajar juntos.
- **Ejemplo Sencillo**:
  ```java
  // Clase con una sola responsabilidad
  public class User {
      private String name;
      private String email;

      public User(String name, String email) {
          this.name = name;
          this.email = email;
      }

      public String getName() {
          return name;
      }

      public String getEmail() {
          return email;
      }
  }

  // Clase con múltiples responsabilidades (mala práctica)
  public class User {
      private String name;
      private String email;

      public User(String name, String email) {
          this.name = name;
          this.email = email;
      }

      public String getName() {
          return name;
      }

      public String getEmail() {
          return email;
      }

      public void sendEmail(String message) {
          // lógica para enviar un correo electrónico
      }

      public void saveToDatabase() {
          // lógica para guardar en la base de datos
      }
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Clase con una sola responsabilidad en un contexto avanzado
  public class Order {
      private List<Item> items;

      public Order(List<Item> items) {
          this.items = items;
      }

      public List<Item> getItems() {
          return items;
      }
  }

  public class OrderProcessor {
      public void process(Order order) {
          for (Item item : order.getItems()) {
              processItem(item);
          }
      }

      private void processItem(Item item) {
          // lógica para procesar el artículo
      }
  }

  // Clase con múltiples responsabilidades en un contexto avanzado (mala práctica)
  public class OrderProcessor {
      private List<Item> items;

      public OrderProcessor(List<Item> items) {
          this.items = items;
      }

      public List<Item> getItems() {
          return items;
      }

      public void process() {
          for (Item item : items) {
              // lógica para procesar el artículo
          }
      }

      public void sendNotification() {
          // lógica para enviar notificaciones
      }

      public void saveToDatabase() {
          // lógica para guardar en la base de datos
      }
  }
  ```

## Capítulo 11: Sistemas
- **Diseño de sistemas**:
  - Pensar en la arquitectura antes de escribir código.
  - Utilizar principios de diseño sólido.
- **Modularidad**:
  - Dividir el sistema en módulos independientes y cohesivos.
- **Ejemplo Sencillo**:
  ```java
  // Modularidad
  public class OrderService {
      private OrderRepository orderRepository;

      public OrderService(OrderRepository orderRepository) {
          this.orderRepository = orderRepository;
      }

      public void placeOrder(Order order) {
          orderRepository.save(order);
      }
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Diseño de sistemas avanzado con modularidad
  public class InventoryService {
      private InventoryRepository inventoryRepository;

      public InventoryService(InventoryRepository inventoryRepository) {
          this.inventoryRepository = inventoryRepository;
      }

      public void updateStock(Item item, int quantity) {
          inventoryRepository.update(item, quantity);
      }
  }

  public class OrderService {
      private OrderRepository orderRepository;
      private InventoryService inventoryService;

      public OrderService(OrderRepository orderRepository, InventoryService inventoryService) {
          this.orderRepository = orderRepository;
          this.inventoryService = inventoryService;
      }

      public void placeOrder(Order order) {
          orderRepository.save(order);
          for (Item item : order.getItems()) {
              inventoryService.updateStock(item, -item.getQuantity());
          }
      }
  }
  ```

## Capítulo 12: Emergent Design
- **Diseño emergente**:
  - El diseño debe evolucionar con el tiempo y ser refinado continuamente.
- **Simplicidad**:
  - Mantener el diseño lo más simple posible.
- **Pruebas**:
  - Las pruebas deben guiar el diseño y refactorización del código.
- **Ejemplo Sencillo**:
  ```java
  // Diseño emergente sencillo
  public class Calculator {
      public int add(int a, int b) {
          return a + b;
      }

      public int subtract(int a, int b) {
          return a - b;
      }
  }
  ```
- **Ejemplo Avanzado**:
  ```java
  // Diseño emergente avanzado
  public class ShoppingCart {
      private List<Item> items;

      public ShoppingCart() {
          this.items = new ArrayList<>();
      }

      public void addItem(Item item) {
          items.add(item);
      }

      public void removeItem(Item item) {
          items.remove(item);
      }

      public double getTotalPrice() {
          double total = 0;
          for (Item item : items) {
              total += item.getPrice

();
          }
          return total;
      }
  }

  public class DiscountedShoppingCart extends ShoppingCart {
      private double discountRate;

      public DiscountedShoppingCart(double discountRate) {
          super();
          this.discountRate = discountRate;
      }

      @Override
      public double getTotalPrice() {
          double total = super.getTotalPrice();
          return total * (1 - discountRate);
      }
  }
  ```

https://elhacker.info/manuales/Lenguajes%20de%20Programacion/Codigo%20limpio%20-%20Robert%20Cecil%20Martin.pdf