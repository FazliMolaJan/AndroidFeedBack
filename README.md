# Android Feed Back 

[![platform](https://img.shields.io/badge/platform-Android-yellow.svg)](https://www.android.com)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0.html)


<p align="center">
<img src="https://github.com/mejdi14/AndroidFeedBack/tree/master/photos/feedback.gif" height="250" width="300" >
	</p>

## Installation

Add this in your root `build.gradle` file (**not** your module `build.gradle` file):

```gradle
allprojects {
	repositories {
		...
		maven { url "https://jitpack.io" }
	}
}
```
## Dependency

Add this to your module's `build.gradle` file (make sure the version matches the JitPack badge above):

```gradle
dependencies {
	...
	implementation 'com.github.mejdi14:Flat-Dialog-Android:1.0.4'
}
```

## Screenshots
<img src="https://github.com/mejdi14/Flat-Dialog-Android/blob/master/screenshots/image1.jpg" height="420" width="260" hspace="20"><img src="https://github.com/mejdi14/Flat-Dialog-Android/blob/master/screenshots/image2.jpg" height="420" width="260" hspace="20"><img src="https://github.com/mejdi14/Flat-Dialog-Android/blob/master/screenshots/image3.jpg" height="420" width="260">
<img src="https://github.com/mejdi14/Flat-Dialog-Android/blob/master/screenshots/image4.jpg" height="420" width="260" hspace="20"><img src="https://github.com/mejdi14/Flat-Dialog-Android/blob/master/screenshots/image5.jpg" height="420" width="260" hspace="20">

## How to use

``` java
 final FlatDialog flatDialog = new FlatDialog(ExempleActivity.this);
        flatDialog.setTitle("Login")
                .setSubtitle("write your profile info here")
                .setFirstTextFieldHint("email")
                .setSecondTextFieldHint("password")
                .setFirstButtonText("CONNECT")
                .setSecondButtonText("CANCEL")
                .withFirstButtonListner(new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        Toast.makeText(ExempleActivity.this, flatDialog.getFirstTextField(), Toast.LENGTH_SHORT).show();
                    }
                })
                .withSecondButtonListner(new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        flatDialog.dismiss();
                    }
                })
                .show();
```

## More useful methods
<table>
  <tr>
    <th>Method</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>isCancelable(boolean)</td>
    <tdDefine if you want to close dialog when you click outside</td>
  </tr>
  <tr>
    <td>setIcon(image)</td>
    <td>Add an image at the top of the dialog</td>
  </tr>
	  <tr>
    <td>setBackgroundColor(color)</td>
    <td>Change the dialog background color</td>
  </tr>
  <tr>
    <td>setFirstTextFieldHint(String)</td>
    <td>Set a hint for the edittext</td>
  </tr>
  <tr>
    <td>setFirstTextFieldTextColor(color)</td>
    <td>Set the edittext text color<br></td>
  </tr>
  <tr>
    <td>setFirstTextFieldBorderColor(color)</td>
    <td>Set the border color for the edittext</td>
  </tr>
	 <tr>
    <td>setFirstTextFieldInputType(type)</td>
    <td>Set the input type for the edittext</td>
  </tr>
		 <tr>
    <td>setFirstButtonColor(color)</td>
    <td>Set the button background color</td>
  </tr>
</table>

## Contributing

Any contributions, large or small, major features, bug fixes, are welcomed and appreciated