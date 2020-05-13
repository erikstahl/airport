Airport 
FlightStatus: String {
    case enRoute = "En Route"
    case scheduled = "Scheduled"
    case canceled = "Canceled"
    case delayed = "Delayed"
    case boarding = "Boarding"
}
struct Airport {
    let city: String
    let code: String
}
struct Flight {
    var flight: String
    var departureTime: Date?
    var terminal: String?
    var airline: String
    var status: FlightStatus
    var destination: String
}
class DepartureBoard {
    var departures: [Flight]
    var airport: Airport
    init(city: String, code: String) {
        departures = []
        airport = Airport(city: city, code: code)
    }
let jfk = Airport(city: "New York", code: "JFK")
let flight1 = Flight(flight: "AA 597", departureTime: Date(), terminal: "A5", airline: "Delta", status: .canceled, destination: "Mexico")
let flight2 = Flight(flight: "AB 987", departureTime: Date(), terminal: nil, airline: "American", status: .enRoute, destination: "Germany")
let flight3 = Flight(flight: "AD 920", departureTime: Date(), terminal: "C1", airline: "Frontier", status: .boarding, destination: "Oklahoma")
currentDepartureBoard.departures.append(flight1)
currentDepartureBoard.departures.append(flight2)
currentDepartureBoard.departures.append(flight3)
func printDepartures(departureBoard: DepartureBoard) {
    for currentDepartureBoard in departureBoard.departures {
        print(currentDepartureBoard)
    }
}
printDepartures(departureBoard: currentDepartureBoard)
Destination: Los Angeles Airline: Delta Air Lines Flight: KL 6966 Departure Time:  Terminal: 4 Status: Canceled
//:     Destination: Rochester Airline: Jet Blue Airways Flight: B6 586 Departure Time: 1:26 PM Terminal:  Status: Scheduled
//:     Destination: Boston Airline: KLM Flight: KL 6966 Departure Time: 1:26 PM Terminal: 4 Status: Scheduled
func printDepartures2(departureBoard: DepartureBoard) {
    let flights = [flight1, flight2, flight3]
    for flight in flights {
        print("Flight:\(flight1.flight)")
    }
}
printDepartures2(departureBoard: currentDepartureBoard)
//: ## 5. Add an instance method to your `DepatureBoard` class (above) that can send an alert message to all passengers about their upcoming flight. Loop through the flights and use a `switch` on the flight status variable.
//: a. If the flight is canceled print out: "We're sorry your flight to \(city) was canceled, here is a $500 voucher"
//:




func calculateAirfare(checkedBags: Int, distance:    Int, travelers: Int) -> Double
    let total + (Double)
