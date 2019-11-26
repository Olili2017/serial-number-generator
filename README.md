# Serial Number/ID Generator

[![](https://jitpack.io/v/Olili2017/serial-number-generator.svg)](https://jitpack.io/#Olili2017/serial-number-generator)

> Java library that generates random strings/serial numbers based on the options provided

## Adding serial number generator to your project

---

### Maven projects

Step 1: Add the JitPack repository to your build file

```xml
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
```

Step 2: Add the dependency

```xml
<dependency>
	<groupId>com.github.Olili2017</groupId>
	<artifactId>serial-number-generator</artifactId>
	<version>v1.0.0</version>
</dependency>
```

### Gradle projects

Step 1: Add it in your root build.gradle at the end of repositories:

```gradle
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```

Step 2: Add the dependency

```gradle
dependencies {
	implementation 'com.github.Olili2017:serial-number-generator:v1.0.0'
}
```

## Usage

---

By default, the serial number length is 4 charactors. ie. If no string length is specified.

> ### Example with no string length specified

```java
// Generate a 4 charactor long serial number
String serialNumber = new SerialNumberGenerator().generate();
```

Sample result : ```DBDA```

> ### Specifying the length of generated output string

Sometimes we need more charactors in our serial numbers. below is an example on how to achieve this with ```serial-number-generator```

```java
// Generate a custom length serial number

String serialNumber;
int serialNumberLength = 8; // change this prefered length

serialNumber = new SerialNumberGenerator(serialNumberLength)
				.generate();

```

Sample result : ```BEEGHEGG```

> ### Specifying a separator in output string

Often times we need charactors separators in our serial numbers. Below is an example on how to achieve this with ```serial-number-generator```

#### Note : ```The length of the serial number must be divisible by the number of charactors```

```java
// Generate a custom length serial number with separators

String serialNumber;
int serialNumberLength = 16; // change this prefered length
int splitInto = 4; // number of equal parts in the string output
char separator = '-'; // can be any charactor even spaces

serialNumber = new SerialNumberGenerator(serialNumberLength)
				.split(splitInto,separator)
				.generate();

```

Sample result : ```OALI-OIBL-GFPK-FBAC```



---

## License

MIT License

Copyright &copy; 2019 Daniel Olili

---

## Author Info

- Twitter - [@olilidaniel](https://twitter.com/olilidaniel)
- Website - [Daniel Olili](https://olili.netlify.com)
- LinkedIn - [daniel olili](https://www.linkedin.com/in/daniel-olili-93029b111/)