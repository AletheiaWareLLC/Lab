Lab
===

A collaborative development environment containing multiple views driven by events stored in a blockchain and transmitted across a network.

1. Alice creates a Lab that runs on her Computer.
2. Alice creates an Experiment that runs in a VM in her Lab.
3. Alice invites others by sharing the IP address of her Lab and the hash of her Experiment.
4. Bob creates a Lab that runs on his Computer and opens Alice's Experiment in a VM in his Lab.
5. Alice and Bob can now Collaborate in their Labs on the same Experiment.
6. Changes made to the files in the Experiment by one Collaborator need to be approved by the other(s).

// TODO - need to work with existing systems; git, linux, sh/bash, golang

- File Tree - see file system hierarchy
- File Editor - read/write file contents
- File Deltas - change history & queue of pending file changes
- Terminal - command/terminal/shell environment

This project defines the data structures of Lab as protocol buffers (https://developers.google.com/protocol-buffers/), allowing implementations in C, C++, C#, Dart, Go, Java, and/or Python.

Build
=====

    ./build.sh --c_out=<c-output>

    ./build.sh --cpp_out=<cpp-output>

    ./build.sh --csharp_out=<csharp-output>

    ./build.sh --dart_out=<dart-output>

    ./build.sh --go_out=<go-output>

    ./build.sh --java_out=lite:<java-output>

    ./build.sh --python_out=<python-output>

// Addition ideas
- Draw - dry-erase/chalk/black/white board style scratch pad for conveying ideas
    message RGBA {
        uint32 red = 1;
        uint32 green = 2;
        uint32 blue = 3;
        uint32 alpha = 4;
    }
    
    message Draw {
        RGBA color = 1;
        uint32 size = 2;
        repeated int32 points = 3 [packed=true];
    }
- Chat - team communication and coordination
    message Chat {
        string text = 1;
    }
- Go - format, vet, build, test, and execute
- Bugs
- Documentation - README/Wiki/Stories/Designs/Requirements/Presentations
- Story - record who, what, when, why, and how (where is irrelevant?)
- Tasks
- Settings - manage experiment and configure settings
 - Network - configure nodes
 - Output - configure distribution/release/OS/architecture
 - Environment - configure execution environment/platform/container/device
- Team - add/delete/list experiment team members
- Views
 - add/delete/cycle/layout/fullscreen/sort views
