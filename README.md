gvillalta99.haskell
===================

Installs haskell.

Installation
------------

`$ ansible-galaxy install gvillalta99.haskell`

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: gvillalta99.haskell
           tags:
             - haskell
             - development
            haskell:
              release_year: "2014"
              version: "2.0.0"
              tmp_dir: "/tmp"
              parent_dir: "/usr/local"
              post_install_commands:
                - cabal update
                - cabal install cabal-install --force-reinstall
                - cabal install ghc-mod --force-reinstall


It's advisable to set the following in your `ansible.cfg`:

    [defaults]
    hash_behavior = merge

Requirements
------------

- Tested on Ubuntu Trusty 14.04

License
-------

BSD
