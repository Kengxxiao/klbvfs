# klbvfs
《LoveLive! School Idol Festival All Stars》SQLite VFS

# Example (pseudo code)
  ```
  klbvfs_register(); //klbvfs.dll
  
  fileRealName = "asset_a_ja_0.db_204b005d9bcf65489afed9c6a254d1e8c623cbd2.db";
  uint[] key = GetRawSqliteKey(fileRealName, SQ); //SQ from PlayerPrefs
  newName = fileRealName.rename($"@{key[0]}.{key[1]}.{key[2]}_{fileRealName}");
  sqlite3_file* p;
  sqlite3_open_v2(newName, &p, 1, "klb_vfs");
  
  ...
  ```