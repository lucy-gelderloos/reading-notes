# Class 28 - RecyclerView

RecyclerView is the name of a class and a library, which allow you to define repeating parts of your interface and have them dynamically generated as they appear on the screen.

Key classes:

- `RecyclerView` (add it to the layout like any other UI element)
- `ViewHolder` is created without any data; RecyclerView binds it to data after it's created
- Methods for calling and binding that data are found in the `Adapter`

To use the RecyclerView, first decide what your recycled items are going to look like, then define the Adapter that links the views with the data. Layouts can be arranged using the LayoutManager class, with options including linear, grid, and staggered grid.

A simple example: 

```java
public class CustomAdapter extends RecyclerView.Adapter<CustomAdapter.ViewHolder> {

    private String[] localDataSet;

    //
    //Provide a reference to the type of views that you are using
    //(custom ViewHolder).
    //
    public static class ViewHolder extends RecyclerView.ViewHolder {
        private final TextView textView;

        public ViewHolder(View view) {
            super(view);
            // Define click listener for the ViewHolder's View

            textView = (TextView) view.findViewById(R.id.textView);
        }

        public TextView getTextView() {
            return textView;
        }
    }

    //
    //Initialize the dataset of the Adapter.
    //
    //@param dataSet String[] containing the data to populate views to be used
    //by RecyclerView.
    //
    public CustomAdapter(String[] dataSet) {
        localDataSet = dataSet;
    }

    // Create new views (invoked by the layout manager)
    @Override
    public ViewHolder onCreateViewHolder(ViewGroup viewGroup, int viewType) {
        // Create a new view, which defines the UI of the list item
        View view = LayoutInflater.from(viewGroup.getContext())
                .inflate(R.layout.text_row_item, viewGroup, false);

        return new ViewHolder(view);
    }

    // Replace the contents of a view (invoked by the layout manager)
    @Override
    public void onBindViewHolder(ViewHolder viewHolder, final int position) {

        // Get element from your dataset at this position and replace the
        // contents of the view with that element
        viewHolder.getTextView().setText(localDataSet[position]);
    }

    // Return the size of your dataset (invoked by the layout manager)
    @Override
    public int getItemCount() {
        return localDataSet.length;
    }
}
```

## Things I'd like to know more about

What different layouts are best suited for.
