### Lab Report Week 3

#### Part 1

```
class Handler implements URLHandler {
    String[] l = new String[500];
    ArrayList<String> stringsList = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Strings: " + stringsList.toString());
        }

        else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] param = url.getQuery().split("=");
                if (param[0].equals("s")) {
                    stringsList.add(param[1]);
                    return String.format("String added: \"" + param[1] + "\"");
                }
            }

            else if (url.getPath().contains("/search")) {
                String[] param = url.getQuery().split("=");
                ArrayList<String> quer = new ArrayList<>();
                if (param[0].equals("s")) {
                    for (int i = 0; i < stringsList.size(); i++) {
                        if (stringsList.get(i).contains(param[1])) {
                            quer.add(stringsList.get(i));
                        }
                    }
                    return String.format("Strings containing search: " + quer.toString());
                }
            }

            return "404 Not Found!";
        }
    }
}

class SearchEngine {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151") ;
            return;
        }

        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

