# Adafruit-Weather-Icon
Weather icon for adafruit GFX font.

In order to use it, simply use Adafruit_GFX.h

```
#include <Adafruit_GFX.h>     // For Font
#include <Adafruit_SSD1306.h> // For the screen
```

Then Init your screen 

```
Adafruit_SSD1306 display(OLED_RESET);
```

Finally use it :)

```

void testdrawchar(void) {
	display.setTextSize(1);				// Set font size to defaut
	display.setTextColor(WHITE);		
	display.setFont(&Weathericon);		// Change font 

	for (uint8_t i=32; i < 96; i++) { 	// Loop on each character available 
		display.setCursor(10,20);		// Just cause Icon are pretty "big"
		Serial.println(i);				
		display.write(i);
		display.display();
		delay(200);						
		display.clearDisplay();
	}
}
```


