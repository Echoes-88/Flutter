## CREATE ARRAY OF OBJECTS AND ITERATE

JS :
```TS
type Offer = {
  title: string;
  subtitle: string;
  icon: string;
  type: string;
}

const offerTypes: Offer[] = [
  {
    'title': "Des colis",
    "subtitle": "Indiquez ce que vous souhaitez vendre et jusqu'à quand",
    "icon": "Icons.dashboard",
    "type": "colis"
  },
  {
    'title': "Des palettes",
    "subtitle": "Indiquez ce que vous souhaitez vendre et jusqu'à quand",
    "icon": "Icons.dashboard",
    "type": "palettes"
  }
];
  
offertTypes.map(offer=> ....)
```
  
DART :
```DART
class Offer {
    String title;
    String subtitle;
    String icon;
    String type;

  Offer({required this.title, required this.subtitle, required this.icon, required this.type});
}
  
List<Offer> offerTypes = [
  Offer(title: "Des colis", subtitle: "Indiquez ce que vous souhaitez vendre et jusqu'à quand", icon: "Icons.dashboard", type: "colis"),
  Offer(title: "Des palettes", subtitle: "Indiquez ce que vous souhaitez vendre et jusqu'à quand", icon: "Icons.dashboard", type: "palettes"),
];
  
...
children: <Widget>[...offerTypes.map((offer)=> 
    CardWithIcon(
    title: offer.title,
    subTitle: "Vous proposez quelques colis",
    icon: Icons.dashboard,
    onPressed: () {
      ctrl.conditioningType.value = "colis";
    },
    selected: ctrl.conditioningType.value == "colis"),
).toList()
  ```

