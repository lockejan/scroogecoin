# Scroogecoin

Maintainer: Jan Schmitt \
Login: lockejan

---

Implementation of a custom Scroogecoin assignment to fullfill the listed examples below.

## Installation

0. Have leiningen installed on your machine.
1. Just clone the Repository.
2. Navigate into the **"scroogecoin"** directory.
3. Enter **"lein repl"** in your terminal and hit enter. ;)

## Usage

There are different functions available:

- (init!)
- (supervise)
- (append!)
- (verify blockchain signature)
- (get-balance!)

Further informations are given via docstrings.
Example call for docstrings: (doc foo)

## Example

1. Init blockchain \
   (init!)

2. Start supervise mechanism \
   (supervise)

3. Scrooge generates 3.14 coins for Philipp \
   (append! {:sender :Scrooge :recipient :Philipp :amount 3.14})

4. Philipp transfers 1 coin to John \
(append! {:sender :Philipp :recipient :John :amount 1})

5. Michael attempts to transfer 1 coin to Philipp (fails) \
(append! {:sender :Michael :recipient :Philipp :amount 1})

6. Philipp transfers 1 coin to Michael \
(append! {:sender :Philipp :recipient :Michael :amount 1})

7. Verify blockchain \
(let [{:keys [blockchain signature]} @state]
   (verify blockchain signature))

8. Get Balance \
   (get-balance!)

9. Scrooge reinitializes the blockchain. Supervisor-mechanism reports manipulation. \
   (init!)

## License

Copyright © 2019 Jan Schmitt

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
