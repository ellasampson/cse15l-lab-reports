## Week 5 Lab Report

### `grep -r`
(`grep -r <<string>> <<directory>>`)

The `-r` command allows grep to search recursively through a directory, rather than just one or multiple files.

##### Example 1: `grep -r "health-care professional" technical`

```
technical/government/Media/A_helping_hand.txt:affects children. Mintie noticed that health-care professionals
technical/plos/pmed.0020246.txt:        Discriminatory or unethical behavior by health-care professionals against PLWA, as
technical/plos/pmed.0020246.txt:        Anecdotal information suggests that health-care professionals in Nigeria may engage in
technical/plos/pmed.0020246.txt:          representative sample of health-care professionals, we proportionally sampled doctors,
technical/plos/pmed.0020246.txt:          percent of the health-care professionals were sampled from tertiary care facilities. We
technical/plos/pmed.0020246.txt:          301 health-care professionals. However, our sample design included several levels of
technical/plos/pmed.0020246.txt:          the number of health-care professionals were derived from Federal Ministry of Health
technical/plos/pmed.0020246.txt:          The 104-item health-care professional survey included questions on respondent
technical/plos/pmed.0020246.txt:          health-care professional practices and attitudes towards people with HIV/AIDS, rather
technical/plos/pmed.0020246.txt:            Seventeen percent of surveyed health-care professionals reported that their facility
technical/plos/pmed.0020246.txt:            Ninety-one percent of professionals agreed that staff and health-care professionals
technical/plos/pmed.0020246.txt:            Forty percent believed that health-care professionals with HIV/AIDS should not be
technical/plos/pmed.0020246.txt:            Among health-care professionals, the three most important concerns about treating
technical/plos/pmed.0020246.txt:            (Table 6). Sixty-six percent had observed other health-care professionals refusing to
technical/plos/pmed.0020246.txt:            To prevent discrimination by health-care professionals against patients with
technical/plos/pmed.0020246.txt:            HIV/AIDS, most participants (87%) indicated that health-care professionals who engage
technical/plos/pmed.0020246.txt:            health-care professionals reported that it is possible to determine a person's HIV
technical/plos/pmed.0020246.txt:        Most health-care professionals in the four states where the study was conducted appeared
technical/plos/pmed.0020246.txt:        behavior by health-care professionals against people with HIV/AIDS in Nigeria.
technical/plos/pmed.0020246.txt:          possible that sampled facilities and health-care professionals may differ significantly
technical/plos/pmed.0020246.txt:          overreporting of discriminatory behavior or may result from health-care professionals
technical/plos/pmed.0020246.txt:          While this study focused on HIV/AIDS, it is possible that health-care professionals
technical/plos/pmed.0020246.txt:          patients. Even if health-care professionals engage in breaches of confidentiality and
technical/plos/pmed.0020257.txt:        health-care professionals in 111 health-care facilities in four of Nigeria's 36 states.
technical/plos/pmed.0020257.txt:        The researchers concluded that, while most health-care professionals surveyed reported
technical/plos/pmed.0020257.txt:        sampled facilities and health-care professionals may differ significantly from those that
```
`grep -r "health-care professional" technical` searches for the string "health-care professional" recursively through the technical directory.
The use of `-r` is helpful in this case because it allowed me to search for lines containing the string "health-care professional" in the entire
technical directory, ratherthan having to specify specific files.

##### Example 2: `grep -r "intergovernmental" technical`

```
technical/government/Gen_Account_Office/og96022.txt:contain a significant intergovernmental mandate. Accordingly,
technical/government/Gen_Account_Office/og96022.txt:Orders on property rights (12630), intergovernmental partnership
technical/government/Gen_Account_Office/og96023.txt:(intergovernmental partnership), 12988 (civil justice reform) and
technical/government/Gen_Account_Office/og96026.txt:Consistent with the intergovernmental provisions of sections 203
technical/government/Gen_Account_Office/og96033.txt:significant intergovernmental mandate. Consequently the rule does
technical/government/Gen_Account_Office/og96041.txt:Since the rule does not impose a federal intergovernmental or
technical/government/Gen_Account_Office/og96042.txt:will not impose an intergovernmental mandate because there are no
technical/government/Gen_Account_Office/og96045.txt:will not impose an intergovernmental mandate because there are no
technical/government/Gen_Account_Office/og96047.txt:contain a significant intergovernmental mandate. Accordingly,
technical/government/Gen_Account_Office/og97041.txt:intergovernmental mandate included in the rule. EPA claims that
technical/government/Gen_Account_Office/og97041.txt:intergovernmental mandate. In any event, EPA claims to have
technical/government/Gen_Account_Office/og97045.txt:qualify as either a federal intergovernmental mandate or a federal
technical/government/Gen_Account_Office/og98024.txt:million. There is no intergovernmental mandate because the OSHA
technical/government/Gen_Account_Office/og98030.txt:intergovernmental or private sector mandate of $100 million or
technical/government/Gen_Account_Office/og98041.txt:intergovernmental or private sector mandate of $100 million or
technical/government/Gen_Account_Office/og98044.txt:intergovernmental or private sector mandate of $100 million or
technical/government/Gen_Account_Office/og98046.txt:intergovernmental mandate of $100 million or more in any one year
```
`grep -r "health-care professional" technical` searches for the string "intergovernmental" recursively through the technical directory.
The use of `-r` is helpful in this case because it allowed me to search for lines containing the string "intergovernmental" in the entire technical directory, rather
than having to specify specific files.

##### Example 3: `grep -r "subcommittees" technical`
```
technical/911report/chapter-13.1.txt:                committees. Those committees have no subcommittees just for intelligence, and only a
technical/911report/chapter-13.1.txt:                and subcommittees of Congress. One expert witness (not a member of the
technical/911report/chapter-13.3.txt:                of the hearing records of the subcommittees on immigration of the House and Senate      
technical/government/About_LSC/State_Planning_Report.txt:The Steering Committee, working through subcommittees, produced
technical/government/About_LSC/State_Planning_Report.txt:The Task Force worked through subcommittees organized around the
technical/government/About_LSC/State_Planning_Report.txt:subcommittees reported to the full committee. A final Task Force
technical/government/Gen_Account_Office/d03232sp.txt:House and relevant committees or subcommittees in connection
technical/government/Gen_Account_Office/d03232sp.txt:House, including the applicable committees' or subcommittees'
technical/government/Gen_Account_Office/Testimony_cg00010t.txt:times before 93 congressional committees or subcommittees as shown
technical/government/Gen_Account_Office/Testimony_d01609t.txt:committees and subcommittees. Our experts testified on a broad
technical/government/Gen_Account_Office/Testimony_d01609t.txt:committees and subcommittees, thus severely limiting-and
technical/government/Gen_Account_Office/Testimony_Jul17-2002_d02957t.txt:issues raised by House committees and subcommittees.
technical/government/Gen_Account_Office/Testimony_Jul17-2002_d02957t.txt:The Congress, through its appropriations subcommittees, has
```
`grep -r "health-care professional" technical` searches for the string "subcommittees" recursively through the technical directory.
The use of `-r` is helpful in this case because it allowed me to search for lines containing the string "subcommittees" in the entire technical directory, rather
than having to specify specific files. Additionally, I got results from multiple directories, 911report and government. The use of `-r` allowed grep to search both of
these directories.

### `grep -l`
(`grep -l «string» «files»`)

The `-l` command returns the only names of the files that contain the specific string, rather than the lines of the files themselves. This is useful when only the names
of files are what need to be determined in a search.

##### Example 1: `grep -l "health-care professional" technical/plos/*`
```
technical/plos/pmed.0020246.txt
technical/plos/pmed.0020257.txt
```
`grep -l "health-care professional" technical/plos/*` searches for the string "health-care professional" in all files with the path `technical/plos/*`.
The use of `-l` is helpful because it returns only the names of the files that contain "health-care professional".

##### Example 2: `grep -l "intergovernmental" technical/government/Gen_Account_Office/*`
```
technical/government/Gen_Account_Office/og96022.txt
technical/government/Gen_Account_Office/og96023.txt
technical/government/Gen_Account_Office/og96026.txt
technical/government/Gen_Account_Office/og96033.txt
technical/government/Gen_Account_Office/og96041.txt
technical/government/Gen_Account_Office/og96042.txt
technical/government/Gen_Account_Office/og96045.txt
technical/government/Gen_Account_Office/og96047.txt
technical/government/Gen_Account_Office/og97041.txt
technical/government/Gen_Account_Office/og97045.txt
technical/government/Gen_Account_Office/og98024.txt
technical/government/Gen_Account_Office/og98030.txt
technical/government/Gen_Account_Office/og98041.txt
technical/government/Gen_Account_Office/og98044.txt
technical/government/Gen_Account_Office/og98046.txt
```
`grep -l "intergovernmental" technical/government/Gen_Account_Office/*` searches for the string "intergovernmental" in all files with the path
`technical/government/Gen_Account_Office/*`. The use of `-l` is helpful because it returns only the names of the files that contain "intergovernmental".

##### Example 3: `grep -l "subcommittees" technical/government/Gen_Account_Office/*`
```
technical/government/Gen_Account_Office/d03232sp.txt
technical/government/Gen_Account_Office/Testimony_cg00010t.txt
technical/government/Gen_Account_Office/Testimony_d01609t.txt
technical/government/Gen_Account_Office/Testimony_Jul17-2002_d02957t.txt
```
`grep -l "subcommittees" technical/government/Gen_Account_Office/*` searches for the string "subcommittees" in all files with the path
`technical/government/Gen_Account_Office/*`. The use of `-l` is helpful because it returns only the names of the files that contain "subcommittees".

### `grep -c`
(`grep -c <<string>> <<files>>`)

The `-c` command returns only the number of lines that contain the given string in the file or files. This is useful when you are only concerned about how many times
a string appears in lines of a file or files.

##### Example 1: `grep -c "health-care professional" technical/plos/pmed.00202*`
```
technical/plos/pmed.0020200.txt:0
technical/plos/pmed.0020201.txt:0
technical/plos/pmed.0020203.txt:0
technical/plos/pmed.0020206.txt:0
technical/plos/pmed.0020208.txt:0
technical/plos/pmed.0020209.txt:0
technical/plos/pmed.0020210.txt:0
technical/plos/pmed.0020212.txt:0
technical/plos/pmed.0020216.txt:0
technical/plos/pmed.0020226.txt:0
technical/plos/pmed.0020231.txt:0
technical/plos/pmed.0020232.txt:0
technical/plos/pmed.0020235.txt:0
technical/plos/pmed.0020236.txt:0
technical/plos/pmed.0020237.txt:0
technical/plos/pmed.0020238.txt:0
technical/plos/pmed.0020239.txt:0
technical/plos/pmed.0020242.txt:0
technical/plos/pmed.0020246.txt:22
technical/plos/pmed.0020247.txt:0
technical/plos/pmed.0020249.txt:0
technical/plos/pmed.0020257.txt:3
technical/plos/pmed.0020258.txt:0
technical/plos/pmed.0020268.txt:0
technical/plos/pmed.0020272.txt:0
technical/plos/pmed.0020273.txt:0
technical/plos/pmed.0020274.txt:0
technical/plos/pmed.0020275.txt:0
technical/plos/pmed.0020278.txt:0
technical/plos/pmed.0020281.txt:0
```
`grep -c "health-care professional" technical/plos/pmed.00202*` searches all files with the path `technical/plos/pmed.00202*`and returns the number of
lines in each file that contain the string "health-care professional". The use of `-c` is helpful when you don't want to see the contents of each file.

##### Example 2: `grep -c "intergovernmental" technical/government/Gen_Account_Office/og980*`
```
technical/government/Gen_Account_Office/og98018.txt:0
technical/government/Gen_Account_Office/og98019.txt:0
technical/government/Gen_Account_Office/og98022.txt:0
technical/government/Gen_Account_Office/og98024.txt:1
technical/government/Gen_Account_Office/og98026.txt:0
technical/government/Gen_Account_Office/og98029.txt:0
technical/government/Gen_Account_Office/og98030.txt:1
technical/government/Gen_Account_Office/og98032.txt:0
technical/government/Gen_Account_Office/og98040.txt:0
technical/government/Gen_Account_Office/og98041.txt:1
technical/government/Gen_Account_Office/og98044.txt:1
technical/government/Gen_Account_Office/og98045.txt:0
technical/government/Gen_Account_Office/og98046.txt:1
```
`grep -c "intergovernmental" technical/government/Gen_Account_Office/og980*` searches all files with the path `technical/government/Gen_Account_Office/og980*`
and returns the number of lines in each file that contain the string "intergovernmental". The use of `-c` is helpful when you don't want to see the
contents of each file.

##### Example 3: `grep -c "subcommittees" technical/government/Gen_Account_Office/Testimony*`
```
technical/government/Gen_Account_Office/Testimony_cg00010t.txt:1
technical/government/Gen_Account_Office/Testimony_d01609t.txt:2
technical/government/Gen_Account_Office/Testimony_Jul15-2002_d02940t.txt:0
technical/government/Gen_Account_Office/Testimony_Jul17-2002_d02957t.txt:2
```
`grep -c "subcommittees" technical/government/Gen_Account_Office/Testimony*` searches all files with the path `technical/government/Gen_Account_Office/Testimony*`
and returns the number of lines in each file that contain the string "subcommittees". The use of `-c` is helpful when you don't want to see the
contents of each file.
