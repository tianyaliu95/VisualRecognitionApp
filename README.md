# VisualRecognitionApp  
<strong>VizAssistant</strong> - An accessible Android app that assists the visually impaired in completing daily reading tasks independently by converting images to voice messages using optical character recognition (OCR) and Android TalkBack.
<hr />
<b>Project Demo:</b> <a href="https://youtu.be/BZoTnwjp4tQ">Click here for the full version with TalkBack sound!</a>
<br />
<b>Project Demo GIF (without TalkBack sound):</b>
<img src="https://github.com/tianyaliu95/VisualRecognitionApp/blob/master/DemoGIF.gif" alt="">
<div>Note: the app is running with Android Accessibility Mode turned on <a href="https://support.google.com/accessibility/android/answer/6006564?hl=en">(What is Android Accessibility Mode?)</a></div>


## <b>Client Side: </b>
<ul>
	<li>User Interface:
		<ul>
			<li>First Page: camera/albums buttons on the top-right & result placeholder at the bottom</li>
			<li>Result Page: image captured/selected in the middle & text result/error meesage at the bottom</li>
		</ul>
	</li>
	<li>Client <-> Server
		<ul>
			<li>Image data accessing and packaging</li>
			<li>OCR server query with image data</li>
			<li>UI update after parsing response from server</li>
		</ul>
	</li>
</ul>

## <b>Server Side: </b>
<ul>
	<li>Integrated Google Cloud Vision API with Java servlet built in HTTP server (Apache Tomcat)</li>
	<li>Deployed to Google Compute Engine (GCE) by building a Docker container with a Docker image and running the service on GCE Virtual Machine</li>
	<li>Improvement: pushed Docker image to Docker Hub and deployed to GKE cluster for higher scalability</li>
</ul>
<div><b>Web Service Overview</b></div>
<img src="https://github.com/tianyaliu95/VisualRecognitionApp/blob/master/Server/Web%20Service%20Overview.JPG" alt="web service overview">