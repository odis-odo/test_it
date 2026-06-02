
Robocopy preserves file timestamps by default as the standard `/COPY:DAT` switch automatically includes **Data**,**Attributes**,and **Timestamps**. The directory (folder) timestamps are not preserved by default; the default behavior for folders is to copy only **Data** and **Attributes** (equivalent to `/DCOPY:DA)`.  

To preserve folder timestamps (Creation, Modified and Access times), youo must add the `/DCOPY:T` switch to your command. For example:  

```cmd
robocopy source destination /COPY:DAT /DCOPY:T
```  

Robocopy's default behavior:  

- **File Timestamps**: Always copied (Default `/COPY:DAT`)
- **Folder Timestamps: **Not** copied by default; requires `/DCOPY:T`
- **File Attributes**: Always copied by default (part of `/COPY:DAT`)
- **Security/Permissions**: **Not** copied by default; requires `/COPY:S` or `/SEC`  


If you need to copy all file and folder information including security and timestamps, use `/COPY:ALL` switch combined with `/DCOPY:DAT` (for example `/COPY:ALL /DCOPY:DAT`) to ensure folder timestamps are included.