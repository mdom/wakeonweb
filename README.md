# NAME

wakeonweb - Simple dashboard to wake up computers

# DESCRIPTION

This script is a minimal dashboard to list known computers from
_/etc/ethers_ and allows users to wake them up with WOL. It uses your
arp cache to find new machines and add them to _/etc/ethers_.

# INSTALLATION

You can just copy the script somewhere in your cgi-bin. The only
dependencies on debian are perl, lib-mojolicious-perl, wakeonlan and
oping.

# UPDATE DATABASE

To update your ethers file use something like this in your crontab:

    @hourly /usr/lib/cgi-bin/wakeonweb get -M PATCH /update

# BUGS AND LIMITATIONS

The output of the arp command is not standarized. This script currently
only works with arp on linux.

# COPYRIGHT AND LICENSE

Copyright 2020 Mario Domgoergen `<mario@domgoergen.com>`

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as
published by the Free Software Foundation, either version 3 of the
License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
