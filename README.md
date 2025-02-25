# Lagom2 Customization
- Repository containing customisation files for the WHMCS Lagom 2 theme.
- Depends on `/lagom2` theme placed in `[WHMCS ROOT]/templates/`.
- Active theme style: **Depth**.
- Custom CSS added: `core\styles\depth\assets\css\theme-custom.css`.
- Activate a template via `/admin/addonmodules.php?templateName=lagom2&controller=Template&action=pages&module=RSThemes`.

| **Lagom Version** | **Repository** |
|-|-|
| 2.2.7 | `git clone https://repos.blacknight.ie/Systems/WHMCS/Templates/lagom-customization` |

## Customizations
- Most modified .tpl files are copied from `/templates/lagom2`, edited and placed into `/templates/lagom2/core/pages/$template$/blacknight`.
- `navbar.tpl` is copied from `/templates/lagom2/includes`, edited and placed into `/templates/lagom2/includes/overwrites`.
- `sort_countries.php` Supplied by RSThemes and added to `core\hooks`.

| **Tested** | **WHMCS** | **File** | **Description** |
|-|-|-|-|
| ✔ | 8.10.1 | `clientareadetails.tpl` | - Include **Client ID** input field (readonly) under **Personal Information** heading in `/clientarea.php?action=details`. |
| ✔ | 8.10.1 | `clientareadomains.tpl` | - Reorder **My Domains** DataTable columns in `/clientarea.php?action=domains`.<br>- Change domain **href** to `/clientarea.php?action=domaindetails&id=XX` in same window. |
| ✔ | 8.10.1 | `clientareaproductdetails.tpl` | - Move `{$moduleclientarea}` above `{if !$customModuleInfo}`.<br>- If it exists, include [formatBytes](https://repos.blacknight.ie/Systems/WHMCS/Custom-Hooks/custom-hooks-collection) function to display usage in meaningful values such as Mb, Gb etc. |
| ✔ | 8.10.1 | `clientareaproducts.tpl` | - Reorder **My Products & Services** DataTable columns in `/clientarea.php?action=services`.<br>- Change domain **href** to `clientarea.php?action=productdetails&id={$service.id}` in same window. |
| ✔ | 8.10.1 | `invoicepdf.tpl` | - Include Blacknight's UK VAT Number for UK based customers.<br>- Append Client ID after customer/business name.<br>- Append item type & relid to each invoice item.<br>- Include reverse charge text under invoice items table.<br>- Include Blacknight's bank details in footer.<br>- Remove transaction ID from Transactions table.<br>- Adjust line heights in different areas of the PDF. |
| ✔ | 8.10.1 | `viewinvoice.tpl` | - Include Blacknight's UK VAT Number for UK based customers.<br>- Append item type & relid to each invoice item. |
| ✔ | 8.10.1 | `navbar.tpl` | - Include Client ID in `.dropdown-header-info` for account dropdown (2 inclusions). |
| ✔ | 8.10.1 | `sort_countries.php` | - Assume it sorts countries. |
| ✔ | 8.10.1 | `irish.svg` | - Replace UK flag with IE flag by adding to `assets\img\flags` and set in `theme-custom.css`. |

## Comments
- Look out for *HTML*, *PHP* and *Javascript* comments that identify start/end of Blacknight lagom2 customisations.

**HTML**
```html
<!-- start repo-lagom-customization -->
<!-- end repo-lagom-customization -->
```
**JavaScript & PHP**
```javascript
/* start repo-lagom-customization */
/* end repo-lagom-customization */
```
