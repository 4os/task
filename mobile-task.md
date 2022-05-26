<h1 align=center>Tuğberk Can Özen  Appcent Case</h1> 

I model the data I got from a game site and transferred it to the application with Alamofire. I created a detail page for the games and showed the pictures by downloading them with Kingfisher. I made the auto layout of the application programmatically with Snapkit. I hope you like.

## Technologies
+ MVVM Architecture ✅ 
+ Programmatically (Snapkit) ✅ 
+ Kingfisher ✅ 
+ Alamofire ✅
+ Scroll View ✅ 
+ Collection View ✅
+ User Defaults ✅
+ Splash Screen ✅

## Demo

Video alanı

## API

Ex: https://rawg.io/apidocs 

```swift
{
class NetworkConstant{
        enum GameServiceEndPoint: String {
            case BASE_URL = "https://api.rawg.io/api/games"
            case API_KEY = "73a717c6a42b406087a4bbd1600f3702"
            
            static func fetchGame() -> String {
                "\(BASE_URL.rawValue)?key=\(API_KEY.rawValue)"
            }
            
            static func detailGame(gameId: Int) -> String {
                "\(BASE_URL.rawValue)/\(gameId)?key=\(API_KEY.rawValue)"
            }
        }
    }
}
```
