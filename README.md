import java.util.*;

public class Main
{
    public static void main(String args[])
    {
        int noofbookings,availableTickets;
        int ticketid,price,nooftickets;
        Scanner scan=new Scanner(System.in);
        noofbookings=scan.nextInt();
        availableTickets=scan.nextInt();
        Ticket obj[]=new Ticket[noofbookings];
        for(int i=0;i<noofbookings;i++)
        {
            obj[i] = new Ticket();
        }
        obj[0].setavailableTickets(availableTickets);
        for(int i=0;i<noofbookings;i++)
        {
            ticketid=scan.nextInt();
            price=scan.nextInt();
            nooftickets=scan.nextInt();
            obj[i].setData(ticketid,price);
            availableTickets=obj[i].getavailableTickets();
            System.out.println("Available tickets: "+availableTickets);
            int totalamount=obj[i].getAmount(nooftickets);
            System.out.println("Total amount: "+totalamount);
            availableTickets=obj[i].getavailableTickets();
            System.out.println("Available tickets after booking: "+availableTickets);
        }
    }
}
