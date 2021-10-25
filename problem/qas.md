## Quality Attributes Scenarios

Lets start by mapping architecture characteristics (we also referred them as architecture illities or non functional requirements) and see what type of characteristics we could extract out from the core system requirements.

![Farmacy Family Archutecture Illities](../images/arch-nfr.png)

## *Security*
- User personal data must be protected via encryption in all communication channels. 
- User personal data must be protected via encryption or access control wherever it is stored or manipulated. 
- User medical data needs to be HIPA Complaint.
- User medical data needs to be secured to avoid any potential hacker attacks.

## *Availability*
- The system must be highkly available to fullfill on going customer needsd and available to integrate with other 3rd party systems like Clinic/eDietian as well as farmacy Foods.

## *Scalability*
- The system must quickly and automatically cater to an increasing number of users.
- As users can join from different geographical locations so at any difficult to pin point from where the next batch of load gets trigerred. 

## *Elasticity*
- Scalability is required for elasticity, but not the other way around.
- The system must quickly and automatically cater to a bust in the incoming requests.
- There are Onine wellness classes happening or some forums are really axgive at particular time of the day so better to add (scale up/out) more resources.

## *Extensibility*
- The level of extensibility reflects how easy it is to extend or enhance the software system. Software systems that are designed to be extensible take future growth into consideration by anticipating the need to add new functionality.
- It also enable our platform to quickly do experiments.
- There are different integration points to this system so it should be easily extendiable for any such future needs (new integration point, new engagement model etc.)

## *Performance - response time* 
- Customer engaged in different forums or live ongoing welness education classes are few examples where quick response time is very critical.

## *Performance - throughput* 
- During peak hours, the system must be able to support a high number of concurrent user sessions (e.g., 100 simultaneous users). 

## *App usability* 
- The different versions of the app should provide a user experience that appeals to the target user population. 
- Using UX design techniques, and providing high levels of customization are goals.
- AT the end of the day, it should be a seamless experience for Farmacy Foods and Family customers.
