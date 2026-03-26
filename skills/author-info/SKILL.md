---
name: author-info
description: Retrieve author information including website links, donate methods, and resource paths
inputs:
  - name: info_type
    type: string
    description: Type of information to retrieve (all, basic, links, donate, resources)
    required: false
    default: all
  - name: field
    type: string
    description: Specific field to retrieve from the requested info type
    required: false
---

# Author Info Skill

This skill provides access to author information stored in JSON files. It can be used to retrieve author details for documentation, about pages, or project READMEs.

## Data Structure

The author information is stored in three JSON files:

- `data/author.json` - Basic author information (name, bio, email, etc.)
- `data/links.json` - Author's website and social links
- `data/donate.json` - Donate/support methods
- `data/resources/` - Static resources (logos, avatars, etc.)

## Usage

When asked for author information, read the appropriate JSON files and return the requested information:

- **info_type=all**: Returns all author information
- **info_type=basic**: Returns basic info from author.json
- **info_type=links**: Returns website and social links from links.json
- **info_type=donate**: Returns donate methods from donate.json
- **info_type=resources**: Returns resource file paths from resources directory

The data is located in the same directory as this SKILL.md file.

## Examples

- "获取作者的基本信息" → read data/author.json
- "作者的GitHub链接是什么" → read data/links.json and find github field
- "如何打赏作者" → read data/donate.json
- "作者的logo在哪里" → list files in data/resources/ directory
