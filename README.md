# Welcome to C# Note Book!

**Tổng hợp ngắn gọn tất cả các kiến thức liên quan đến C#.Net**

## Tổng hợp về máy tính

### Các thành phần chính của máy tính

-   **CPU - Central Processing Unit (Bộ xử lý trung tâm)**: Trái tim của máy tính. Bao gồm ALU (thực hiện các phép toán và logic số học cơ bản) và CU (giúp sử dụng các tài nguyên một cách hiệu quả).
-   **Main memory (Bộ nhớ chính - RAM)**: CPU không thể truy cập ổ cứng mà chỉ có thể truy cập  _main memory_. Vì vậy Program file cần được đưa từ  _ổ cứng_  vào  _main memory_  để CPU có thể thực thi.
-   **Hard disk (Ổ đĩa cứng)**: Thiết bị lưu trữ của máy tính. Bao gồm  *program files*  và  *data files*.
-   **Input devices (Thiết bị đầu vào)**: Tất cả điều gì được nhập từ bàn phím sẽ được lưu trong  _input buffer_  (bộ đệm đầu vào). Program sẽ đọc input từ  _input buffer_. Ex: Chuột, bàn phím, ...
-   **Output devices (Thiết bị đầu ra)**: Tất cả đầu ra sẽ được lưu trong  _output buffer_  (bộ đệm đầu ra) và sẽ được xuất ra. Ex: Loa, màn hình, ...

### Software

-   Là tập hợp các chương trình sử dụng tài nguyên của  _Hardware components  (các thành phần của phần cứng)_.
-   Có 2 loại phần mềm:
    -   **System software (Phần mềm hệ thống):** Bao gồm  *Operating system*  (DOS, WINDOWS, LINUX, UNIX),  *System support*  (compiler, interpreter, Assembler),  *System development*  (Linker, Loader, Editor).
    -   **Application software:** Bao gồm  *Application-Specific*  (MS OFFICE, Oracle) và  *General Purpose Software*  (Tally).

### Ngôn ngữ lập trình cấp cao và cấp thấp

-   Ngôn ngữ lập trình cấp thấp (Hệ thống có thể dễ dàng hiểu được):  **Machine Language**  &  **Assembly Language**  (hợp ngữ).
-   Ngôn ngữ lập trình cấp cao: Phụ thuộc vào người dùng.

### Cách hoạt động của các chương trình máy tính

- Translators (trình dịch) là phần mềm hệ thống chuyển đổi code sang mã nhị phân. Nó được chia thành ba loại: **compiler** (biên dịch), **Interpreter** (trình thông dịch), **Assembler** (cách làm việc giống với biên dịch).
- So sánh:
	| Tiêu chí | Trình biên dịch | Trình thông dịch |
	|--|--|--|
	| Định nghĩa | Trước khi chạy, chương trình sẽ dịch toàn bộ thành mã máy rồi mới tiến hành thực thi | Khi chạy chương trình, ngôn ngữ mới được dịch sang ngôn ngữ máy và thực thi |
	| Đầu vào | Toàn bộ chương trình | Chỉ một dòng code |
	| Đầu ra  | Mã đối tượng trung gian | Không tạo ra bất kỳ mã đối tượng trung gian nào |
	| Cơ chế hoạt động | Việc biên dịch sẽ phải hoàn thành công việc trước khi thực thi | 			Việc biên dịch và thực thi sẽ là đồng thời
	| Tốc độ | Nhanh hơn | Chậm hơn |
	| Bộ nhớ | Yêu cầu bộ nhớ nhiều hơn do việc tạo mã đối tượng | Nó đòi hỏi ít bộ nhớ 	hơn vì nó không tạo mã đối tượng trung gian
	| Errors | Hiển thị tất cả các lỗi sau biên dịch, tất cả cùng một lúc | Hiển thị lỗi của từng dòng một
	| Phát hiện error | Rất khó khăn | Tương đối dễ |
	| Các ngôn ngữ lập trình | C, C++, C#, Scala, TypeScript | PHP, Perl, Python, Ruby
- **Operating system** - OS (hệ điều hành): Giao diện giữa người dùng máy tính và phần cứng máy tính.
    -   **Loader** (bộ nạp): Tải machine code vào bộ nhớ hệ thống.
    -   **Linker** (trình liên kết): Liên kết các chương trình nhỏ hơn để tạo thành một chương trình duy nhất (một chương trình dài được chia thành nhiều module).

### Các loại Applications khác nhau

-   Có 2 loại ứng dụng:
    -   **Standalone applications** (ứng dụng độc lập): Các ứng dụng được cài đặt trên máy tính, luôn phụ thuộc vào hệ điều hành (Ex: Chrome, Excel, ...).
    -   **Web applications** (ứng dụng web): Các ứng dụng không cần cài đặt trên máy tính, độc lập với hệ điều hành, không phụ thuộc vào một hệ điều hành cụ thể (Ex: facebook.com, gmail.com, ...).
-   **Operating System extensions**: Window => .exe, Mac => .dmg, Linux => .rpm.
> Tất cả các ngôn ngữ lập trình đều là ứng dụng độc lập.

## C#.NET

### Các thành phần chính của .NET framework

   -   **Common Language Runtime**(CLR): Thành phần máy ảo cơ bản của .NET. Là run-time giúp quá trình phát triển dễ dàng hơn. Giúp quản lý mã và quản lý thực thi các chương trình .NET.
   -   **Framework Class Library**(FCL) - (còn được gọi là Assemblies): Tập hợp các library, method và các class oop. => Cài đặt .NET framework về cơ bản là cài đặt CLR và FCL vào hệ thống.

### C#.NET Basics

#### 1. Data Types in C#

- **Value data types**: lưu trực tiếp giá trị của biến trong bộ nhớ, chấp nhận cả chữ có dấu và không dấu.
	- Predefined types: sbyte, int, bool, char, double, float, long, short, decimal, etc.
	- User defined types: enum, struct.
- **Pointer data type**: Chứa địa chỉ bộ nhớ của giá trị biến. Sử dụng dấu `&`  để xác định địa chỉ của một biến và dấu `*` để truy cập giá trị của một địa chỉ.
- **References data types**: chứa địa chỉ bộ nhớ của giá trị biến, không lưu trực tiếp giá trị biến trong bộ nhớ.
	- Predefined types: object, string.
	- User defined types: class, interface, delegate.
- Cách lấy size của kiểu dữ liệu định trước: `sizeof(dataType);`
- Cách lấy default value: `default(dataType);`

#### 2. Operators

-   Toán tử (a++): Gọi là  **postfix**.
-   Toán tử (++a) =>  **prefix**.
-   Cách xử lý **postfix** và **prefix** nằm trong 1 biểu thức hỗn hợp:
    -   B1: Ưu tiên xử lý **prefix** trước.
    -   B2: Thực hiện các phép toán còn lại.
    -   B3: Gán giá trị cho biến bên trái dấu bằng.
    -   B4: Tiến hành tính **postfix**.
-   Độ ưu tiên toán tử:
    -   TT1: Toán tử đơn:  `+, -, ++, --`.
    -   TT2: Các toán tử số học:  `*, /, +, -`.
    -   TT3: Các toán tử quan hệ:  `>, <, >=, <=, ==, !=`.
    -   TT4: Các toán tử luận lý:  `&&, ||, ?:`.
    -   TT5: Các toán tử gán:  `=, *=, /=, +=, -=`.
> Nên dùng ngoặc tròn để quy định biểu thức nào sẽ được thực hiện trước
> để tránh nhầm lẫn. 

#### 4. Loop

-  **break**: Thoát khỏi vòng lặp trực tiếp chứa nó.
-  **continue**: Kết thúc sớm một vòng lặp.
-  **foreach**:
	```C#
	foreach(<bien_lap> in <mang, tap  hop>)
	{
		<Cong  viec>;
	}
	```
-  **do ... while**: Phù hợp với suy nghĩ tự nhiên khi thiết kế thuật toán.
-  **while**: khắc phục một số trường hợp lỗi của **do ... while**.
-  **for**: Cách viết ngắn gọn của **while**, sử dụng khi điều kiện lặp phụ thuộc vào biến lặp và số lần lặp có thể biết trước.
-  **foreach**: duyệt đối tượng trong tập danh sách.

#### 5. Function

- Hàm có thể có giá trị trả về hoặc không.
- Hàm không có giá trị trả về được gọi là thủ tục (procedure).
- Khai báo hàm:

  ```C#
  <kieu_tra_ve> <ten_ham>(<kieu_bien_1> <tham_so_1>, ...)
  {
    Noi_dung_ham;
    [return <gia_tri_tra_ve>];
  }

  <ten_ham> (value1, value2);
  // <tham_so_1>: Tham so hinh thuc
  // value1, value2: Tham so thuc 
  ```

- Đặt tên hàm nên dùng động từ.
- Tham trị, tham chiếu:
  - **Truyền tham trị** (call by value):
    - Sao chép giá trị của **đối số** vào **tham số hình thức** của hàm. Sau khi thoát khỏi hàm.
    - **Đối số** được truyền vào vẫn giữ nguyên giá trị gốc (những thay đổi của tham số **không ảnh hưởng** đến giá trị của đối số).
  - **Truyền tham chiếu** (call by reference):
    - Sao chép địa chỉ của **đối số** vào **tham số hình thức**.
    - Những thay đổi đối với **tham số** sẽ có tác dụng lên **đối số**.
    - Sử dụng từ khóa `ref` hoặc `out`.
    - Tham số kiểu đa trị (mảng, đối tượng, ...) mặc định là truyền tham chiếu (không cần dùng từ khóa `ref` hoặc `out`).
  - Sự khác biệt giữa `ref` và `out`:
    - `ref` bắt buộc phải khởi tạo giá trị cho biến trước khi vào hàm.
    - `out` bắt buộc phải gán giá trị cho biến trước khi thoát khỏi hàm.

#### 6. Commonly used library

- Thư viện nhập / xuất Console:
  - Xuất thông báo ra màn hình console: `Console.WriteLine(...);`, `Console.Write(...);`.
  - Nhập dữ liệu từ bàn phím: `Console.ReadLine(...);`.
- Chuyển kiểu dữ liệu (Parse): `int.Parse(...);`, `Convert.ToInt32();`.
- Toán học (Math): `Math.PI`, `Math.Sqrt(x)`, `Math.Pow(x, y)`, `Math.Min(x, y)`, `Math.Max(x, y)`, `Math.Round(5.674, 1)`, `Math.Sin()`, `Math.Cos()`, ...
- Ngẫu nhiên (random):

  ```C#
    Random rd = new Random();
    // [0...90]
    int x = rd.Next(0, 100);
    // [-50...101]
    int z = rd.Next(-50, 102);
    // [0...1)
    double r = rd.NextDouble();
  ```

- Ngày tháng (DateTime):

  ```C#
    DateTime birthday = new DateTime(2002, 09, 13);
    Console.WriteLine(birthday.ToString("dd/MM/yyyy"));

    // Chuyen doi ve DateTime
    DateTime d = DateTime.Parse("20/10/2022");
  ```

#### 7. Debug in C#

- Debug để tìm ra nguyên nhân dẫn đến các lỗi khác nhau như: Lỗi biên dịch, lỗi lúc thực thi, lỗi sai logic, ...
- Cách theo dõi giá trị biến khi gỡ lỗi:
  - **Cửa sổ Locals**: tự động liệt kê danh sách các biến của method đang thực thi.
  - **Cửa sổ Watch**: cho phép nhập vào biến hoặc biểu thức cần xem xét.
  - **Cửa sổ Immediate**: cho phép thực hiện một câu lệnh nào đó ngoài đoạn mã đang debug mà không ảnh hưởng đến bước debug hiện tại.
  - **Cửa sổ Call Stack**: cho phép xem trình tự được gọi của các phương thức sau khi phương thức chứa dòng lệnh hiện hành thực hiện xong.
- Thực thi dòng lệnh khi gỡ lỗi:
  - **Step Over** (F10): thực hiện các dòng lệnh kế tiếp một cách tuần tự. Trong các dòng lệnh đi qua nếu gặp một method nào đó thì sẽ thực thi toàn bộ phương thức như một dòng lệnh thông thường (_không đi sâu vào method_).
  - **Step Info** (F11): Giống **Step Over** nhưng khi gặp method sẽ chạy từng dòngs lệnh trong method đó.
  - **Step Out** (Shift + F5): Thực hiện tất cả các lệnh còn lại trong method khi sử dụng **Step Info**.
  
#### 8. Xử lý biệt lệ

- Kiểm soát các biệt lệ giúp cho phần mềm tiếp tục hoạt động nếu lỗi xảy ra (lỗi phát sinh trong coding, ApplicationException, SystemException) hoặc cũng đưa ra các gợi ý bên phía User Problem.
- Các cấp độ lỗi thường gặp:
  - Lỗi biên dịch
  - Lỗi runtime exception
  - Logic exception - sai nghiệp vụ yêu cầu.
- **Unchecked error**: Có lỗi ko quan tâm và tắt ngang phần mềm.
- **Checked error**: Có lỗi xuất thông báo lỗi nhưng không tắt ngang phần mềm.
- **throw** statement: Thấy lỗi nhưng không xử lý luôn mà ném đi một nơi khác (thường sử dụng trong xử lý file, làm thư viện).
- **finally**: Luôn luôn được thực hiện.
- Có thể tự định nghĩa một class Exception kế thừa từ `ApplicationException` để có thể tái sử dụng code.
- **Error provider**: Kiểm soát biệt lệ dựa trên nhập liệu của người dùng.

#### 9. String

##### Kiểu char

- Lưu trữ ký tự Unicode 16-bit.
- Kiểu trong .NET framework: `System.Char`.
- Cách chuyển từ int => char: `char chr = (char)65 // Ký tự 'A'`.
- Chuyển kiểu:
  - char.Parse(string)
  - Convert.ToChar(string)
  - Chý ý: Chuỗi đưa vào chỉ có 1 ký tự, nếu nhiều ký tự => error.
- So sánh kiểu:
  - So sánh 2 ký tự, trả về hiệu số giữa 2 ký tự. Ex:

    ```C#
    char chr1 = 'A';
    char chr2 = 'B';

    Console.WriteLine(chr1.CompareTo(chr2)); // -1 (chr1 - chr2)
    ```

  - So sánh trả về boolean (return **true** nếu 2 ký tự **bằng nhau**, **false** nếu **không bằng**). Ex:

    ```C#
    char ch1 = 'A';
    char ch2 = (char)65;
    char ch3 = 'B';
    Console.WriteLine(ch1.Equals(ch2)); // true
    Console.WriteLine(ch1.Equals(ch3)); // false
    ```

- Kiểm tra **char**:
  - `Char.IsDigit(ch)`: **True** nếu **ch** là chữ số.
  - `Char.IsLetter(ch)`: **True** nếu **ch** là chữ cái.
  - `Char.IsNumeric(ch)`: **True** nếu **ch** là chữ số Unicode.
  - `Char.IsWhiteSpace(ch)`: **True** nếu **ch** là khoảng trắng.
  - `Char.IsLower(ch)`: **True** nếu **ch** là chữ thường.
  - `Char.IsUpper(ch)`: **True** nếu **ch** là chữ hoa.
- Thao tác với **char**:
  - `Char.ToLower(char)`: Chuyển ký tự chữ hoa sang chữ thường.
  - `Char.ToUpper(char)`: Chuyển ký tự chữ thường sang chữ hoa.

##### Kiểu string

- **string** là mảng các ký tự thuộc kiểu **char**
- Kiểu trong .NET framework: `System.string`.
- Escape character (ký tự đặc biệt):
  - Tab: `"\t"`
  - Xuống hàng: `"\n"`
  - Backslash: `"\\"`
- Khai báo nguyên văn: thêm dấu '@'. Ex: `string str2 = @"C:\Windows";`
- Chuyển đổi sang **string**:
  - `ToString()`: Trả về chuỗi ứng với nội dung của biến.
  - `Convert.ToString(obj)`.
- Thao tác với **string**:
  - `ToCharArray()` hoặc `[]`: Return về mảng các ký tự trong chuỗi. Ex:

    ```C#
    string str1 = "Hello";
    // Return ký tự e
    char ch1 = str1.ToCharArray()[1];
    Console.WriteLine(ch1); // e
    ```

  - `Lenght`: Return số ký tự trong chuỗi. Ex: `varName.Length;`.

##### Các hàm xử lý string

- **CompareTo**: So sánh chuỗi đang xét với chuỗi _value_. Hai chuỗi bằng nhau (return 0), lớn hơn (return 1), nhỏ hơn (return -1). Ex:

  ```C#
  string s = "Hello";
  int i = s.CompareTo("hello"); // i = 1
  int i = s.CompareTo("Hello"); // i = 0
  ```

- **Constains**: Trả về **True** nếu trong chuỗi đang xét có chứa chuỗi _value_, trả về **False** nếu ngược lại. Ex:

  ```C#
  string s = "Hello";
  bool i = s.Constains("lo");  
  ```

- **CopyTo**: Copy ký tự tùy ý sang một mảng khác. Ex:

  ```C#
  string s = "hello";
  char[] ch = new char[5];
  char[0] = 'a';
  char[1] = 'b';
  s.CopyTo(1, ch, 2, 3);
  Console.WriteLine(ch);  // "abello"
  ```

- **EndsWith()**: Return **true** nếu chuỗi được chỉ định là **kết thúc** của chuỗi đang xét. Ex:

  ```C#
  string s = "hello";
  bool result = s.EndsWidth("lo");  // true
  ```

- **StartsWith(string)**: Ngược lại **EndsWith()**.

- **string.Format()**: Trả về chuỗi được xây dựng từ `{<value i>: <kieu format>}`. Ex:

  ```C#
  string s = "hello";
  int n = 9;
  s = string.Format("Giá trị n = {0:N}, căn bậc 2 là: {1:N}", n, Math.Sqrt(n));
  Console.WriteLine(s); // Giá trị n = 9, căn bậc 2 là: 3
  s = string.Format("Giá sản phẩm là: {0:C}", 200);
  Console.WriteLine(s); // Giá sản phẩm là: $200
  ```

- **Insert(index, string)**: Chèn một chuỗi vào vị trí được chỉ định. Ex:

  ```C#
  string s = "hello";
  string val = "everybody";
  s = s.Insert(5, val);
  Console.WriteLine(s);
  ```

- **IndexOf(character/string)**: Trả về vị trí xuất hiện đầu tiên của ký tự hoặc chuỗi. Return -1 nếu không tìm thấy.
- **LastIndexOf(character/string)**: Trả về vị trí xuất hiện cuối cùng.
- **PadLeft(width, character)**: Trả về chuỗi với số ký tự được chỉ định, chuỗi ban đầu sẽ được đặt bên phải. Ex:

  ```C#
  string s = "Hello!";
  string s_leftAligned = s.PadLeft(10, "*");
  Console.WriteLine(s_leftAligned); // "*****Hello!"
  ```

- **PadRight(width, character)**: Ngược lại với **PadLeft()**.
- **Remove(startIndex, count)**: Xóa _count_ ký tự khỏi chuỗi ban đầu, bắt đầu từ vị trí _startIndex_. Ex:

  ```C#
  string s = "Hello!";
  s = s.Remove(4, 3); // "Hell"
  ```

- **Replace(oldStr, newStr)**: Thay thế chuỗi con _oldStr_ ban đầu bằng chuỗi bằng chuỗi con mới _newStr_.

  ```C#
  string s = "Hello!";
  s = s.Replace("ll", "r"); // "Hero"
  ```

- **Substring(startIdx, count)**: Lấy ra chuỗi con từ bên trong chuỗi gốc với vị trí bắt đầu _startIdx_ và số phần tử được chỉ định _count_. Ex:

  ```C#
  string s = "Hello!";
  s = s.Substring(1, 3); // "ell";
  ```

- **ToLower()**: Return về chuỗi có kiểu chữ thường từ chuỗi ban đầu.
- **ToUpper()**: Return kiểu chữ hoa.
- **Trim()**: Bỏ khoảng trắng ở đầu và cuối một chuỗi.
- **TrimEnd()**: Chỉ bỏ khoảng trắng ở cuối.
- **TrimStart()**: Chỉ bỏ khoảng trắng ở đầu.
- **Split(separator)**: Trả về mảng các chuỗi con được phân cách bởi _Separator_. Ex:

  ```C#
  string str = "mot,hai,ba";
  string[] str2 = str.Split(',');
  ```

- **Join(separator, value)**: Nối các chuỗi trong mảng _value_ thành 1 chuỗi, phân cách bởi _separator_.

  ```C#
  string[] array = new string[3];
  array[0] = "mot";
  array[1] = "hai";
  array[3] = "ba";
  string str = string.join("*", array);
  ```

#### 10. Array

- Khai báo mảng: `DataType[] arrayName;`.
- Khởi tạo mảng: `arrayName = new DataType[so_phan_tu];`.
- Khởi tạo và gán luôn giá trị cho mảng: `arrName = new DataType[3]{5, 6, 7};`.
- Xác định số phần tử của mảng: `arrName.Length`.
- Không nên duyệt mảng bằng **foreach** khi:
  - Cần duyệt một phần trong mảng (ví dụ duyệt từ phần tử t2 => t10).
  - 