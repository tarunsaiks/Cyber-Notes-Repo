# How ACLs Work in Windows
An Access Control List (ACL) in Windows is a fundamental security feature that determines who can access objects (like files, folders, registry keys, or Active Directory objects) and what actions they can perform on those objects [1](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists)[2](https://superuser.com/questions/246280/what-are-windows-acls)[3](https://learn.microsoft.com/en-us/windows-hardware/drivers/ifs/access-control-list).

- An ACL is essentially a list attached to a securable object.
- Each entry in the list is called an Access Control Entry (ACE).
- Each ACE specifies:
    - A _trustee_ (usually a user, group, or system account)
    - The permissions (access rights) allowed, denied, or audited for that trustee [1](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists)[2](https://superuser.com/questions/246280/what-are-windows-acls)[3](https://learn.microsoft.com/en-us/windows-hardware/drivers/ifs/access-control-list).
## Types of ACLs

Windows uses two main types of ACLs:

|Type|Description|
|---|---|
|DACL (Discretionary Access Control List)|Specifies who is allowed or denied access to the object. The owner or someone with the right permissions can modify the DACL. If an object has no DACL, everyone has full access; if the DACL is empty, no one can access the object[1](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists)[3](https://learn.microsoft.com/en-us/windows-hardware/drivers/ifs/access-control-list).|
|SACL (System Access Control List)|Specifies which access attempts should be logged for auditing purposes. For example, it can log successful or failed attempts to read or modify an object[1](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists)[3](https://learn.microsoft.com/en-us/windows-hardware/drivers/ifs/access-control-list).|
## How Permissions Are Evaluated

- When a user or process tries to access an object, Windows checks the object's DACL.
- The system evaluates each ACE in order:
    - If an ACE explicitly denies a requested permission, access is denied immediately.
    - If an ACE allows the requested permission, access is granted unless a previous ACE denied it.
- The order of ACEs matters: Deny entries should come before Allow entries to ensure proper enforcement [3](https://learn.microsoft.com/en-us/windows-hardware/drivers/ifs/access-control-list).
## Inheritance

- ACLs can be inherited: permissions set on a parent folder or object can automatically apply to child objects, simplifying management [2](https://superuser.com/questions/246280/what-are-windows-acls)[5](https://cybergladius.com/the-active-directory-access-control-list-explained/).

## Where ACLs Are Used

- Files and folders (NTFS permissions)
- Registry keys
- Printers and devices
- Active Directory objects [1](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists) [2](https://superuser.com/questions/246280/what-are-windows-acls) [5](https://cybergladius.com/the-active-directory-access-control-list-explained/)
## Example

Suppose a file has the following DACL:

- (Alice, Read)
- (Bob, Full Control)
- (Everyone, Deny Write)

This means:

- Alice can read the file.
- Bob can do anything with the file.
- No one (including Alice and Bob) can write to the file because the "Everyone, Deny Write" ACE takes precedence[2](https://superuser.com/questions/246280/what-are-windows-acls).

## Why ACLs Matter

ACLs are the core mechanism Windows uses to enforce security and permissions. Without them, there would be no way to control who can access or modify system resources[2](https://superuser.com/questions/246280/what-are-windows-acls).

## Summary Table

|Term|Meaning|
|---|---|
|ACL|List of permissions attached to an object|
|ACE|Single entry in an ACL specifying a user/group and their permissions|
|DACL|Controls who can access or is denied access to an object|
|SACL|Controls what access attempts are logged for auditing|

In short, ACLs in Windows are lists that define which users or groups can access an object and what they can do with it, forming the backbone of Windows security [1](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists) [2](https://superuser.com/questions/246280/what-are-windows-acls) [3](https://learn.microsoft.com/en-us/windows-hardware/drivers/ifs/access-control-list).