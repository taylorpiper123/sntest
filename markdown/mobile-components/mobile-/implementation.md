
# Implementation

---

  
**Android**  
```kotlin  
class MainActivity : AppCompatActivity() {
    @SuppressLint("UnusedMaterialScaffoldPaddingParameter")
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        setContent {
            Scaffold(
                topBar = { TopAppBar(
                    title = {
                        Text(text ="IconButton From Vector Resources")
                    }
                )},
                content = { MainContent() },
                backgroundColor = Color(0xFFFEFEFA)
            )
        }
    }  
```  
  
**IOS**  
```swift  
guard let scene = view.window?.windowScene else { return }
let config = SKOverlay.AppConfiguration(appIdentifier: "your-app-id", position: .bottom)
let overlay = SKOverlay(configuration: config)
overlay.present(in: scene)  
```  
