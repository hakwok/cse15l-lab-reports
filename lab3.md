```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String[] list = new String[100];
    int count = 0;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return makeList(this.list);
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    list[this.count] = parameters[1].replace("+", " ");
                    this.count++;
                    return makeList(this.list);
                }
            }
            return "404 Not Found!";
        }
    }
    public String makeList(String[] stringList){
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
