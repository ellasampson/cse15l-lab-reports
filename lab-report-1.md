## Week 1 Lab Report
---

## Remote Access Tutorial

### Step 1: Install Visual Studio Code

- Download vscode and follow the setup instructions
- When you’re done, the window should look like this:

![Image 1](vscodestartermenu.png)

### Step 2: Remotely Connect

- If you're on a Windows computer, check if you already have the OpenSSH client installed. If not, install it [here](https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse?tabs=gui).
- Open a new terminal in VSCode
- Input the command `ssh cs15lfa22!!@ieng6.ucsd.edu` with the last 2 digits of *your* username in place of `!!`
- Type `yes` when prompted and enter, then enter your password
> I had an issue at first! Make sure to reset your password before entering it for the first time. Some of my lab partners also encountered issues with their passwords, so if resetting it doesnt work, try entering your AD password.
- You should now see something similar to this in your console:

![Image 2](sshlogin.png)

- You should now be connected to the remote server!

### Step 3: Test Commands

- Here are some examples of commands you can try out:
  - `cd`
  - `ls -lat`
  - `ls -a` 
  > The `ls` commands will list the files in the given directory.
  - `cp /home/linux/ieng6/cs15lfa22/public/hello.txt ~/`
  - `cat /home/linux/ieng6/cs15lfa22/public/hello.txt`
- Before moving onto the next step where we will test out copying files remotely using `scp`, we need to exit the remote server. You can use either Ctrl + D or enter the command `exit`.

### Step 4: Copying Files Remotely

- Create an example file to copy. This file is going to give us information about the system we are working with.
- Copy
  ```
  class WhereAmI {
    public static void main(String[] args) {
      System.out.println(System.getProperty("os.name"));
      System.out.println(System.getProperty("user.name"));
      System.out.println(System.getProperty("user.home"));
      System.out.println(System.getProperty("user.dir"));
    }
  }
  ```
  into a file called `WhereAmI.java` and save it onto your computer.
- Compile and run the program:
  `javac WhereAmI.java`
  `java WhereAmI`
- INSERT PICTURE
- Now in the same terminal, run the command `scp WhereAmI.java cs15lfa22!!@ieng6.ucsd.edu:~/` and enter your password again.
- Input the command `cs15lfa22!!@ieng6.ucsd.edu` and run the program again:
  `javac WhereAmI.java`
  `java WhereAmI`
- INSERT PICTURE
- See how the output is different? The values reflect the new remote server!


