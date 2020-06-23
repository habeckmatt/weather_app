# Weather Finder
This app allows a user to input a city and a country to receive information about the local weather.
The data the user receives includes:  
&nbsp;&nbsp;-Temperature  
&nbsp;&nbsp;-Humidity  
&nbsp;&nbsp;-Description of the current conditions

# Motivation
My initial goal was to create an app built with React. I then wanted to try and utilize an
API to retrieve information based upon the weather. The lacking pieces of this project are it's responsiveness
due to my focus on the React piece of the project.

# Screenshots
![Weather App Homepage](weather_api_thumbnail.jpg)

# Tech/framework used
**Built with**  
&nbsp;&nbsp;[-React](https://github.com/facebook/react)

# Features
The main feature of this app is the ability of a user to search for weather for a particular city.
It retrieves this data from an API and displays it in the UI.

# Code Example

    const Weather = (props) => {
    return (
        <div className="weather__info">
            { 
            props.city && props.country &&  <p className="weather__key">Location:
                <span className="weather__value"> { props.city }, { props.country }</span></p>
            }       
            { 
            props.temperature && <p className="weather__key">Temperature:
                <span className="weather__value"> { props.temperature }</span></p>
            }         
            { 
            props.humidity && <p className="weather__key">Humidity:
                <span className="weather__value"> { props.humidity }</span></p> 
            }
            { 
            props.description && <p className="weather__key">Conditions:
                <span className="weather__value"> { props.description }</span></p> 
            }
            { 
            props.error && <p className="weather__error">{ props.error }</p>
            }
        </div>  
    );
    }

    export default Weather;

# Installation
npm install weather

# License
MIT © Matt Habeck
