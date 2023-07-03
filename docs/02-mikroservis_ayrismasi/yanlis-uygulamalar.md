---
layout: default
title:  Antipatterns
parent: Mikroservis Ayrışması
nav_order: 10
---

# Dönüşümle ilgili Yanlış Uygulamalar

## Veri odaklı dönüşüm
 * data is a corporate asset, not an application asset
 * migrate the functional portion of the service first
 * let the data portion of the bounded context of a service evolve over time

### functionality first, data last
* pros
  * karmaşık veri dönüşümleri tekrar tekrar yapılmaz
  * gerektiği zaman servis detaylandırması açılabilir. 
  * kod migrationı göreceli daha kolaydır
* cons
  * tam oturana kadar zayıf bir bounded context olur.    

## İş değil Teknoloji odaklı dönüş
* too much focus on technology and infrastructure (staging iterations) and not on business functionality
* for individuals or teams working with microservices to fall into the trap of treating each service as its own "stage," with each service's performance and metrics taking precedence over the overall goals and needs of the system as a whole.
  For example, if each microservice team is only concerned with optimizing their own service's performance without considering the impact on the other services and the system as a whole, this can lead to inefficiencies, dependencies, and communication breakdowns.
To avoid this anti-pattern, it is important to maintain a holistic perspective and prioritize collaboration, communication, and shared goals across all teams working with microservices. This includes ensuring that each service is designed with the overall system architecture in mind, and that communication and coordination between teams are emphasized and supported.

# Veri birleştirmeyle ilgili Yanlış Uygulamalar

