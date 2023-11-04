# Quran-Database

Please ⭐️ this repo and share it with others.

# Description

Large database of the entire Quran with many features:

* The Holy Quran is divided into pages, parts, and verses.
* Names of Quranic suras in Arabic and English.
* Verses with and without diacritics.
* Meanings of verses.
* Verse parsing.
* Reasons for the revelation of verses.
* Tafsir (interpretation) of the Quran by al-Saadi, al-Muisir, and al-Baghawi.


# Getting Started  

1- Download `quran.zip` file attached to the repo.

2- Extract `quran.db` file form `quran.zip`.

3- Add `quran.db` file to `assets` file.

4- Add `Room` dependencies to `build.gradle Module Level`.

```Code
    def room_version = "put_latest_version"
    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"
```

5- Create `Aya Class` to represent table.
* For java :
```java
@Entity(tableName = "quran")
public class Aya {

    @NonNull
    @ColumnInfo
    private String aya_text_emlaey;

    @NonNull
    @ColumnInfo
    private String sora_name_en;

    @ColumnInfo
    private int page;

    @ColumnInfo
    private int jozz;

    @ColumnInfo
    private int aya_no;

    @NonNull
    @ColumnInfo
    private String aya_text;

    @NonNull
    @ColumnInfo
    private String sora_name_ar;

    @PrimaryKey
    @ColumnInfo
    private int id;

    @ColumnInfo
    private int line_start;

    @ColumnInfo
    private int sora;


    @ColumnInfo
    private int line_end;

    @NonNull
    @ColumnInfo
    private String maany_aya;

    @NonNull
    @ColumnInfo
    private String earab_quran;

    @NonNull
    @ColumnInfo
    private String reasons_of_verses;

    @NonNull
    @ColumnInfo
    private String tafseer_saadi;

    @NonNull
    @ColumnInfo
    private String tafseer_moysar;

    @NonNull
    @ColumnInfo
    private String tafseer_bughiu;


    @NonNull
    @ColumnInfo
    private String aya_text_tashkil;

    public Aya(@NonNull String aya_text_emlaey, @NonNull String sora_name_en, int page, int jozz, int aya_no, @NonNull String aya_text, @NonNull String sora_name_ar, int id, int line_start, int sora, int line_end, @NonNull String maany_aya, @NonNull String earab_quran, @NonNull String reasons_of_verses, @NonNull String tafseer_saadi, @NonNull String tafseer_moysar, @NonNull String tafseer_bughiu, @NonNull String aya_text_tashkil) {
        this.aya_text_emlaey = aya_text_emlaey;
        this.sora_name_en = sora_name_en;
        this.page = page;
        this.jozz = jozz;
        this.aya_no = aya_no;
        this.aya_text = aya_text;
        this.sora_name_ar = sora_name_ar;
        this.id = id;
        this.line_start = line_start;
        this.sora = sora;
        this.line_end = line_end;
        this.maany_aya = maany_aya;
        this.earab_quran = earab_quran;
        this.reasons_of_verses = reasons_of_verses;
        this.tafseer_saadi = tafseer_saadi;
        this.tafseer_moysar = tafseer_moysar;
        this.tafseer_bughiu = tafseer_bughiu;
        this.aya_text_tashkil = aya_text_tashkil;
    }

    @NonNull
    public String getAya_text_tashkil() {
        return aya_text_tashkil;
    }

    public void setAya_text_tashkil(@NonNull String aya_text_tashkil) {
        this.aya_text_tashkil = aya_text_tashkil;
    }

    @NonNull
    public String getTafseer_saadi() {
        return tafseer_saadi;
    }

    public void setTafseer_saadi(@NonNull String tafseer_saadi) {
        this.tafseer_saadi = tafseer_saadi;
    }

    @NonNull
    public String getTafseer_moysar() {
        return tafseer_moysar;
    }

    public void setTafseer_moysar(@NonNull String tafseer_moysar) {
        this.tafseer_moysar = tafseer_moysar;
    }

    @NonNull
    public String getTafseer_bughiu() {
        return tafseer_bughiu;
    }

    public void setTafseer_bughiu(@NonNull String tafseer_bughiu) {
        this.tafseer_bughiu = tafseer_bughiu;
    }

    @NonNull
    public String getReasons_of_verses() {
        return reasons_of_verses;
    }

    public void setReasons_of_verses(@NonNull String reasons_of_verses) {
        this.reasons_of_verses = reasons_of_verses;
    }

    public void setSora(int sora) {
        this.sora = sora;
    }

    @NonNull
    public String getMaany_aya() {
        return maany_aya;
    }

    public void setMaany_aya(@NonNull String maany_aya) {
        this.maany_aya = maany_aya;
    }

    @NonNull
    public String getEarab_quran() {
        return earab_quran;
    }

    public void setEarab_quran(@NonNull String earab_quran) {
        this.earab_quran = earab_quran;
    }
    
    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public int getJozz() {
        return jozz;
    }

    public void setJozz(int jozz) {
        this.jozz = jozz;
    }

    public int getSora() {
        return sora;
    }

    public void setSoraNumber(int soraNumber) {
        this.sora = soraNumber;
    }

    public String getSora_name_en() {
        return sora_name_en;
    }

    public void setSora_name_en(String sora_name_en) {
        this.sora_name_en = sora_name_en;
    }

    public String getSora_name_ar() {
        return sora_name_ar;
    }

    public void setSora_name_ar(String sora_name_ar) {
        this.sora_name_ar = sora_name_ar;
    }

    public int getPage() {
        return page;
    }

    public void setPage(int page) {
        this.page = page;
    }

    public int getLine_start() {
        return line_start;
    }

    public void setLine_start(int line_start) {
        this.line_start = line_start;
    }

    public int getLine_end() {
        return line_end;
    }

    public void setLine_end(int line_end) {
        this.line_end = line_end;
    }

    public int getAya_no() {
        return aya_no;
    }

    public void setAya_no(int aya_no) {
        this.aya_no = aya_no;
    }

    public String getAya_text() {
        return aya_text;
    }

    public void setAya_text(String aya_text) {
        this.aya_text = aya_text;
    }

    public String getAya_text_emlaey() {
        return aya_text_emlaey;
    }

    public void setAya_text_emlaey(String aya_text_emlaey) {
        this.aya_text_emlaey = aya_text_emlaey;
    }
}
```

*For kotlin :
```kotlin
@Entity(tableName = "quran")
class Aya(
    @field:ColumnInfo var aya_text_emlaey: String,
    @field:ColumnInfo var sora_name_en: String,
    @field:ColumnInfo var page: Int,
    @field:ColumnInfo var jozz: Int,
    @field:ColumnInfo var aya_no: Int,
    @field:ColumnInfo var aya_text: String,
    @field:ColumnInfo var sora_name_ar: String,
    @field:ColumnInfo @field:PrimaryKey var id: Int,
    @field:ColumnInfo var line_start: Int,
    @field:ColumnInfo var sora: Int,
    @field:ColumnInfo var line_end: Int,
    @field:ColumnInfo var maany_aya: String,
    @field:ColumnInfo var earab_quran: String,
    @field:ColumnInfo var reasons_of_verses: String,
    @field:ColumnInfo var tafseer_saadi: String,
    @field:ColumnInfo var tafseer_moysar: String,
    @field:ColumnInfo var tafseer_bughiu: String,
    @field:ColumnInfo var aya_text_tashkil: String
)
```

6- Create `Database Class`

* For java :
```java
@Database(entities = {Aya.class}, version = 1)
public abstract class MyDataBase extends RoomDatabase {

    public static final String DATABASE_NAME = "DatabaseQuran";
    private static volatile MyDataBase myDataBase = null;
    
    public static void initDataBase(Context context) {


        if (myDataBase == null) {
            synchronized (MyDataBase.class) {

                if (myDataBase == null) {

                    Log.e("TAG", "initDataBase: ");

                    myDataBase = Room.databaseBuilder(context,
                                    MyDataBase.class,
                                    DATABASE_NAME)
                            .createFromAsset("quran.db")
                            .allowMainThreadQueries()
                            .fallbackToDestructiveMigration()
                            .build();
                }
            }
        }
    }

    public static MyDataBase getInstance() {
        return myDataBase;
    }
}
```

* For kotlin :
```kotlin
@Database(entities = [Aya::class], version = 1)
abstract class MyDataBase : RoomDatabase() {

    companion object {
        const val DATABASE_NAME = "DatabaseQuran"
        @Volatile
        private var myDataBase: MyDataBase? = null

        fun initDataBase(context: Context) {
            if (myDataBase == null) {
                synchronized(MyDataBase::class.java) {
                    if (myDataBase == null) {
                        Log.e("TAG", "initDataBase: ")
                        myDataBase = Room.databaseBuilder(
                            context.applicationContext,
                            MyDataBase::class.java,
                            DATABASE_NAME
                        )
                            .createFromAsset("quran.db")
                            .allowMainThreadQueries()
                            .fallbackToDestructiveMigration()
                            .build()
                    }
                }
            }
        }

        fun getInstance(): MyDataBase {
            return myDataBase!!
        }
    }
}
```

* Do Not forget to create your own `DAO`

# Modifications

* Use [DB Browser for SQLite](https://sqlitebrowser.org/dl/) to change (add, update, or delete) the database.
