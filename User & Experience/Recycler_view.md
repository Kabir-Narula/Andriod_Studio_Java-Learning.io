
# Cheat Sheet 4.5: RecyclerView



## 1. RecyclerView components
To display data in a RecyclerView, you need the following:

- **Data**: Data can come from any source (locally, from a database, or from cloud storage).
- **RecyclerView**: The main container that holds list items in a scrollable view.
- **Item Layout**: XML layout for each item that will appear in the list.
- **Layout Manager**: Manages the layout of list items. Use one of the built-in managers:
    - LinearLayoutManager: For vertical or horizontal lists.
    - GridLayoutManager: For grid arrangements.
    - StaggeredGridLayoutManager: For staggered grid layouts.
- **Adapter**: Connects data to the RecyclerView. It tells the RecyclerView how to display data.
- **ViewHolder**: Holds the layout for a single list item. Each ViewHolder is managed by the Adapter.

RecyclerView architecture is built for efficiency, caching View items and reusing them as they move in and out of the screen, minimizing memory usage.

---

## 2. Implementing a RecyclerView

### Step-by-step:
1. **Add the RecyclerView dependency**: 
   If needed, add the RecyclerView dependency in the `build.gradle` file:
   
   ```gradle
   implementation 'com.android.support:recyclerview-v7:26.1.0'
   ```

2. **Add RecyclerView to the Activity layout**:
   Include a RecyclerView in your activity layout XML:

   ```xml
   <android.support.v7.widget.RecyclerView
        android:id="@+id/recyclerview"
        android:layout_width="match_parent"
        android:layout_height="match_parent">
   </android.support.v7.widget.RecyclerView>
   ```

3. **Create an item layout**: 
   Define the XML layout for one item in the list:

   ```xml
   <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
       android:layout_width="match_parent"
       android:layout_height="wrap_content"
       android:orientation="vertical"
       android:padding="6dp">

       <TextView
           android:id="@+id/word"
           style="@style/word_title" />
   </LinearLayout>
   ```

4. **Create an Adapter**: 
   Extend `RecyclerView.Adapter` to bind data to the View items.

   ```java
   public class WordListAdapter extends RecyclerView.Adapter<WordListAdapter.WordViewHolder> {
       private final LayoutInflater mInflater;
       private final LinkedList<String> mWordList;

       public WordListAdapter(Context context, LinkedList<String> wordList) {
           mInflater = LayoutInflater.from(context);
           this.mWordList = wordList;
       }

       @Override
       public WordViewHolder onCreateViewHolder(ViewGroup parent, int viewType) {
           View mItemView = mInflater.inflate(R.layout.wordlist_item, parent, false);
           return new WordViewHolder(mItemView, this);
       }

       @Override
       public void onBindViewHolder(WordViewHolder holder, int position) {
           String mCurrent = mWordList.get(position);
           holder.wordItemView.setText(mCurrent);
       }

       @Override
       public int getItemCount() {
           return mWordList.size();
       }
   }
   ```

5. **Create a ViewHolder**: 
   Extend `RecyclerView.ViewHolder` to handle each individual list item.

   ```java
   class WordViewHolder extends RecyclerView.ViewHolder implements View.OnClickListener {
       public final TextView wordItemView;
       final WordListAdapter mAdapter;

       public WordViewHolder(View itemView, WordListAdapter adapter) {
           super(itemView);
           wordItemView = itemView.findViewById(R.id.word);
           this.mAdapter = adapter;
           itemView.setOnClickListener(this);
       }

       @Override
       public void onClick(View v) {
           wordItemView.setText("Clicked! " + wordItemView.getText());
       }
   }
   ```

6. **Initialize RecyclerView in the Activity**: 
   In your activity's `onCreate()` method, initialize the RecyclerView, Adapter, and LayoutManager.

   ```java
   private RecyclerView mRecyclerView;
   private WordListAdapter mAdapter;

   @Override
   protected void onCreate(Bundle savedInstanceState) {
       super.onCreate(savedInstanceState);
       setContentView(R.layout.activity_main);

       mRecyclerView = findViewById(R.id.recyclerview);
       mAdapter = new WordListAdapter(this, mWordList);
       mRecyclerView.setAdapter(mAdapter);
       mRecyclerView.setLayoutManager(new LinearLayoutManager(this));
   }
   ```

---

## 3. Related practical
The practical implementation of this concept can be found in 4.5: RecyclerView.

---

## 4. Learn more
For more in-depth understanding and references, visit:
- [RecyclerView Documentation](https://developer.android.com/guide/topics/ui/layout/recyclerview)
- [Android Developer: LayoutManager](https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView.LayoutManager)
- [ViewHolder Pattern](https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView.ViewHolder)

RecyclerView provides an efficient way to display large datasets by caching and reusing views, ensuring optimal performance.
