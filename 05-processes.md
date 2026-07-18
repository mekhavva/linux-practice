# Linux Processes

## Objective

Learn how to monitor, manage, and terminate running processes in Linux.

---

# What is a Process?

A process is a running instance of a program.

Examples:

- Firefox
- Google Chrome
- VS Code
- Terminal
- SSH

Everything running in Linux is a process.

---

# Commands

## 1. ps

### Purpose

Display running processes.

### Syntax

```bash
ps
```

### My Practice

```bash
ps
```

### Output

```  PID TTY          TIME CMD
   5190 pts/0    00:00:00 bash
   8701 pts/0    00:00:00 ps


```

### Notes

Shows processes running in the current terminal.

---

## 2. ps -e

### Purpose

Display all running processes.

### Syntax

```bash
ps -e
```

### My Practice

```bash
ps -e
```

### Output

```   PID TTY          TIME CMD
      1 ?        00:00:15 systemd
      2 ?        00:00:00 kthreadd
      3 ?        00:00:00 pool_workqueue_release
      4 ?        00:00:00 kworker/R-rcu_gp
      5 ?        00:00:00 kworker/R-sync_wq
      6 ?        00:00:00 kworker/R-kvfree_rcu_reclaim
      7 ?        00:00:00 kworker/R-slub_flushwq
      8 ?        00:00:00 kworker/R-netns
     10 ?        00:00:00 kworker/0:0H-kblockd
     13 ?        00:00:00 kworker/R-mm_percpu_wq
     14 ?        00:00:00 ksoftirqd/0
     15 ?        00:00:01 rcu_preempt
     16 ?        00:00:00 rcu_exp_par_gp_kthread_worker/0
     17 ?        00:00:00 rcu_exp_gp_kthread_worker
     18 ?        00:00:00 migration/0
     19 ?        00:00:00 kprobe-optimizer
     20 ?        00:00:00 idle_inject/0
     21 ?        00:00:00 cpuhp/0
     22 ?        00:00:00 kdevtmpfs
     23 ?        00:00:00 kworker/R-inet_frag_wq
     24 ?        00:00:00 rcu_tasks_kthread
     25 ?        00:00:00 rcu_tasks_rude_kthread
     26 ?        00:00:00 kauditd
     27 ?        00:00:00 khungtaskd
     28 ?        00:00:00 oom_reaper
     30 ?        00:00:00 kworker/R-writeback
     32 ?        00:00:02 kcompactd0
     33 ?        00:00:00 ksmd
     34 ?        00:00:00 khugepaged
     35 ?        00:00:00 kworker/R-kblockd
     36 ?        00:00:00 kworker/R-blkcg_punt_bio
     37 ?        00:00:00 kworker/R-kintegrityd
     38 ?        00:00:00 irq/9-acpi
     39 ?        00:00:00 kworker/R-tpm_dev_wq
     40 ?        00:00:00 kworker/R-ata_sff
     41 ?        00:00:00 kworker/R-md_bitmap
     42 ?        00:00:00 kworker/R-md_llbitmap_io
     43 ?        00:00:00 kworker/R-md_llbitmap_unplug
     44 ?        00:00:00 kworker/R-md
     45 ?        00:00:00 kworker/R-edac-poller
     46 ?        00:00:00 kworker/R-devfreq_wq
     47 ?        00:00:00 watchdogd
     48 ?        00:00:00 kworker/R-quota_events_unbound
     49 ?        00:00:11 kswapd0
     50 ?        00:00:00 ecryptfs-kthread
     51 ?        00:00:00 kworker/R-kthrotld
     52 ?        00:00:00 kworker/R-acpi_thermal_pm
     53 ?        00:00:00 scsi_eh_0
     54 ?        00:00:00 kworker/R-scsi_tmf_0
     55 ?        00:00:00 scsi_eh_1
     56 ?        00:00:00 kworker/R-scsi_tmf_1
     60 ?        00:00:00 kworker/R-mld
     61 ?        00:00:00 kworker/R-ipv6_addrconf
     62 ?        00:00:00 kworker/R-kstrp
     64 ?        00:00:00 kworker/u5:0
     77 ?        00:00:00 kworker/R-charger_manager
    319 ?        00:00:00 scsi_eh_2
    320 ?        00:00:00 kworker/R-scsi_tmf_2
    338 ?        00:00:00 jbd2/sda2-8
    339 ?        00:00:00 kworker/R-ext4-rsv-conversion
    551 ?        00:00:02 systemd-journal
    593 ?        00:00:09 systemd-oomd
    595 ?        00:00:01 systemd-resolve
    604 ?        00:00:01 systemd-udevd
    728 ?        00:00:00 psimon
    918 ?        00:00:04 kworker/0:2H-kblockd
    940 ?        00:00:00 avahi-daemon
    941 ?        00:00:00 chronyd-starter
    942 ?        00:00:20 dbus-daemon
    950 ?        00:00:00 networkd-dispat
    953 ?        00:00:02 polkitd
    970 ?        00:00:27 snapd
    972 ?        00:00:00 accounts-daemon
    974 ?        00:00:00 cron
    979 ?        00:00:00 switcheroo-cont
    985 ?        00:00:03 systemd-logind
    986 ?        00:00:00 udisksd
   1032 ?        00:00:00 avahi-daemon
   1050 ?        00:00:01 NetworkManager
   1053 ?        00:00:00 wpa_supplicant
   1073 ?        00:00:01 chronyd
   1082 ?        00:00:00 chronyd
   1091 ?        00:00:00 rsyslogd
   1103 ?        00:00:03 VBoxService
   1166 ?        00:00:00 ModemManager
   1199 ?        00:00:00 unattended-upgr
   1219 ?        00:00:00 gdm3
   1251 ?        00:00:00 kworker/R-ttm
   1476 ?        00:00:00 psimon
   1526 ?        00:00:00 power-profiles-
   1585 ?        00:00:00 rtkit-daemon
   1761 ?        00:00:00 colord
   1793 ?        00:00:23 upowerd
   2347 ?        00:00:02 fwupd
   2591 ?        00:00:00 gdm-session-wor
   2642 ?        00:00:07 systemd
   2644 ?        00:00:00 (sd-pam)
   2664 ?        00:00:03 dbus-daemon
   2666 ?        00:00:00 pipewire
   2668 ?        00:00:00 user-session-he
   2671 ?        00:00:00 gnome-keyring-d
   2672 ?        00:00:00 mpris-proxy
   2673 ?        00:00:01 wireplumber
   2674 ?        00:00:00 pipewire
   2675 ?        00:00:00 pipewire-pulse
   2710 tty2     00:00:00 gdm-wayland-ses
   2738 tty2     00:00:00 gnome-session-i
   2845 ?        00:00:00 gcr-ssh-agent
   2846 ?        00:00:00 gnome-session-c
   2847 ?        00:00:00 ssh-agent
   2854 ?        00:00:00 gvfsd
   2860 ?        00:00:00 gvfsd-fuse
   2872 ?        00:00:00 gnome-session-s
   2890 ?        00:04:32 gnome-shell
   2897 ?        00:00:00 xdg-document-po
   2907 ?        00:00:00 xdg-permission-
   2918 ?        00:00:00 fusermount3
   2943 ?        00:00:00 at-spi-bus-laun
   2950 ?        00:00:00 dbus-daemon
   2952 ?        00:00:00 at-spi2-registr
   3001 ?        00:00:00 gnome-shell-cal
   3018 ?        00:00:00 evolution-sourc
   3037 ?        00:00:00 gjs
   3046 ?        00:00:07 ibus-daemon
   3047 ?        00:00:00 gsd-a11y-settin
   3048 ?        00:00:00 gsd-color
   3049 ?        00:00:00 gsd-datetime
   3052 ?        00:00:00 gsd-housekeepin
   3056 ?        00:00:00 goa-daemon
   3057 ?        00:00:00 gsd-keyboard
   3058 ?        00:00:00 gsd-media-keys
   3059 ?        00:00:00 gsd-power
   3061 ?        00:00:00 gsd-print-notif
   3064 ?        00:00:00 gsd-rfkill
   3065 ?        00:00:00 gsd-screensaver
   3066 ?        00:00:00 gsd-sharing
   3068 ?        00:00:00 gsd-smartcard
   3069 ?        00:00:00 gsd-sound
   3072 ?        00:00:00 gsd-usb-protect
   3077 ?        00:00:00 gsd-wwan
   3080 ?        00:00:00 gsd-disk-utilit
   3082 ?        00:00:00 evolution-alarm
   3088 ?        00:00:00 update-notifier
   3195 ?        00:00:00 evolution-calen
   3210 ?        00:00:00 geoclue
   3256 ?        00:00:00 gsd-printer
   3266 ?        00:00:00 gjs
   3273 ?        00:00:00 goa-identity-se
   3291 ?        00:00:00 ibus-memconf
   3292 ?        00:00:17 ibus-extension-
   3298 ?        00:00:00 ibus-portal
   3300 ?        00:00:00 localsearch-3
   3302 ?        00:00:00 xdg-desktop-por
   3344 ?        00:00:01 xdg-desktop-por
   3348 ?        00:00:00 evolution-addre
   3367 ?        00:00:00 gvfs-udisks2-vo
   3420 ?        00:00:00 gvfs-goa-volume
   3443 ?        00:00:01 gvfs-afc-volume
   3454 ?        00:00:00 gvfs-mtp-volume
   3471 ?        00:00:00 gvfs-gphoto2-vo
   3476 ?        00:00:02 ibus-engine-sim
   3558 ?        00:00:00 gvfsd-metadata
   3599 ?        00:00:00 dconf-service
   3618 ?        00:00:00 gvfsd-trash
   3647 ?        00:00:01 snapd-desktop-i
   3830 ?        00:00:00 xdg-desktop-por
   4368 ?        00:00:00 cupsd
   4369 ?        00:00:00 cups-browsed
   4496 ?        00:00:04 kworker/u4:3-events_unbound
   5054 ?        00:01:33 ptyxis
   5089 ?        00:00:01 ptyxis-agent
   5154 ?        00:00:00 Xwayland
   5159 ?        00:00:00 gsd-xsettings
   5166 ?        00:00:00 mutter-x11-fram
   5185 ?        00:00:00 ibus-x11
   5190 pts/0    00:00:00 bash
   5226 ?        00:02:57 firefox
   5481 ?        00:00:00 crashhelper
   5683 ?        00:00:00 forkserver
   5686 ?        00:00:00 Socket Process
   5738 ?        00:00:07 Privileged Cont
   5747 ?        00:00:00 RDD Process
   5854 ?        00:00:07 snap
   6127 ?        00:00:01 WebExtensions
   6354 ?        00:00:02 kworker/u4:4-ext4-rsv-conversion
   6368 ?        00:01:34 Isolated Web Co
   6371 ?        00:00:30 Isolated Web Co
   6567 ?        00:00:01 Utility Process
   6772 ?        00:00:01 gjs
   6844 ?        00:00:04 Isolated Servic
   7027 ?        00:01:59 Isolated Web Co
   7587 ?        00:00:00 Web Content
   7623 ?        00:00:00 Web Content
   7715 ?        00:00:00 Web Content
   7803 ?        00:00:01 kworker/u4:1-flush-8:0
   7947 ?        00:00:00 ssh-agent
   8025 ?        00:00:00 kworker/0:2-events
   8460 ?        00:00:00 kworker/0:1-cgroup_free
   8573 ?        00:00:00 kworker/u4:0-events_power_efficient
   8738 pts/0    00:00:00 ps


```

---

## 3. ps aux

### Purpose

Display detailed information about all running processes.

### Syntax

```bash
ps aux
```

### My Practice

```bash
ps aux
```

### Output

```
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.1  25552  3076 ?        Ss   09:38   0:15 /usr/lib/systemd/systemd --switched-root --system
root           2  0.0  0.0      0     0 ?        S    09:38   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        S    09:38   0:00 [pool_workqueue_release]
root           4  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-rcu_gp]
root           5  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-sync_wq]
root           6  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-kvfree_rcu_reclaim]
root           7  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-slub_flushwq]
root           8  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-netns]
root          10  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/0:0H-kblockd]
root          13  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-mm_percpu_wq]
root          14  0.0  0.0      0     0 ?        S    09:38   0:00 [ksoftirqd/0]
root          15  0.0  0.0      0     0 ?        I    09:38   0:01 [rcu_preempt]
root          16  0.0  0.0      0     0 ?        S    09:38   0:00 [rcu_exp_par_gp_kthread_worker/0]
root          17  0.0  0.0      0     0 ?        S    09:38   0:00 [rcu_exp_gp_kthread_worker]
root          18  0.0  0.0      0     0 ?        S    09:38   0:00 [migration/0]
root          19  0.0  0.0      0     0 ?        S    09:38   0:00 [kprobe-optimizer]
root          20  0.0  0.0      0     0 ?        S    09:38   0:00 [idle_inject/0]
root          21  0.0  0.0      0     0 ?        S    09:38   0:00 [cpuhp/0]
root          22  0.0  0.0      0     0 ?        S    09:38   0:00 [kdevtmpfs]
root          23  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-inet_frag_wq]
root          24  0.0  0.0      0     0 ?        I    09:38   0:00 [rcu_tasks_kthread]
root          25  0.0  0.0      0     0 ?        I    09:38   0:00 [rcu_tasks_rude_kthread]
root          26  0.0  0.0      0     0 ?        S    09:38   0:00 [kauditd]
root          27  0.0  0.0      0     0 ?        S    09:38   0:00 [khungtaskd]
root          28  0.0  0.0      0     0 ?        S    09:38   0:00 [oom_reaper]
root          30  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-writeback]
root          32  0.0  0.0      0     0 ?        S    09:38   0:02 [kcompactd0]
root          33  0.0  0.0      0     0 ?        SN   09:38   0:00 [ksmd]
root          34  0.0  0.0      0     0 ?        SN   09:38   0:00 [khugepaged]
root          35  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-kblockd]
root          36  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-blkcg_punt_bio]
root          37  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-kintegrityd]
root          38  0.0  0.0      0     0 ?        S    09:38   0:00 [irq/9-acpi]
root          39  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-tpm_dev_wq]
root          40  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-ata_sff]
root          41  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-md_bitmap]
root          42  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-md_llbitmap_io]
root          43  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-md_llbitmap_unplug]
root          44  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-md]
root          45  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-edac-poller]
root          46  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-devfreq_wq]
root          47  0.0  0.0      0     0 ?        S    09:38   0:00 [watchdogd]
root          48  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-quota_events_unbound]
root          49  0.0  0.0      0     0 ?        S    09:38   0:11 [kswapd0]
root          50  0.0  0.0      0     0 ?        S    09:38   0:00 [ecryptfs-kthread]
root          51  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-kthrotld]
root          52  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-acpi_thermal_pm]
root          53  0.0  0.0      0     0 ?        S    09:38   0:00 [scsi_eh_0]
root          54  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-scsi_tmf_0]
root          55  0.0  0.0      0     0 ?        S    09:38   0:00 [scsi_eh_1]
root          56  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-scsi_tmf_1]
root          60  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-mld]
root          61  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-ipv6_addrconf]
root          62  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-kstrp]
root          64  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/u5:0]
root          77  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-charger_manager]
root         319  0.0  0.0      0     0 ?        S    09:38   0:00 [scsi_eh_2]
root         320  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-scsi_tmf_2]
root         338  0.0  0.0      0     0 ?        S    09:38   0:00 [jbd2/sda2-8]
root         339  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-ext4-rsv-conversion]
root         551  0.0  0.1  51052  2156 ?        S<s  09:38   0:02 /usr/lib/systemd/systemd-journald
systemd+     593  0.0  0.0  16804  1400 ?        Ss   09:38   0:09 /usr/lib/systemd/systemd-oomd
systemd+     595  0.0  0.1  22804  2576 ?        Ss   09:38   0:01 /usr/lib/systemd/systemd-resolved
root         604  0.0  0.0  42596  1256 ?        Ss   09:38   0:01 /usr/lib/systemd/systemd-udevd
root         728  0.0  0.0      0     0 ?        S    09:38   0:00 [psimon]
root         918  0.0  0.0      0     0 ?        I<   09:38   0:04 [kworker/0:2H-kblockd]
avahi        940  0.0  0.0   6740  1216 ?        Ss   09:38   0:00 avahi-daemon: running [havva-VirtualBox.local]
root         941  0.0  0.0   2888   540 ?        Ss   09:38   0:00 /bin/sh /usr/lib/systemd/scripts/chronyd-starter.
message+     942  0.1  0.1  11920  3036 ?        Ss   09:38   0:20 @dbus-daemon --system --address=systemd: --nofork
root         950  0.0  0.0  58108  1680 ?        Ss   09:38   0:00 /usr/bin/python3 /usr/bin/networkd-dispatcher --r
polkitd      953  0.0  0.2 324120  3908 ?        Ssl  09:38   0:02 /usr/lib/polkit-1/polkitd --no-debug --log-level=
root         970  0.1  0.8 1776664 13480 ?       Ssl  09:38   0:27 /snap/snapd/current/usr/lib/snapd/snapd
root         972  0.0  0.1 320856  2016 ?        Ssl  09:38   0:00 /usr/libexec/accounts-daemon
root         974  0.0  0.0  18344  1012 ?        Ss   09:38   0:00 /usr/sbin/cron -f -P
root         979  0.0  0.1 319080  2056 ?        Ssl  09:38   0:00 /usr/libexec/switcheroo-control
root         985  0.0  0.1  18560  1992 ?        Ss   09:38   0:03 /usr/lib/systemd/systemd-logind
root         986  0.0  0.1 543780  2808 ?        Ssl  09:38   0:00 /usr/libexec/udisks2/udisksd
avahi       1032  0.0  0.0   6560   460 ?        S    09:38   0:00 avahi-daemon: chroot helper
root        1050  0.0  0.3 569016  5604 ?        Ssl  09:38   0:01 /usr/sbin/NetworkManager --no-daemon
root        1053  0.0  0.0  17956   868 ?        Ss   09:38   0:00 /usr/sbin/wpa_supplicant -u -s -O DIR=/run/wpa_su
_chrony     1073  0.0  0.0  24592  1200 ?        S    09:38   0:01 /usr/sbin/chronyd -n -F 1
_chrony     1082  0.0  0.0  12116   544 ?        S    09:38   0:00 /usr/sbin/chronyd -n -F 1
syslog      1091  0.0  0.0 220604   956 ?        Ssl  09:38   0:00 /usr/sbin/rsyslogd -n -iNONE
root        1103  0.0  0.0 368920  1100 ?        Sl   09:38   0:03 /usr/sbin/VBoxService
root        1166  0.0  0.1 391604  2040 ?        Ssl  09:38   0:00 /usr/sbin/ModemManager
root        1199  0.0  0.1 137380  1928 ?        Ssl  09:38   0:00 /usr/bin/python3 /usr/share/unattended-upgrades/u
root        1219  0.0  0.1 396016  2484 ?        Ssl  09:38   0:00 /usr/sbin/gdm3
root        1251  0.0  0.0      0     0 ?        I<   09:38   0:00 [kworker/R-ttm]
root        1476  0.0  0.0      0     0 ?        S    09:38   0:00 [psimon]
root        1526  0.0  0.1 320556  2364 ?        Ssl  09:38   0:00 /usr/libexec/power-profiles-daemon
rtkit       1585  0.0  0.0  21872   924 ?        SNsl 09:39   0:00 /usr/libexec/rtkit-daemon
colord      1761  0.0  0.1 328720  2128 ?        Ssl  09:39   0:00 /usr/libexec/colord
root        1793  0.1  0.1 330276  3200 ?        Ssl  09:39   0:24 /usr/libexec/upowerd
root        2347  0.0  0.2 376096  3444 ?        Ssl  10:19   0:02 /usr/libexec/fwupd/fwupd
root        2591  0.0  0.1 397160  2056 ?        Sl   10:51   0:00 gdm-session-worker [pam/gdm-password]
havva       2642  0.0  0.1  23572  1976 ?        Ss   10:51   0:07 /usr/lib/systemd/systemd --user
havva       2644  0.0  0.0  23448   716 ?        S    10:51   0:00 (sd-pam)
havva       2664  0.0  0.1  10080  2412 ?        Ss   10:51   0:03 /usr/bin/dbus-daemon --session --address=systemd:
havva       2666  0.0  0.4 119980  7240 ?        S<sl 10:51   0:00 /usr/bin/pipewire
havva       2668  0.0  0.0 303924  1444 ?        Ssl  10:51   0:00 /snap/snapd-desktop-integration/387/usr/bin/user-
havva       2671  0.0  0.1 194520  1892 ?        SLsl 10:51   0:00 /usr/bin/gnome-keyring-daemon --foreground --comp
havva       2672  0.0  0.0   7560  1216 ?        Ss   10:51   0:00 /usr/bin/mpris-proxy
havva       2673  0.0  0.3 498964  6468 ?        S<sl 10:51   0:01 /usr/bin/wireplumber
havva       2674  0.0  0.0  96096   996 ?        Ssl  10:51   0:00 /usr/bin/pipewire -c filter-chain.conf
havva       2675  0.0  0.3 189664  6280 ?        S<sl 10:51   0:00 /usr/bin/pipewire-pulse
havva       2710  0.0  0.1 179480  1712 tty2     Ssl+ 10:51   0:00 /usr/libexec/gdm-wayland-session /usr/bin/gnome-s
havva       2738  0.0  0.1 175204  1740 tty2     Sl+  10:51   0:00 /usr/libexec/gnome-session-init-worker ubuntu
havva       2845  0.0  0.1 310552  2572 ?        Ssl  10:51   0:00 /usr/libexec/gcr-ssh-agent --base-dir /run/user/1
havva       2846  0.0  0.0  98492  1428 ?        Ssl  10:51   0:00 /usr/libexec/gnome-session-ctl --monitor
havva       2847  0.0  0.0  10480   552 ?        Ss   10:51   0:00 /usr/bin/ssh-agent -D
havva       2854  0.0  0.1 324292  1788 ?        Ssl  10:51   0:00 /usr/libexec/gvfsd
havva       2860  0.0  0.1 335920  1832 ?        Sl   10:51   0:00 /usr/libexec/gvfsd-fuse /run/user/1000/gvfs -f
havva       2872  0.0  0.1 550812  3180 ?        Ssl  10:51   0:00 /usr/libexec/gnome-session-service --session=ubun
havva       2890  2.1  8.0 3542768 135992 ?      Rsl  10:51   4:39 /usr/bin/gnome-shell --mode=ubuntu
havva       2897  0.0  0.1 642076  1856 ?        Ssl  10:51   0:00 /usr/libexec/xdg-document-portal
havva       2907  0.0  0.1 318648  2016 ?        Ssl  10:51   0:00 /usr/libexec/xdg-permission-store
root        2918  0.0  0.0   2792   596 ?        Ss   10:51   0:00 fusermount3 -o rw,nosuid,nodev,fsname=portal,auto
havva       2943  0.0  0.1 381076  1812 ?        Ssl  10:51   0:00 /usr/libexec/at-spi-bus-launcher
havva       2950  0.0  0.0   8608  1108 ?        S    10:51   0:00 /usr/bin/dbus-daemon --config-file=/usr/share/def
havva       2952  0.0  0.1 168680  2200 ?        Sl   10:51   0:00 /usr/libexec/at-spi2-registryd --use-gnome-sessio
havva       3001  0.0  0.1 658564  1820 ?        Sl   10:51   0:00 /usr/libexec/gnome-shell-calendar-server
havva       3018  0.0  0.1 839832  2284 ?        Ssl  10:51   0:00 /usr/libexec/evolution-source-registry
havva       3037  0.0  0.1 2603268 2992 ?        Sl   10:51   0:00 /usr/bin/gjs -m /usr/share/gnome-shell/org.gnome.
havva       3046  0.0  0.1 396808  2684 ?        Ssl  10:51   0:08 /usr/bin/ibus-daemon --panel disable
havva       3047  0.0  0.1 265020  2228 ?        Ssl  10:51   0:00 /usr/libexec/gsd-a11y-settings
havva       3048  0.0  0.1 402252  2472 ?        Ssl  10:51   0:00 /usr/libexec/gsd-color
havva       3049  0.0  0.1 271384  2184 ?        Ssl  10:51   0:00 /usr/libexec/gsd-datetime
havva       3052  0.0  0.1 401992  2676 ?        Rsl  10:51   0:00 /usr/libexec/gsd-housekeeping
havva       3056  0.0  0.1 478052  2268 ?        Sl   10:51   0:00 /usr/libexec/goa-daemon
havva       3057  0.0  0.1 394360  2212 ?        Ssl  10:51   0:00 /usr/libexec/gsd-keyboard
havva       3058  0.0  0.2 702232  3880 ?        Ssl  10:51   0:00 /usr/libexec/gsd-media-keys
havva       3059  0.0  0.2 561816  3572 ?        Rsl  10:51   0:00 /usr/libexec/gsd-power
havva       3061  0.0  0.1 338844  2428 ?        Ssl  10:51   0:00 /usr/libexec/gsd-print-notifications
havva       3064  0.0  0.1 468208  2380 ?        Ssl  10:51   0:00 /usr/libexec/gsd-rfkill
havva       3065  0.0  0.1 181116  2068 ?        Rsl  10:51   0:00 /usr/libexec/gsd-screensaver-proxy
havva       3066  0.0  0.1 478620  2412 ?        Ssl  10:51   0:00 /usr/libexec/gsd-sharing
havva       3068  0.0  0.1 396936  2176 ?        Ssl  10:51   0:00 /usr/libexec/gsd-smartcard
havva       3069  0.0  0.1 266168  2320 ?        Ssl  10:51   0:00 /usr/libexec/gsd-sound
havva       3072  0.0  0.1 491624  2184 ?        Ssl  10:51   0:00 /usr/libexec/gsd-usb-protection
havva       3077  0.0  0.1 401636  2240 ?        Rsl  10:51   0:00 /usr/libexec/gsd-wwan
havva       3080  0.0  0.1 312172  1844 ?        Sl   10:51   0:00 /usr/libexec/gsd-disk-utility-notify
havva       3082  0.0  0.1 859264  2688 ?        Sl   10:51   0:00 /usr/libexec/evolution-data-server/evolution-alar
havva       3088  0.0  0.1 654780  3012 ?        Sl   10:51   0:00 /usr/bin/update-notifier
havva       3195  0.0  0.1 708024  1940 ?        Ssl  10:51   0:00 /usr/libexec/evolution-calendar-factory
geoclue     3210  0.0  0.1 639524  2296 ?        Ssl  10:51   0:00 /usr/libexec/geoclue
havva       3256  0.0  0.1 418952  1792 ?        Sl   10:51   0:00 /usr/libexec/gsd-printer
havva       3266  0.0  0.1 2602356 2988 ?        Sl   10:51   0:00 /usr/bin/gjs -m /usr/share/gnome-shell/org.gnome.
havva       3273  0.0  0.1 399216  1864 ?        Sl   10:51   0:00 /usr/libexec/goa-identity-service
havva       3291  0.0  0.1 180460  1848 ?        Sl   10:51   0:00 /usr/libexec/ibus-memconf
havva       3292  0.1  0.1 511132  3188 ?        Sl   10:51   0:17 /usr/libexec/ibus-extension-gtk3
havva       3298  0.0  0.1 319780  1848 ?        Sl   10:51   0:00 /usr/libexec/ibus-portal
havva       3300  0.0  0.1 674940  2624 ?        SNsl 10:51   0:00 /usr/libexec/localsearch-3
havva       3302  0.0  0.2 640468  4712 ?        Ssl  10:51   0:00 /usr/libexec/xdg-desktop-portal
havva       3344  0.0  0.2 551552  3628 ?        Ssl  10:51   0:01 /usr/libexec/xdg-desktop-portal-gnome
havva       3348  0.0  0.1 706204  1952 ?        Ssl  10:51   0:00 /usr/libexec/evolution-addressbook-factory
havva       3367  0.0  0.1 398172  2076 ?        Ssl  10:51   0:00 /usr/libexec/gvfs-udisks2-volume-monitor
havva       3420  0.0  0.1 319116  1848 ?        Ssl  10:51   0:00 /usr/libexec/gvfs-goa-volume-monitor
havva       3443  0.0  0.1 401152  1888 ?        Ssl  10:51   0:01 /usr/libexec/gvfs-afc-volume-monitor
havva       3454  0.0  0.1 319164  2056 ?        Ssl  10:51   0:00 /usr/libexec/gvfs-mtp-volume-monitor
havva       3471  0.0  0.1 320132  2044 ?        Ssl  10:51   0:00 /usr/libexec/gvfs-gphoto2-volume-monitor
havva       3476  0.0  0.1 180584  2456 ?        Sl   10:51   0:02 /usr/libexec/ibus-engine-simple
havva       3558  0.0  0.1 180104  2236 ?        Ssl  10:51   0:00 /usr/libexec/gvfsd-metadata
havva       3599  0.0  0.1 165348  1792 ?        Ssl  10:52   0:00 /usr/libexec/dconf-service
havva       3618  0.0  0.1 545780  1880 ?        Sl   10:52   0:00 /usr/libexec/gvfsd-trash --spawner :1.17 /org/gtk
havva       3647  0.0  0.1 518288  1720 ?        Sl   10:52   0:01 /snap/snapd-desktop-integration/387/usr/bin/snapd
havva       3830  0.0  0.2 503440  3992 ?        Ssl  10:52   0:00 /usr/libexec/xdg-desktop-portal-gtk
root        4368  0.0  0.0  40744  1564 ?        Ss   11:31   0:00 /usr/sbin/cupsd -l
cups-br+    4369  0.0  0.1 207528  2120 ?        Ssl  11:31   0:00 /usr/sbin/cups-browsed
root        4496  0.0  0.0      0     0 ?        I    12:11   0:04 [kworker/u4:3-events_unbound]
havva       5054  4.9  5.0 1156704 84612 ?       Rl   13:52   1:41 /usr/bin/ptyxis --gapplication-service
havva       5089  0.0  0.1 239944  2224 ?        Ssl  13:52   0:01 /usr/libexec/ptyxis-agent --socket-fd=3 --rlimit-
havva       5154  0.0  0.0 212032  1564 ?        S    13:52   0:00 /usr/bin/Xwayland :0 -rootless -noreset -accessx 
havva       5159  0.0  0.1 262584  2600 ?        Ssl  13:52   0:00 /usr/libexec/gsd-xsettings
havva       5166  0.0  0.2 843780  5028 ?        Sl   13:52   0:00 /usr/libexec/mutter-x11-frames
havva       5185  0.0  0.1 373876  2424 ?        Sl   13:52   0:00 /usr/libexec/ibus-x11
havva       5190  0.0  0.1  20108  2552 pts/0    Ss   13:52   0:00 /usr/bin/bash
havva       5226  8.7 17.6 12187560 296340 ?     Sl   13:53   2:58 /snap/firefox/8107/usr/lib/firefox/firefox
havva       5481  0.0  0.0 149388   548 ?        Sl   13:53   0:00 /snap/firefox/8107/usr/lib/firefox/crashhelper 52
havva       5683  0.0  0.5 445544  9072 ?        S    13:53   0:00 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       5686  0.0  0.9 460008 16112 ?        Sl   13:53   0:00 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       5738  0.3  2.8 2630444 47168 ?       Sl   13:53   0:07 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       5747  0.0  0.8 633836 14796 ?        Sl   13:53   0:00 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       5854  0.3  0.3 1692504 6520 ?        Sl   13:53   0:07 /snap/snapd/current/usr/bin/snap userd
havva       6127  0.0  1.8 2608044 31504 ?       Sl   13:53   0:01 /snap/firefox/8107/usr/lib/firefox/firefox -conte
root        6354  0.1  0.0      0     0 ?        I    13:53   0:02 [kworker/u4:4-ext4-rsv-conversion]
havva       6368  4.8  6.8 11358832 115284 ?     Sl   13:53   1:35 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       6371  1.5  4.6 2966224 78928 ?       Sl   13:53   0:30 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       6567  0.0  0.9 636144 16532 ?        Sl   13:53   0:01 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       6772  0.0  0.4 2808152 7852 ?        Sl   13:54   0:01 gjs /usr/share/gnome-shell/extensions/ding@raster
havva       6844  0.2  1.9 2587276 33084 ?       Sl   13:54   0:04 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       7027  6.2 19.6 3334608 330656 ?      Sl   13:55   1:59 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       7587  0.0  1.5 2570296 26112 ?       Sl   14:04   0:00 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       7623  0.0  1.5 2570296 26156 ?       Sl   14:04   0:00 /snap/firefox/8107/usr/lib/firefox/firefox -conte
havva       7715  0.0  1.5 2570296 26164 ?       Sl   14:05   0:00 /snap/firefox/8107/usr/lib/firefox/firefox -conte
root        7803  0.1  0.0      0     0 ?        I    14:06   0:01 [kworker/u4:1-flush-8:0]
havva       7947  0.0  0.1  10496  1924 ?        S    14:08   0:00 /usr/bin/ssh-agent -D -a /run/user/1000/gcr/.ssh
root        8025  0.0  0.0      0     0 ?        I    14:09   0:00 [kworker/0:2-events]
root        8460  0.0  0.0      0     0 ?        I    14:19   0:00 [kworker/0:1-cgroup_free]
root        8573  0.0  0.0      0     0 ?        I    14:22   0:00 [kworker/u4:0-events_power_efficient]
havva       8780  100  0.2  21320  5000 pts/0    R+   14:27   0:00 ps aux

```

### Notes

Very common command for Linux administrators.

---

## 4. top

### Purpose

Display live system processes.

### Syntax

```bash
top
```

### My Practice

```bash
top
```

### Output

```

top - 14:37:22 up  4:59,  1 user,  load average: 2.21, 1.16, 1.02
Tasks: 203 total,   2 running, 201 sleeping,   0 stopped,   0 zombie
%Cpu(s): 45.5 us,  7.1 sy,  0.0 ni, 45.5 id,  0.0 wa,  0.0 hi,  2.0 si,  0.0 st 
MiB Mem :   1642.9 total,     90.2 free,   1036.9 used,    581.0 buff/cache     
MiB Swap:   2048.0 total,    851.0 free,   1197.0 used.    606.0 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                      
   5054 havva     20   0 1156872  68336  52088 S  29.5   4.1   2:24.45 ptyxis                                       
   2890 havva     20   0 3561552 168848  64088 R  19.0  10.0   5:25.61 gnome-shell                                  
   6368 havva     20   0   10.8g 108320  27152 S   4.9   6.4   2:05.65 Isolated Web Co                              
   5226 havva     20   0   11.6g 256008  68488 S   1.3  15.2   3:24.45 firefox                                      
   7027 havva     20   0 3321280 269704  38116 S   0.7  16.0   2:12.91 Isolated Web Co                              
    942 message+  20   0   11920   3728   1420 S   0.3   0.2   0:20.99 dbus-daemon                                  
   8855 havva     20   0   22068   4508   3808 R   0.3   0.3   0:04.31 top                                          
   8918 root      20   0       0      0      0 I   0.3   0.0   0:00.29 kworker/u4:1-events_unbound                  
      1 root      20   0   25552   7608   4616 S   0.0   0.5   0:15.80 systemd                                      
      2 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kthreadd                                     
      3 root      20   0       0      0      0 S   0.0   0.0   0:00.00 pool_workqueue_release                       
      4 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-rcu_gp                             
      5 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-sync_wq                            
      6 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-kvfree_rcu_reclaim                 
      7 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-slub_flushwq                       
      8 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-netns                              
     10 root       0 -20       0      0      0 I   0.0   0.0   0:00.05 kworker/0:0H-kblockd                         
     13 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-mm_percpu_wq                       
     14 root      20   0       0      0      0 S   0.0   0.0   0:00.54 ksoftirqd/0 
```

### Notes

Press q to quit.

---

## 5. htop

### Purpose

Interactive process viewer.

### Syntax

```bash
htop
```

### My Practice

```bash
htop
```


### Notes

If not installed:

```bash
sudo apt install htop
```

---

## 6. pidof

### Purpose

Find the Process ID (PID) of a program.

### Syntax

```bash
pidof program_name
```

### Example

```bash
pidof bash
```

### Output

```5190
```

---

## 7. pgrep

### Purpose

Search processes by name.

### Syntax

```bash
pgrep bash
```

### Output

```5190


```

---

## 8. kill

### Purpose

Terminate a process using its PID.

### Syntax

```bash
kill PID
```

### Example

```bash
kill 2458
```

### Notes

Use only with processes you own.

---

## 9. kill -9

### Purpose

Force terminate a process.

### Syntax

```bash
kill -9 PID
```

### Notes

Use only if a normal kill does not work.

---

## 10. jobs

### Purpose

Display background jobs.

### Syntax

```bash
jobs
```


## 11. bg

### Purpose

Continue a suspended job in the background.

### Syntax

```bash
bg
```

---

## 12. fg

### Purpose

Bring a background job to the foreground.

### Syntax

```bash
fg
```

---

# Important Concepts

## PID

Every process has a unique Process ID.

Example

```text
PID = 3215
```

---

## Foreground Process

Runs in the current terminal.

Example:

nano

---

## Background Process

Runs while the terminal remains usable.

Example

```bash
firefox &
```

---

# Common Errors

Example

```text
kill: (12345): No such process
```

Reason

The PID does not exist.

---

Example

```text
Operation not permitted
```

Reason

You do not own the process.

---

# Summary

After completing this lesson I can:

- Display running processes.
- Find a PID.
- Monitor CPU and memory usage.
- Kill a process.
- Understand foreground and background jobs.
