New Toast Message

```java
Button btn=findViewById(R.id.btnAceptar);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Log.i("MyApp","This is a magic log message!");
                Toast.makeText(getApplicationContext(),"Es magico",Toast.LENGTH_SHORT)
                    .show();
            }
        });

```

New Activity

```java
public Button btn;
    public void init()
    {
        btn=findViewById(R.id.btnAceptar);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent toy=new Intent(MainActivity.this,second.class);
                startActivity(toy);
            }
        });
    }
```

```java
private Button button;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button=findViewById(R.id.button);
        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                abrirActividad2();
            }
        });
    }
    public void abrirActividad2()
    {
        Intent intent=new Intent(this, Third.class);
        startActivity(intent);
    }

```



# NEXUS VS ARTIFACTORY

