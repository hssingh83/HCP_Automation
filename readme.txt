mvn -PDebug test -Dbrowser=chrome -Durl=VoiceWatch-26.2

mvn -PSanity test -Dbrowser=chrome -Durl=VoiceWatch-26.2

mvn -PRegression test -Dbrowser=chrome -Durl=VoiceWatch-26.2


mvn -PRegression -Dsurefire.suiteXmlFiles=testng_Debug.xml test -Dbrowser=chrome -Durl=VoiceWatch-26.2

mvn -PRegression test -Dsurefire.suiteXmlFiles=testng_Debug.xml -Dbrowser=chrome -Durl=https://os-2k16-vm332.empirix.com




#To Run on eclipse

Comment

First#
String URL=System.getProperty("url");

if (URL.contains("VoiceWatch-26.0")) {	
	driver.get(prop.getProperty("url1"));
}	
	if (URL.contains("VoiceWatch-26.1")) {
		
		driver.get(prop.getProperty("url2"));
	
} if (URL.contains("VoiceWatch-26.2")) {
	
	driver.get(prop.getProperty("url3"));	
}

Second#
String browserName=System.getProperty("browser");
================================
Uncomment

First#

String browserName=prop.getProperty("browser");

Second#
//driver.get(prop.getProperty("url3"));

=====================================

H * * * * %browser=chrome; BRANCH=origin/develop1; Profile=Sanity; url=VoiceWatch-26.2;
H H/3 * * * %browser=chrome; BRANCH=origin/develop1; Profile=Debug; url=VoiceWatch-26.2;


