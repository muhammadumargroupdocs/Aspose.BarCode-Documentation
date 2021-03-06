---
title: How to Integrate Aspose.BarCode for .NET with Aspose.PDF
type: docs
weight: 10
url: /net/how-to-integrate-aspose-barcode-for-net-with-aspose-pdf/
---

PDF documents have become a popular medium for generating reports or other official documents in many organizations. Aspose Pty Ltd. provides a component, [Aspose.PDF](https://products.aspose.com/pdf/net) to generate PDF documents on the fly. Developers can add barcodes to their PDF documents by integrating Aspose.BarCode with Aspose.PDF. This article will briefly describe the technique to integrate these two products together for adding high-quality barcode images to PDF documents. In this article, we will discuss creating a barcode image using Aspose.BarCode and then embed that barcode image to a PDF document generated by Aspose.PDF.
## **Creating the Barcode**
First of all, we will create an object of the BarcodeGenerator class. The desired data to be encoded into a barcode will be assigned to the CodeText property of the BarcodeGenerator object. The Code128 symbology will be selected from the Symbology enumeration and then assigned to the SymbologyType property of the BarcodeGenerator object as shown below:

{{< gist "aspose-com-gists" "f801733f5eb53b0777dd38da9db8366a" "Examples-CSharp-TechnicalArticles-CreatingBarCode-CreatingBarCode.cs" >}}
## **Save Barcode to MemoryStream**
Once the properties of the BarcodeGenerator object are configured then we can create and save the barcode image to a MemoryStream. For this purpose, we will create an instance of MemoryStream and then store the barcode image to this MemoryStream by calling the Save method of the BarcodeGenerator as shown below:

{{< gist "aspose-com-gists" "f801733f5eb53b0777dd38da9db8366a" "Examples-CSharp-TechnicalArticles-SaveBarCodeToMemoryStream-SaveBarCodeToMemoryStream.cs" >}}
## **Create a PDF Document using Aspose.PDF**
After the barcode image is saved to a MemoryStream, we are done with the barcode image. The only thing now needed is to add this barcode image (saved in the MemoryStream) to the PDF document. So, now it's time to create a PDF document using Aspose.PDF so that we can add this newly generated barcode image to it. Let's start by creating an instance of [Aspose.Pdf.Document](https://apireference.aspose.com/net/pdf/aspose.pdf/document) class and then add a page to this document instance as shown below:

{{< gist "aspose-com-gists" "f801733f5eb53b0777dd38da9db8366a" "Examples-CSharp-TechnicalArticles-AddBarcodeImageToPDFDocument-CreatePdfDocument.cs" >}}
## **Add Barcode Image to the PDF Document**
Aspose.Pdf provides a Document class that represents a PDF document. We can create an instance of the Document class by calling its empty constructor. After creating an empty document, we will add a page by calling Document.Pages.Add method. The Barcode image shall be generated in the Memorystream using BarcodeGenerator.Save method with Memorystream as a parameter and BMP as BarCodeImageFormat. The PdfFileMend class object shall be initiated provided by Aspose.PDF to add Barcode image to PDF as shown below.

{{< gist "aspose-com-gists" "f801733f5eb53b0777dd38da9db8366a" "Examples-CSharp-TechnicalArticles-AddBarcodeImageToPDFDocument-AddBarcodeImageToPDFDocument.cs" >}}
## **Conclusion**
Aspose.BarCode can easily be integrated with any of the Aspose Components to create rich applications for fulfilling the maximum requirements of the users. The most interesting thing is that any change in Aspose.BarCode version would not affect its integration with other Aspose Components because Aspose.PDF only deals with the barcode image produced by the Aspose.BarCode and not its internal structure.
