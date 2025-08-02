# cs370-final-project

Featured Project: Remmy,  Intelligent Recipe Manager and Pantry Tracker

Check out Remmy, a personal recipe assistant that helps users create nutritious meals based on what's already in their pantry. Currently I am working on adding ML features for even more efficient recipe generation that fits the users needs more.


Tools: Java, PostgreSQL, Java Swing, Nutrition APIs

What I Did:

Built a desktop app that generates custom recipes using pantry inventory, tracks food expiration, and shows detailed macronutrient info.
Designed and implemented a user login system and persistent data storage using PostgreSQL.
Integrated a nutrition API to fetch real-time nutrient profiles for recipe ingredients.
Developed intuitive UI with Java Swing to display recipe cards, shuffle meal ideas, and manage pantry items.

### Setup Instructions

Install the following: 
- Java JDK 17+
- Download JDK
- PostgreSQL (14 or later)
- A Java IDE e.g. IntelliJ IDEA, Eclipse, or VS Code with Java support
1: Clone the Repository
git clone https://github.com/arpitag2004/cs370-final-project.git
cd cs370-final-project
2: Set Up PostgreSQL Database
Launch psql or pgAdmin
Create a new database:
CREATE DATABASE remmy;
psql -U your_username -d remmy -f schema.sql
Make sure your database config in the code (DBConnection.java) matches:
String url = "jdbc:postgresql://localhost:5432/remmy";
String user = "your_username"; // what you pick !
String password = "your_password";
3: Add Nutrition API Key
If your app fetches nutritional data:
Sign up for an API key (e.g. Edamam or Spoonacular)
Place the API key in a config file
4: Compile and Run the App
If using terminal:
javac -cp .:postgresql-42.2.18.jar *.java
java -cp .:postgresql-42.2.18.jar Main

🧪 Optional: Populate Sample Pantry Data
Use sample_data.sql or enter a few test items through the UI to test the recipe generation feature.
