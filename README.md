# PhoneMask
PhoneMask is full based on Kotlin language lightweight android library for EditText formatting. Easy way for add phone readability in your project.

## How to use it
Just use PhoneMaskManager class
```kotlin
 PhoneMaskManager()
                .withMask(" (###) ###-##-##")
                .withRegion("+7")
                .withValueListener(object : ValueListener{
                    override fun onPhoneChanged(phone: String) {
                       
                    }
                })
                .bindTo((findViewById(R.id.text_edit_text) as EditText))
```

### About methods
- withMask 
(required field)
Init your mask format. Use `#` symbol by default

- withRegion
(optional field)
Init your region

- withValueListener 
(optional field)
If you want to receive callback from EditText just add ValueListener, and you receive phone string in clear format 
(For example: +70009199191)

- bindTo 
(required calling)
Afrer setup just call this method for binding to `EditText`