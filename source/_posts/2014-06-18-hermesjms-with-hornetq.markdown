---
layout: post
title: "hermesJMS with hornetQ"
date: 2014-06-18 17:10:09 +0800
comments: true
categories: 
---

*The prerequisite of this post is that the hornetQ server is already configured to work with Jboss server (i.e. Jboss 7)*

**The environment with below tools:**

   * HermesJMS v1.14
   * HornetQ Server version 2.2.21.Final
   * Jboss 7
   
**1) Get [HermesJMS](http://www.hermesjms.com "hermesjms") and install HermesJMS v1.14**

**2) New a JMS session through 'Actions' menu**

**3) Switch to 'Providers' tab and configure classpathgroup, name it 'hornetq'** *(add the jboss-client.jar, you can get this jar file from Jboss7 distribution)*

  ![hornetq](/images/hermesjms/02.jpg)

**4) Configure ConnectionFactory as below**

  * Class  : select 'hermes.JNDIConnectionFactory'  
  * Loader : select 'hornetq' 

  ![ConnectionFactory](/images/hermesjms/01.jpg)

**5) Add Topic or Queue to the JMS session** *(below with a topic=/topic/commonEntity/v1)*

  ![ConnectionFactory](/images/hermesjms/03.jpg)

**6) Click the Topic or Queue to watch the incoming JMS messages**

  ![ConnectionFactory](/images/hermesjms/05.jpg)



*Reference:*

1. [HermesJMSWithHornetQ on Jboss](https://community.jboss.org/wiki/UsingHermesJMSWithHornetQ "UsingHermesJMSWithHornetQ")

2. [HermesJMS and ActiveMQ integration with SoapUI](http://xebee.xebia.in/index.php/2014/03/16/soap-over-jms-with/)

----------

