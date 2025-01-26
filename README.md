# Next.js 15 App Router: Custom Layout issue with Dynamic Routes

This repository demonstrates a bug encountered when using a custom layout with dynamic routes in Next.js 15's App Router.  The issue is that the custom layout does not render correctly for some dynamic routes, possibly due to the way route segments are handled in combination with the new app router. 

## Steps to Reproduce
1. Clone the repository.
2. Install dependencies: `npm install`
3. Start the development server: `npm run dev`
4. Navigate to `/` - The default layout works
5. Navigate to `/blog/[slug]` (e.g., `/blog/my-post`) - layout does not apply.

## Expected Behavior
The custom layout should be applied consistently across all routes, regardless of whether they are dynamic or not.

## Actual Behavior
The custom layout is not applied to dynamic routes (`/blog/[slug]` ).

## Solution
The solution involves ensuring proper loading and handling of dynamic segments within the layout component. The updated `app/layout.js` example demonstrates a possible fix.

## Additional Notes
This bug might be related to the latest developments of the app router, so it's crucial to consult the official documentation and potential updates for resolution.