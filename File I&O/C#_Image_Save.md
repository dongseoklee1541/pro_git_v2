C#에서 이미지를 저장하는 메서드는 Image.Save가 있다. 이 메서드는 여러가지의 메소드를 오버로드 받는다.

---
* Save(String, ImageCodecInfo, EncoderParameters)	: 지정된 인코더 및 이미지 인코더 매개 변수를 사용하여 이 Image를 지정된 파일에 저장합니다.
* Save(Stream, ImageCodecInfo, EncoderParameters)	: 지정된 인코더 및 이미지 인코더 매개 변수를 사용하여 이 이미지를 지정된 스트림에 저장합니다.
* Save(String, ImageFormat)	: 이 Image를 지정된 형식으로 지정된 파일에 저장합니다.
* Save(Stream, ImageFormat)	: 이 이미지를 지정된 형식의 지정된 스트림에 저장합니다.
* Save(String) : 이 Image를 지정된 파일이나 스트림에 저장합니다.
---

내가 궁금한 것은 **Save(String)** 의 경우 String 안에 있는 확장자의 이름에 따라서 알아서 포멧에 맞춰서 저장을 해주는가였다.
(예를 들어 String에 "case.jpg","case.bmp" 라면 각각 jpg와 bmp 방식으로 인코딩을 해주는 것인가?)
