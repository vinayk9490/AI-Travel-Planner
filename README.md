# AI Travel Planner 🤖✈️

This project uses a multi-agent system built with Microsoft's **AutoGen** framework to create comprehensive and personalized travel itineraries. By leveraging the power of multiple specialized AI agents, this tool can handle complex travel planning requests, from checking the weather to creating a day-by-day schedule and estimating the total cost.

## ✨ Features

-   **🌦️ Weather Information**: Get real-time weather conditions for your destination and receive clothing recommendations.
-   **🏰 Tourist Attractions**: Discover the top tourist spots and must-see attractions.
-   **🏨 Hotel Recommendations**: Find the best budget-friendly hotels with good ratings.
-   **📅 Day-wise Itinerary**: Receive a detailed, personalized 5-day itinerary.
-   **💰 Cost Estimation**: Get a breakdown and total estimated cost for your trip.
-   **🗣️ Multi-Agent Collaboration**: A planner agent delegates tasks to a team of specialized agents, each an expert in its domain.

## 🛠️ How It Works

The system is orchestrated by a `Travel_Planner` agent that acts as a project manager. When a user provides a travel request, the planner breaks it down into smaller subtasks and assigns them to the appropriate specialist agent:

1.  **Weather_Information Agent**: Fetches weather data.
2.  **Tourism_Information Agent**: Finds attractions.
3.  **Hotel_Information Agent**: Recommends hotels.
4.  **Daywise_Itinerary_Planner Agent**: Creates the schedule.
5.  **Total_Cost Agent**: Calculates the budget.
6.  **Trip_Summary Agent**: Compiles all the information into a final summary.

These agents work together within a group chat, sharing information to build a complete travel plan that meets the user's requirements.

## 🚀 Technologies Used

-   **Framework**: `autogen`
-   **LLM Integration**: `langchain`, `openai`
-   **APIs**:
    -   OpenWeatherMap API for weather data.
    -   Google Serper API for web search (attractions, hotels, etc.).
    -   OpenAI API (GPT-4o) for language understanding and generation.

## ⚙️ Setup and Usage

### 1. Prerequisites
- Python 3.8+
- An OpenAI API Key
- A Google Serper API Key
- An OpenWeatherMap API Key

### 2. Clone the Repository
```bash
git clone [https://github.com/vinayk9490/AI-Travel-Planner.git](https://github.com/vinayk9490/AI-Travel-Planner.git)
cd AI-Travel-Planner

3. Install Dependencies
It's recommended to use a virtual environment.

python -m venv env
source env/bin/activate  # On Windows, use `env\Scripts\activate`

Install the required packages from the notebook or a requirements.txt file.

pip install autogen langchain openai python-dotenv pyowm google-search-results

4. Configure API Keys
Create a .env file in the root directory of the project and add your API keys:

OPENAI_API_KEY="your_openai_api_key"
SERPER_API_KEY="your_google_serper_api_key"
OPENWEATHERMAP_API_KEY="your_openweathermap_api_key"
