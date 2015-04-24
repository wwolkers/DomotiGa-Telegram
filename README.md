# DomotiGa-Telegram

uses telegram-cli from https://github.com/vysheng/

quick install instructions:

sudo apt-get install libreadline-dev libconfig-dev libssl-dev lua5.2 liblua5.2-dev libevent-dev make

git clone --recursive https://github.com/vysheng/tg.git && cd tg

./configure

make

bin/telegram-cli -k tg-server.pub -W

The first time you start telegram you must enter the phone number,
including country code (for Netherlands +31).
I used an extra SIM card for this, so that my DomotiGa setup has a
separate Telegram account. (There are SIM cards available from 1 euro
already)

You should receive on your phone an sms message with a code, enter it
and hit "Enter"

Now we are ready to use telegram, if you send a message from your
smartphone you can see it on terminal.

To send a message type

msg Name_Lastname My message from Raspberry

Now create at least 1 contact:

add_contact <phone-number> <first-name> <last-name>

Change the MMain.module:

Change AllowedContacts to specify anyone who is allowed to communicate
with DomotiGa over Telegram.
Change the hTelegramCLI to point to where your tg install is
Change the $sURL to point to your DomotiGa JSON-RPC port

compile the DomotiGa-Telegram helper, and start it.