# AndroidStoragePathNote
Android儲存路徑

<h2>Context和Environment的區別</h2>

● Context : 取得在APP環境下面的資料夾，資料會隨著APP移除而刪除
（ex：Context.getFilesDir( ) -> data/data/[package_name]/cache）

● Enviroment : 取得在系統環境的相關資訊，資料不會隨著APP移除而刪除
（ex：Environment.getExternalStoragePublicDirectory(Environment.DIRECTORY_DOWNLOADS); 
-> storage/sdcard0/Download）


<h2>系統環境資料夾位置</h2>

● Environment.getDataDirectory( ) : ```/data```

● Environment.getRootDirectory( ) : ```/system```

● Environment.getExternalStorageDirectory() : ```/storage/sdcard0 或 /mnt/sdcard```

● Environment.getExternalStoragePublicDirectory(“”) : ```同上```

● Environment.getExternalStoragePublicDirectory(“folder1") : ```/storage/sdcard0/folder1```

<h2>內部儲存空間（Internal Storage）</h2>

儲存位置($appDataDir) : ```/data/data/[package_name]```

● Context.getFilesDir( ) : ```($appDataDir)/files```

● Context.getCacheDir( ) : ```($appDataDir)/cache```

● Context.getDir (String name, int mode) : ```($appDataDir)/app_$name```

<h2>外部儲存空間（External Storage）</h2>

儲存位置($appDataDir) : ```/storage/sdcard0/Android/data/[package_name]```

● Context.getExternalFilesDir(“ “) : ```($appDataDir)/files```

● Context.getExternalFilesDir(“ File1 ”) : ```($appDataDir)/files/File1```

● Context.getExternalFilesDir(Environment.Music) : ```($appDataDir)/files/Music```

● Context.getExternalFilesDir(Environment.Picture) : ```($appDataDir)/files/Picture```

● Context.getExternalCacheDir() : ```($appDataDir)/cache```
