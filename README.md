# MixBump

This is a simple elixir script to version bump a mix project. This exists
because I often forget to update sub versions and find it tedious to edit the
file by hand each time. Maybe you do too?

## Install

    git clone https://github.com/MaxPower15/mixbump.git
    cd mixbump
    sudo cp mixbump /usr/bin/
    sudo chmod +x /usr/bin/mixbump

The script assumes that the elixir binary exists at `/usr/local/bin/elixir`,
which is the default after installing with homebrew on OSX. If it doesn't
exist there for you, either change the script or add a symlink:

    sudo ln -s /my/actual/elixir /usr/local/bin/elixir

## Usage

Bump sub version without staging or committing:

    mixbump /path/to/mix.exs

Bumb sub version and stage:

    mixbump add /path/to/mix.exs
    mixbump a /path/to/mix.exs

Bump suv version, stage, and commit

    mixbump commit /path/to/mix.exs
    mixbump c /path/to/mix.exs
