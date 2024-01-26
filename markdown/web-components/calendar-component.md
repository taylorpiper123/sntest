
# Calendar Component

The calendar component offers a user-friendly interface for date selection and month navigation, ideal for scheduling, booking, and event marking.

---

  
![calendar component](https://studio-assets.supernova.io/design-systems/19054/85d3c1c7-d255-4c5c-adc3-486c452a8e9a.png)  
calendar component, This is the frame of the component pulled in Supernova.
Developers and designer can click on it and be re-directed to the component inside Figma.  
  


**[Calendar Component](./calendar-component.md)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Health status:&nbsp;&nbsp;&nbsp;**Healthy**

Calendar  
  
  
| Component property | Value |  
| :-- | --: |  
| Is documented | ✅ |  
| Repository | - |  
| Figma component | [Open in Figma](https://www.figma.com/file/VkOZLQ5xv7UZfwKHSTkFFi?node-id=2596:14) |  
| Status | Healthy |

### **Design Properties**

**Dimensions**: Default size of 320px x 240px.

**Primary color**:

  
primary.color: rgb(255, 255, 255)  


### **Interactivity & Behavior**

- **Date Selection**: Users can click to select a date. Clicking and dragging allows range selection.

- **Navigation**: Arrows on either side of the month name allow users to navigate between months.

- **Special Dates**: Dates with a dot below them indicate special events or holidays.

### **Usage Guidelines**

- **Best Practices**: Use PrimeCal for date&hyphen;specific tasks like event scheduling or booking.

- **Do's**:
Ensure ample space around the component for clarity.
Use in conjunction with other date&hyphen;related components for a seamless experience.

- **Don'ts**:
Don't use for non&hyphen;date&hyphen;specific tasks.
Avoid placing too close to page edges or other interactive elements.

### Code implementation

```javascript  
import React, { useState } from 'react';
import Calendar from 'react-calendar';
import 'react-calendar/dist/Calendar.css'

export default function Component() {
  const [value, onChange] = useState(new Date());

  return (
    <div>
      <Calendar onChange={onChange} value={value} />
    </div>
  );
}  
```

```javascript  
import React from 'react';
export default function Button(props) {
 return (
   <button>
     Click me!
   </button>
 );
}  
```