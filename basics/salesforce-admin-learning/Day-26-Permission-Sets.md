# Day 26: Permission Sets in Salesforce

## What is a Permission Set?

A Permission Set gives:

```text
Extra permissions to a user without changing the Profile.
```

It is used to extend user access.

---

# Why Permission Sets?

Suppose Doctor Profile does not allow:

- Delete Patient

But one Senior Doctor needs it.

Instead of creating a new Profile:

Create:

```text
Delete Patient Access
```

Permission Set.

---

# Profile vs Permission Set

| Profile | Permission Set |
|---|---|
| Mandatory | Optional |
| One Profile per User | Multiple Permission Sets allowed |
| Base Permissions | Extra Permissions |
| Less Flexible | More Flexible |

---

# Important Rule

Permission Sets:

✅ Add permissions

❌ Cannot remove permissions

---

# Real Example

User:

```text
Rahul
```

Profile:

```text
Doctor
```

Permission Sets:

- Delete Patient Access
- Export Reports
- Billing Access

---

# How to Create Permission Set

Navigation:

```text
Gear Icon
 ↓
Setup
 ↓
Permission Sets
 ↓
New
```

Then:

- Give Label
- Select Permissions
- Save
- Assign User

---

# Key Takeaways

- Permission Sets provide additional access.
- Users can have multiple Permission Sets.
- Permission Sets do not replace Profiles.
- Permission Sets only add permissions.
- Salesforce recommends using Permission Sets extensively.

