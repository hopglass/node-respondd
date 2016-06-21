# node-respondd

A respondd server written in node.js.

## Setup

### Installation

1. Copy the contents of this git repository to `/opt/node-respondd`
2. On `systemd` based systems, copy `node-respondd.service` to `/etc/systemd/system/respondd.service`
   and run `systemctl enable node-respondd`.
   On systems without `systemd`, check how to install services.
3. Configure sudo.

### sudo configuration

*node-respondd* requires *sudo* to be set up and configured, such that `bat-list-neighbours` can be 
executed with root privileges by `respondd`. If you use the `respondd.service` for *systemd*, this would
be for user `nobody`.

A possible way to extend suoders file accordingly would be:

    nobody ALL=(root) NOPASSWD: /opt/node-respondd/bat-list-neighbours

## Configuration

With default setup, the file `/opt/node-respondd/config.json` will be read for configuration.
Check `config.json.defaults` for the default configuration values.

## License

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

