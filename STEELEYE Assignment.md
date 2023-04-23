# VISHAL-GUPTA_FRONTEND
STEELEYE Assignment

-> The List component is a React component that displays a list of items as an unordered list. Each item in the list can be selected by clicking on it. When an item is
   selected, its background color changes to green, and when it is deselected, it changes back to red.

# There are a few problems/warnings with the code:

1. The prop type for the items prop in the WrappedListComponent is incorrect. Instead of PropTypes.array(PropTypes.shapeOf({ text: PropTypes.string.isRequired })), 
   it should be PropTypes.arrayOf(PropTypes.shape({ text: PropTypes.string.isRequired })).

2. The setSelectedIndex function in the WrappedListComponent is incorrectly defined. It should be const [selectedIndex, setSelectedIndex] = useState(null);.

3. The isSelected prop in the WrappedSingleListItem is not being used correctly. It should be isSelected === index instead of isSelected.

4. The onClickHandler prop in the WrappedSingleListItem is not being used correctly. It should be () => onClickHandler(index) instead of onClickHandler(index).


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------


# In this modified code, the following changes were made:

1. The WrappedSingleListItem component was removed and replaced with the SingleListItem component. The unnecessary memo wrapper was removed, and 
   the PropTypes were updated.

2. The isSelected prop in the SingleListItem component was fixed so that it checks whether isSelected is equal to the index prop.

3. The onClickHandler prop in the SingleListItem component was fixed so that it uses an arrow function.

4. The WrappedListComponent component was removed and replaced with the List component. The unnecessary memo wrapper was removed, and the PropTypes were updated.

5. The setSelectedIndex and selectedIndex variables in the List component were swapped so that selectedIndex is defined first.

6. The handleClick function in the List component was updated to use the new selectedIndex state variable.

7. A check was added to the items prop in the List component to make sure it exists before trying to map over it.

8. A key prop was added to the SingleListItem component
