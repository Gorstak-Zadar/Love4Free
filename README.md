<!-- description: PHP MySQL “Love4Free”: install.php creates profiles/gallery/wall tables; index wall + guest profiles—needs hardening for public Internet. -->

# Love4Free

**PHP** + **MySQL** mini **social / dating** site (profiles, bio fields, gallery, shared **wall** posts).

| File | Role |
|------|------|
| **`install.php`** | Web form for DB host/name/user/password; creates **`profiles`**, **`gallery`**, **`wall_posts`**; writes **`db.php`**; creates **`install.lock`**; deletes itself after success. |
| **`index.php`** | Session-based app: wall posting with **cooldown** and duplicate-message checks; can **auto-create** a **guest** profile for new visitors (see `helpers.php` / session logic). |
| **`profile.php`**, **`create_profile.php`**, **`helpers.php`** | Profile CRUD and utilities. |

**Requirements:** **PHP** with **PDO MySQL**, a **MySQL** server, and a vhost pointing at this folder.

**Security:** This is **demo-style** code. Before any **public** deployment you should add **authentication**, **CSRF** protection, **input validation**, **HTTPS**, **rate limits**, and **regular backups**. Do not expose **`install.php`** after setup.

---

## Usage

1. Upload files to your web root.
2. Browse to **`install.php`**, enter DB credentials, complete install.
3. Use **`index.php`** as the main entry.

---

## Disclaimer

**NO WARRANTY.** THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.

**Limitation of Liability.** IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MODIFIES AND/OR CONVEYS THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

---

## Explained like you're five (the honest kind)

Your PC is a **busy kitchen**. This repo is at best a **sticky note on the fridge**: it might remind you where the knives are, but it does not make you a Michelin chef, and it definitely does not stop someone from sneaking in through the window. We use simple words on purpose so nobody confuses scripts with superpowers.

---

## Disclaimer (read this; it matters)

This software and documentation are provided **“as is”**, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. **Use at your own risk.**

If you do not agree, **do not use** this repository.
