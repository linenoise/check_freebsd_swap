NAME
    check_freebsd_swap - Nagios plugin to report on FreeBSD aggregate swap
    file usage

DESCRIPTION
    This script acts as a plugin module for the Nagios IT infrastructure
    monitoring system. It on a FreeBSD server to poll for swap file
    information through pstat(8). This plugin reports on the following 4
    swap file measurements:

    *   available_swap_blocks
    *   swap_usage
    *   total_swap_blocks
    *   used_swap_blocks

    This has been tested with FreeBSD 7.1.

SYNOPSIS
  Command Line Interface
    Get the percentage of swap blocks that are currently in use:

            check_freebsd_swap -m swap_usage -w 80 -c 90

    Get the aggregate number of swap blocks (1k) in use:

            check_freebsd_swap -m used_swap_blocks

    Run this script with command line options stored in a configuration
    file:

            check_freebsd_memory --extra-opts=my_config.ini

SEE ALSO
    If using an external configuration file, it should be structured
    according to the specification at
    <http://nagiosplugins.org/extra-opts/>.

    Thresholds given to this script should be in the format specified at
    <http://nagiosplug.sourceforge.net/developer-guidelines.html>.

    This module is built upon Nagios::Plugin by the Nagios Plugin
    Development Team. Further reading on Nagios, NPRE, and Nagios Plugins is
    available at <http://nagios.com/>.

AUTHOR
    This script is written and maintained by Dann Stayskal
    <dann@stayskal.com> and is available on his website, at
    <http://dann.stayskal.com/software/check_frebsd/>.

LICENSE
    Copyright (C) 2009 by Dann Stayskal.

    This program is free software; you can redistribute it and/or modify it
    under the terms of the GNU General Public License as published by the
    Free Software Foundation; either version 2 of the License, or (at your
    option) any later version.

    This program is distributed in the hope that it will be useful, but
    WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
    Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    59 Temple Place, Suite 330, Boston, MA 02111-1307 USA

    Nagios, the Nagios logo, and Nagios graphics are the servicemarks,
    trademarks, or registered trademarks owned by Nagios Enterprises. All
    other servicemarks and trademarks are the property of their respective
    owner.

