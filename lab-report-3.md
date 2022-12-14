### Lab Report Week 3

#### Part 1

```
class Handler implements URLHandler {
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

![Image 1](add1.png)

In this example, I added the String "sunshine". The handleRequest method is called, and the condition of `if (url.getPath().contains("/add"))` is true, so the contents of the if statement are executed. A String Array is created, containing the values [s, sunshine]. The following if statement `if (param[0].equals("s"))` is therefore true, and so the contents are also executed. The Handler's ArrayList field `stringsList` adds the value of `param[0]`, which is "sunshine". The method returns "String added: sunshine", which is what is shown on the page.

![Image 2](add2.png)

Next, I added the string "sunglasses". Again, the handleRequest method is called, and the same if statements as before are evaluated to be true. The difference now is that `stringsList` now adds a new value "sunglasses", and the returning String reads "String added: sunglasses" which is shown on the page.

![Image 3](add3.png)

Next, I added the string "rain". The same if statements as the two prior examples are executed, and the Handler's `stringsList` field adds a third value of "rain". Similarly to before, the method returns "String added: rain" which is what is shown on the page.

![Image 4](search.png)

Lastly, this time I searched for the value "sun". The handleRquest method is called again, but this time the if statement `if (url.getPath().contains("/search"))` is what's evaluated to be true. The contents of this are executed, and a new String Array is created with the values [s, sun], along with a new empty ArrayList `quer`. The following if statement `if (param[0].equals("s"))` is true, and the contents are executed. The method loops through the ArrayList `stringsList` (as a reminder, this ArrayList contains the values [sunshine, sunglasses, rain]), and if the given value contains the search query "sun", it is added to the new ArrayList `quer`. This therefore filters only the values containing "sun". At the end of the loop, `quer` contains [sunshine, sunglasses]. The method then returns the String "Strings containing search: [sunshine, sunglasses]" which is what is now shown on the page.

#### Part 2

**ArrayExamples:**

Failure-inducing input:

![Image 5](arraytests.png)

Symptom:

![Image 6](testreversed.png)

Bug:

![Image 7](arrayexamples.png)

The method reversed creates a new array and assigns the values of the new array to the existing one, rather than doing the opposite, and returns that array instead of the new one. In order to fix this issue, the values should be assigned to the new array from the existing array, and the new array should be returned.

![Image 8](reversefixed.png)

Explanation:

The expected output of my failure-inducing input of [1,2,3,4] was [4,3,2,1]. The test found an error at index 0, it expected <4> but was <0>. Since the code assigns the values of the new array, which only contains empty values, the resulting array only contains empty values. 

**ListExamples:**

Failure-inducing input:

![Image 9](listtest.png)

Symptom:

![Image 10](listfailure.png)

Bug:

![Image 11](listfilter.png)

The method adds the checked strings to the beginning of the list, rather than the end. This reverses the order and is incorrect because the method should return the values in the original order. To fix this issue, the strings should be added to the end of the list, without including an index in the add function.

![Image 12](listfix.png)

Explanation:

The test expected [Short, Hi] but received [Hi, Short]. This is because the method adds the strings to the new list in the opposite order of how they should be within the list.
