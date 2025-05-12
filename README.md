import React from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { CalendarIcon, TicketIcon, LocateIcon, PlusCircle, ClipboardList, BarChart } from "lucide-react";

export default function HomePage() { return ( <div className="min-h-screen bg-gradient-to-br from-amber-100 to-white text-gray-800 font-sans"> <header className="p-6 shadow-md bg-white flex justify-between items-center"> <h1 className="text-3xl font-bold text-amber-800">Sheher-e-Khaas</h1> <Button className="bg-amber-700 text-white rounded-full">Login / Signup</Button> </header>

<section className="text-center py-12 px-4">
    <h2 className="text-4xl font-semibold text-amber-900 mb-4">
      Janiye, Jiyiye, aur Jashn manaiye – Apne Sheher ke Saath
    </h2>
    <p className="text-lg text-gray-600 mb-6">
      Explore upcoming events, shows, sports, movies, and more in Lucknow.
    </p>
    <Button className="bg-amber-600 text-white px-6 py-2 rounded-xl text-lg">
      Browse Events
    </Button>
  </section>

  <section className="grid grid-cols-1 md:grid-cols-3 gap-6 px-6 py-10">
    <Card className="rounded-2xl shadow-lg">
      <CardContent className="p-6 text-center">
        <CalendarIcon className="mx-auto mb-4 h-10 w-10 text-amber-700" />
        <h3 className="text-xl font-semibold mb-2">Today's Picks</h3>
        <p className="text-gray-600">Handpicked events just for you.</p>
      </CardContent>
    </Card>

    <Card className="rounded-2xl shadow-lg">
      <CardContent className="p-6 text-center">
        <TicketIcon className="mx-auto mb-4 h-10 w-10 text-amber-700" />
        <h3 className="text-xl font-semibold mb-2">Book at MRP</h3>
        <p className="text-gray-600">No extra fees – just original ticket prices.</p>
      </CardContent>
    </Card>

    <Card className="rounded-2xl shadow-lg">
      <CardContent className="p-6 text-center">
        <LocateIcon className="mx-auto mb-4 h-10 w-10 text-amber-700" />
        <h3 className="text-xl font-semibold mb-2">Events Near You</h3>
        <p className="text-gray-600">Find what's happening in your locality.</p>
      </CardContent>
    </Card>
  </section>

  {/* Event Listing Section */}
  <section className="px-6 py-10 bg-white">
    <h3 className="text-2xl font-bold text-amber-800 mb-4">Upcoming Events</h3>
    <div className="grid gap-4 md:grid-cols-3">
      {[1, 2, 3].map((event) => (
        <Card key={event} className="rounded-xl shadow-md">
          <CardContent className="p-4">
            <h4 className="text-xl font-semibold mb-1">Event Title {event}</h4>
            <p className="text-sm text-gray-600 mb-2">Date & Time • Venue</p>
            <p className="text-sm text-gray-700 mb-4">Short description of the event with key details.</p>
            <Button className="bg-amber-700 text-white w-full">Book Ticket</Button>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  {/* Event Submission Section */}
  <section className="px-6 py-10 bg-amber-50">
    <h3 className="text-2xl font-bold text-amber-800 mb-4">List Your Event</h3>
    <div className="grid md:grid-cols-2 gap-4">
      <Card className="rounded-xl shadow-sm">
        <CardContent className="p-4">
          <PlusCircle className="h-6 w-6 text-amber-700 mb-2" />
          <h4 className="text-lg font-semibold mb-2">Promote Your Event</h4>
          <p className="text-sm text-gray-600">Submit your event details, date, location, and ticket info to reach the local audience.</p>
          <Button className="mt-4 bg-amber-700 text-white">Add Event</Button>
        </CardContent>
      </Card>
    </div>
  </section>

  {/* Orders Section */}
  <section className="px-6 py-10">
    <h3 className="text-2xl font-bold text-amber-800 mb-4">My Bookings</h3>
    <div className="grid gap-4">
      <Card className="rounded-lg shadow">
        <CardContent className="p-4">
          <ClipboardList className="h-5 w-5 inline-block mr-2 text-amber-700" />
          <span className="font-medium">You have 2 upcoming bookings.</span>
          <p className="text-sm text-gray-600 mt-1">See full list in your dashboard.</p>
        </CardContent>
      </Card>
    </div>
  </section>

  {/* Sales Section */}
  <section className="px-6 py-10 bg-amber-100">
    <h3 className="text-2xl font-bold text-amber-800 mb-4">Event Sales Report</h3>
    <div className="grid gap-4">
      <Card className="rounded-lg shadow">
        <CardContent className="p-4">
          <BarChart className="h-5 w-5 inline-block mr-2 text-amber-700" />
          <span className="font-medium">Track ticket sales for your listed events.</span>
          <p className="text-sm text-gray-600 mt-1">View breakdown by event and date.</p>
        </CardContent>
      </Card>
    </div>
  </section>

  {/* Footer */}
  <footer className="bg-amber-50 py-6 text-center text-sm text-gray-500">
    &copy; 2025 Sheher-e-Khaas. Made with love in Lucknow.<br />
    Customer Care: <a href="tel:9919900291" className="text-amber-700 font-medium">9919900291</a>
  </footer>
</div>

); }

