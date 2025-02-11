---
tags: runtime-traditionalweb; 
summary: Advanced use cases for the Section Index UI Pattern.
locale: en-us
guid: fd1fc012-8659-4cd2-861e-220cfa3090ec
app_type: traditional web apps
platform-version: o11
---

# Section Index Reference

<div class="info" markdown="1">

Applies only to Traditional Web Apps.

</div>

## Layout and classes

![](<images/sectionindex-4-diag.png>)

## CSS selectors

| **Element** |  **CSS Class** |  **Description**  |
| ---|---|---  
| .section-index |  .section-index.is--sticky|  Defines if the SectionIndex position is fixed or not  |
| .section-index-item |  .section-index-item.is--active|  Defines the current active link  |

## Advanced use case

### Change active color

1. Write the following CSS in the CSS editor and change the `yourcolor`.

        a.section-index-item.is--active {
            border-left-color: yourcolor;
            color: yourcolor;
        }

1. Or using CSS variables: `var(--color-yourcolor)`.

        a.section-index-item.is--active {
            border-left-color: var(--color-yourcolor);
            color: var(--color-yourcolor);
        }

For RTL compatibility, make sure to also add the following code:

    .is-rtl a.section-index-item.is--active {
        border-right-color: yourcolor;
        color: yourcolor;
    }
