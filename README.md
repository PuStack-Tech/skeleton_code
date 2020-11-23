# skeleton_project  
  
A skeleton flutter project to show the  code structure
  
## Code Structure
### models
Files under this are grouped by tab (Doubt Forum, News Feed, Live Session, etc) 

### screens
Files under this are grouped by tab (Doubt Forum, News Feed, Live Session, etc) and main functionality. For example, the screen to show a list of all doubts and the screen to show a doubt's detailed view will be grouped under 'screens/doubt_forum' and will be placed under 'screens/doubt_forum/doubt_list/doubt_list_screen.dart' and 'screens/doubt_forum/doubt_detail/doubt_detail_screen' respectively. It might require multiple screens to achieve one main functionality. For example, to add a doubt to firebase, user need to go through two steps: 1) select category 2) add doubt detail, so there will be two screens grouped under 'screens/doubt_forum/add_doubt', and will be named 'screens/doubt_forum/add_doubt/add_doubt_category_screen.dart' and 'screens/doubt_forum/add_doubt/add_doubt_detail_screen.dart';
In addition to screens grouped by tabs, there are some helper screens that may be used throughout the entire app. For example, image gallery view is used by both doubt forum and news feed. It will be placed under 'screens/image_gallery/image_gallery_screen.dart' 
### services
Files under this directory do not need to be grouped. 

### states
Files under this directory do not need to be grouped. 

### utils
Files under this directory do not need to be grouped. 

### widgets
Files under this are grouped by tab (Doubt Forum, News Feed, Live Session, etc). The difference between widgets under this directory and widgets under each specific screen is that the widget under this directory is shared through the entire tab. For example, doubt comment widget is used by multiple screens under doubt forum (doubt list screen, doubt detail screen, etc) so the doubt comment widget will be put under 'widgets/doubt_comments.dart' instead of 'screens/doubt_forum/doubt_list_screen/widgets/doubt_comments.dart'. 

## Naming Convention
### models
Files under this folder ends with _model.dart

### screens
Files under this folder ends with _screen.dart. 

### services
Files under this folder ends with _service.dart and contains backend CRUD code. For instance, filtered_doubt_service.dart handles the firebase handling related to doubt forum, like fetching initial doubt posts, fetching more doubt posts, commenting a doubt, etc. 

### states
Files under this folder ends with _data.dart, and contains state management related code. Each major component should have its corresponding state management. For instance, filtered_doubt_data.dart will handle the state management code for doubt forum; news_feed_data.dart will handle the state management code for doubt forum. 

### utils 
Files under this folder usually end with _helper.dart, and contain some helper functions grouped by purpose. For instance, functions that handle string manipulation, will be grouped under string_helper.dart.  