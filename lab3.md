**Lab Report 2**

**Part 1**
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String[] list = new String[100];
    int count = 0;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return newLine(this.list);
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    list[this.count] = parameters[1].replace("+", " ");
                    this.count++;
                    return newLine(this.list);
                }
            }
            return "404 Not Found!";
        }
    }
    public String newLine(String[] stringList){
        String newlist= "";
        for(int i = 0; i < stringList.length; i++){
            if(stringList[i] != null){
                newlist += "\n" + (i++) + ". " + stringList[i];
            } 
        }
        return newlist;
    }
}




class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
![screen1](/Screenshots/Lab3-1.PNG)
The methods that are called within my code are the handleRequests method and the newLine method within the Handler class. the argument for the handleRequest would be the user-inputted url, in this case https://0-0-0-0-4000-lp2fvifffngpik1ghadvi73v7k.us.edusercontent.com/add-message?s=Hello, and the newLine method took in the list that we constructed within the Handler class. The changes include that one of the new Strings from the list were ouputted onto the page, in this case going from nothing to having 1. Hello, as well as the index of the count incrementing from 0 to 1. 


![screen2](/Screenshots/Lab3-2.PNG)
Similar to the previous screenshot, the methods that are called within my code are the same as the previous: the handleRequests method and the newLine method within the Handler class. the argument for the handleRequest would be the user-inputted url, in this case https://0-0-0-0-4000-lp2fvifffngpik1ghadvi73v7k.us.edusercontent.com/add-message?s=How%20Are%20You, and the newLine method took in the list that we constructed within the Handler class. The changes include that one of the new Strings from the list were ouputted onto the page, in this case going from 1. Hello to 1.Hello and 2. How Are You, as well as the index of the count incrementing from 1 to 2. 

**Part 2**

Screenshots of ls to the paths to the private and public keys:
