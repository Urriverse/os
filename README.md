# Default OS

Default Urriverse' build configuration for operating system based on Kernel, used by Kenv build system.

## Usage

Before anything, decide what profile you want. different components select their profiles separately (e.g. there is `KERNEL_PROFILE` for Kernel). You need to check each your component to be set up correctly in your configuration file (`configs/<your_config_name>.env`). To make your life easier, we also publish configs we use for OS development, testing and releasing, as soon as they appears in our daily work. You can look a list of available configurations using `ls configs/*`.

Next, when you selected ready configuration or wrote your own, you need to tell Osenv to use it: `osenv config <your_config_name>`. After this, `.osenv_active` hidden file will be created. It contains the name of active configuration. Don't remove it 'til you use Osenv.

Now, congratulations, you can build and/or run your OS image! to build, use command `osenv build` (or `osenv b`), to run in QEmu use command `osenv run` (or `osenv r`). To run test scripts, use command `osenv test` and all components which support `test` command will execute it.

In file `usage.log` which was not removed intentionally you can see how author of text you are reading used Osenv to build and run dev-image.
