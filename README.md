using System;
using System.Collections.Generic;
using System.Linq;
using System.Web.Mvc;
using Airline.Models;

namespace Airline.Controllers
{
    public class AdminController : Controller
    {
        public static List<SearchRequest> routes = new List<SearchRequest>();
        public static List<Flight> flights = new List<Flight>();
        public static List<Passenger> passengers = new List<Passenger>();

        public ActionResult AdminPanel()
        {
            return View();
        }

        // ---------------- ROUTE METHODS ----------------

        public ActionResult AddRoute()
        {
            ViewBag.Routes = routes;
            return View();
        }

        [HttpPost]
        public ActionResult AddRoute(SearchRequest route)
        {
            route.RouteId = routes.Count + 1;
            routes.Add(route);
            return RedirectToAction("AddRoute");
        }

        public ActionResult EditRoute(int id)
        {
            var route = routes.FirstOrDefault(r => r.RouteId == id);
            if (route == null) return HttpNotFound();
            return View(route);
        }

        [HttpPost]
        public ActionResult EditRoute(SearchRequest updatedRoute)
        {
            var route = routes.FirstOrDefault(r => r.RouteId == updatedRoute.RouteId);
            if (route != null)
            {
                route.From = updatedRoute.From;
                route.To = updatedRoute.To;
                route.DepartureDate = updatedRoute.DepartureDate;
                route.RouteNumber = updatedRoute.RouteNumber;
            }
            return RedirectToAction("AddRoute");
        }

        public ActionResult DeleteRoute(int id)
        {
            var route = routes.FirstOrDefault(r => r.RouteId == id);
            if (route != null)
            {
                routes.Remove(route);
            }
            return RedirectToAction("AddRoute");
        }

        // ---------------- FLIGHT METHODS ----------------

        public ActionResult AddFlight()
        {
            ViewBag.Flights = flights;
            ViewBag.Routes = routes;
            return View();
        }

        [HttpPost]
        public ActionResult AddFlight(Flight flight)
        {
            flight.Id = flights.Count + 1;
            flights.Add(flight);
            return RedirectToAction("AddFlight");
        }

        public ActionResult EditFlight(int id)
        {
            var flight = flights.FirstOrDefault(f => f.Id == id);
            if (flight == null)
                return HttpNotFound();

            ViewBag.Routes = routes;
            return View(flight); // Pass flight model to the view
        }

        [HttpPost]
        public ActionResult EditFlight(Flight updatedFlight)
        {
            var flight = flights.FirstOrDefault(f => f.Id == updatedFlight.Id);
            if (flight == null)
                return HttpNotFound();

            // Update all fields
            flight.RouteId = updatedFlight.RouteId;
            flight.DepartureCity = updatedFlight.DepartureCity;
            flight.ArrivalCity = updatedFlight.ArrivalCity;
            flight.DepartureTime = updatedFlight.DepartureTime;
            flight.ArrivalTime = updatedFlight.ArrivalTime;
            flight.EconomyPrice = updatedFlight.EconomyPrice;
            flight.EconomySeats = updatedFlight.EconomySeats;
            flight.BusinessPrice = updatedFlight.BusinessPrice;
            flight.BusinessSeats = updatedFlight.BusinessSeats;
            flight.FirstClassPrice = updatedFlight.FirstClassPrice;
            flight.FirstClassSeats = updatedFlight.FirstClassSeats;
            flight.AirplaneId = updatedFlight.AirplaneId;
            flight.AirplaneNumber = updatedFlight.AirplaneNumber;

            return RedirectToAction("AddFlight");
        }

        public ActionResult DeleteFlight(int id)
        {
            var flight = flights.FirstOrDefault(f => f.Id == id);
            if (flight != null)
            {
                flights.Remove(flight);
            }
            return RedirectToAction("AddFlight");
        }
        public ActionResult PassengerInfo()
        {
            return View("PassengerInfo", passengers);
        }
    }
}
_--------+--------

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

namespace Airline.Models
{
    public class Passenger
    {
        public int Id { get; set; }

        // Flight Information
        public string SeatNumber { get; set; }
        public string Class { get; set; }
        public decimal Price { get; set; }
        public string AirplaneNumber { get; set; }
        public string DepartureCity { get; set; }
        public string ArrivalCity { get; set; }
        public DateTime DepartureDate { get; set; }
        public TimeSpan DepartureTime { get; set; }
        public TimeSpan ArrivalTime { get; set; }

        // Passenger Personal Info
        public string Title { get; set; }
        public string FirstName { get; set; }
        public string LastName { get; set; }
        public string Gender { get; set; }
        public string MobileNumber { get; set; }
        public int Age { get; set; }

        // Booking Meta
        public DateTime BookingDate { get; set; } = DateTime.Now;
    }

}
-----------------
-----------------
Flight. cshtml
