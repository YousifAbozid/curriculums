# Resources

[Everything you need to know to start with C](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/misc/2022/4/e0ccf91eec6b977a9e00ed384dc285df9c2772e3.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230316%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230316T074237Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=42aeaddbb716e8fbdfe479f0b38039a7b44e4fb88531c40d81619ba488e2ec44)

[“C” Programming Language: Brian Kernighan](https://www.youtube.com/watch?v=de2Hsvxaf8M)

[Why C Programming Is Awesome](https://www.youtube.com/watch?v=smGalmxPVYc)

[Learning to program in C part 1](https://www.youtube.com/watch?v=rk2fK2IIiiQ)

[Learning to program in C part 2](https://www.youtube.com/watch?v=FwpP_MsZWnU)

[Understanding C program Compilation Process](https://www.youtube.com/watch?v=VDslRumKvRA)

[Hash-bang under the hood](https://twitter.com/unix_byte/status/1024147947393495040?s=21)

[Linus Torvalds on C vs. C++](http://harmful.cat-v.org/software/c++/linus)

[Write a script that runs a C file through the preprocessor and saves the result into another file](https://blog.ehoneahobed.com/script-that-runs-a-c-file-through-the-preprocessor)

[Write a script that compiles a C file but does not link](https://blog.ehoneahobed.com/script-that-compiles-a-c-file-but-does-not-link)

[Use -masm=intel](https://stackoverflow.com/questions/199966/how-do-you-use-gcc-to-generate-assembly-code-in-intel-syntax)

[-masm=dialect](https://gcc.gnu.org/onlinedocs/gcc/x86-Options.html#index-masm_003ddialect)

[write()/read() system call - Dextutor](https://dextutor.com/write-read-system-call/)

## Betty linter

To run the Betty linter just with command betty <filename>:

- Go to the [Betty](https://github.com/alx-tools/Betty) repository
- Clone the repo to your local machine
- cd into the Betty directory
- Install the linter with `sudo ./install.sh`
- emacs or vi a new file called betty, and copy the script below:

      #!/bin/bash
      # Simply a wrapper script to keep you from having to use betty-style
      # and betty-doc separately on every item.
      # Originally by Tim Britton (@wintermanc3r), multiargument added by
      # Larry Madeo (@hillmonkey)

      BIN_PATH="/usr/local/bin"
      BETTY_STYLE="betty-style"
      BETTY_DOC="betty-doc"

      if [ "$#" = "0" ]; then
          echo "No arguments passed."
          exit 1
      fi

      for argument in "$@" ; do
          echo -e "\n========== $argument =========="
          ${BIN_PATH}/${BETTY_STYLE} "$argument"
          ${BIN_PATH}/${BETTY_DOC} "$argument"
      done

- Once saved, exit file and change permissions to apply to all users with `chmod a+x betty`
- Move the betty file into `/bin/` directory or somewhere else in your `$PATH` with `sudo mv betty /bin/`
- You can now type `betty <filename>` to run the Betty linter!
