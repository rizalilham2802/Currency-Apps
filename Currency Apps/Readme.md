# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap senilai Rp.15.000

## Scope & Functionalities
 - user dapat memasukkan angka
 - user dapat menyentuh tombol hitung 
 - user dapat mendapat info "INVALID" jika yang dimasukkan sebuah text

## How Does it works?

Diawali dari method `MainWindow` pada class MainWindow.xaml.cs, kita mendeklarasikan CurencciControler setelah itu menginitialize di mainwindow karena metod yang pertama kali di eksekusi saat aplikasi berjalan

```javascript
        public MainWindow()
        {
            InitializeComponent();
            currencyController = new CurrencyController();
        }
```

Logika perhitungan terdapat pada class `CurencyController.cs` sebagai berikut
Cara kerjanya pada saat user menginputkan nilai maka akan di kalikan dengan 15000
```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```