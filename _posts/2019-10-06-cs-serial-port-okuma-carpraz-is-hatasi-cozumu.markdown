---
layout: post
title: "Serial Port Çarpraz İş Parçacığı (Cross-Thread) Okuma Hatası Visual Studio / C#"
lang: tr
tags: ["csharp", "c#", "hata", "ipucu", "çözüm", "serial port", "thread"]
categories: ["tip&tricks"]
---

## C#'ta Serial Port Bağlarken Karşılaşılan Zorluklar ve Çözümleri

Serial Port'tan veriyi alıp okuyacak ve kullanacak şekilde çözümünüzü ayarladınız ama aşağıdaki hatalardan biriyle karşılaştınız:

1. Form'unuz veya Console App'iniz kilitlendi ve cevap vermiyor. Bunun için [çözüm 1](#cozum1).

2. Uygulamanız çalışıyor ama debug kısmında Cross-Thread (çarpraz iş parçacığı) hatasını görüyorsunuz. Bunun için [çözüm 2](#cozum2)

## <a name="cozum1"></a> Çözüm 2

Öncelikle aşağıdaki değerin uygulamanız için false olduğuna emin olun ki, illegal çarpraz iş parçacığı işlemlerinde size hata versin.

```cs
System.Windows.Forms.Form.CheckForIllegalCrossThreadCalls = false
```
Ve çözüm 2'ye geçin.

## <a name="cozum2"></a> Çözüm 2

DataReceived içine aşağıdaki gibi bir çözümü ekleyerek sorununuzu kolayca çözebilirsiniz.

```cs
private void SerialPortQR_DataReceived(object sender, SerialDataReceivedEventArgs e)
{
    this.Invoke(new EventHandler(invokeThread)); 
}
private void invokeThread(object s, EventArgs e) {
	//Yapacağınız işlemleri bu kısımda yapınız.
}
```