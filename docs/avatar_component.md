# Avatar Component

**Description**: DDS Avatar components are used to represent users and accounts, displaying the profile picture, initials, or fallback icon given the data provided.

**Use Cases**: These components are used to represent users and accounts in the Drift system.

**Props**:
- `size` (x-large | large | medium | small | x-small): The DDS-specific size of the avatar.
- `name` (string): Name of the user to use either as a fallback or as a tooltip/aria-label.
- `imageUrl` (string): The specific image to render inside of the avatar.
- `status` (available | away | chat-limit): Visual status of the avatar used to attach StatusIndicators to the component.
- `rootProps` (React.HTMLAttributes<HTMLSpanElement>): An object that accepts any props that go directly on the parent div element.

**Notes**:
- These components should be used in combination with ComponentX for optimal results.
- They support custom styling via CSS classes or theming.

**Dependencies**:
- No external libraries or dependencies are used by these components.

**Styling and Customization**:
- You can customize and style the components using CSS classes or theming.

**Testing and Quality Assurance**:
- The components are thoroughly tested and maintained for quality assurance.

**Performance Considerations**:
- The components are optimized for performance.

**User Feedback and Common Issues**:
- No common issues or user feedback reported.

**React Code Example Usage**:
```jsx
import { UserAvatar, Flex } from '@driftt/dds';

const UserAvatarDemo = () => (
  <Flex alignItems="flex-end">
    <UserAvatar size="x-large" />
    <UserAvatar size="large" name="Jerry Smith" />
    <UserAvatar size="medium" />
    <UserAvatar size="small" name="Rick Sanchez" />
    <UserAvatar size="x-small" />
  </Flex>
);
```
Another example:
```jsx
import { AccountAvatar, Flex } from '@driftt/dds';

const AccountAvatarDemo = () => (
  <Flex alignItems="flex-end">
    <AccountAvatar />
    <AccountAvatar name="Rando Dude" />
    <AccountAvatar
      imageUrl="https://media.giphy.com/media/ekwEeLxb7G4DW44YaK/giphy.gif"
      name="Rando Dude"
    />
  </Flex>
);

```