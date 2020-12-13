# HackOff Submission by Team Findvity

> Topic: GE Healthcare challenge

# Apollo

A family of tools for helping support professionals.

## The Idea

The idea here is very simple, we made a set of tools so that the people making the PDFs for field engineers at GE healthcare can also save it as a JSON. Then this JSON can be fed to the CLI, which can parse it and execute some commands.

## Our Approach
The idea, initially, was to parse the pre-exisiting PDFs and generate a JSON as an input to a CLI, which can parse the JSON to execute commands.

We soon realised that scanning and parsing the exisiting PDFs was not the best approach, since OpenCV/Tesseract was very error prone in parsing the PDFs.

Then we started thinking about new approaches. Vasudha suggested a reasonable approach, where the person writing the PDF can itself save it as a JSON. To research more about it, we googled a little and stumbled upon EditorJS, and found it to be very suitable for our approach

  
## Demonstration
[Youtube link](https://youtu.be/zcurNaSbl6k)

# Apollo Editor
[link](https://github.com/Findvity/apollo-editor)

Apollo Editor is a website allows the writers to generate beautiful PDF files for support manuals. They can also save the data as a JSON and export it. Apollo CLI can utilise the JSON to execute commands by itself.

## Tech used
* EditorJS
* HTML
* CSS
* JS

# Apollo CLI
[link](https://github.com/Findvity/apollo)

Apollo is a CLI tool which helps you execute commands and compare responses, then take some decisions accordingly. It takes away the responsibility of wrtiting and executing commands which was error prone in case of a field engineer copying and writing. It acts as a support software and not a replacement of the field engineer.

We used Go because it is highly used in server side tools such as Kubernetes and it has a low memory footprint.

## Tech used
* Go

# Future scope

* The JSON can be uploaded to a central repo and data can be fetched by the CLI in real time (through a REST endpoint)
* There can also be an option for selecting the manual (by heading) in the CLI itself.
* The "Save to PDF" button isn't really functional right now, we're searching for approaches to do that too.
