+++
title = "VFS for Git"
author = ["Jethro Kuan"]
lastmod = 2020-06-24T16:10:10+08:00
slug = "vfs_for_git"
draft = false
+++

## Backlinks {#backlinks}

- [Git Scalar]({{< relref "git_scalar" >}})

VFS for [Git]({{< relref "git" >}}) is a virtualized filesystem used to bypass assumptions
about repository size, allowing Git repositories to scale up to large
repositories.

With GVFS, an initial clone downloads a set of pack-files containing
only commits and trees. These objects are sufficient for generating a
view of the working directory, and examining the commit history with
git log.

GVFS allows dynamically downloading objects as needed.
