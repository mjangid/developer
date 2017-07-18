---
author: mijacobs
description:
title: Ratings Control
template: detail.hbs
pm-contact: abarlow
design-contact: kimsea
dev-contact: mitra
doc-status: Published
---

# Ratings control

> [!IMPORTANT]
> This article describes functionality that hasn’t been released yet and may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

Allowing users to easily view and set ratings that reflect degrees of satisfaction with content and services is a critical app scenario.  The ratings control allows your users to do this with touch, pen, mouse, gamepad and keyboard. Use the ratings control to let your users rate movies, music and books with high quality interaction and animation. The ratings control has several great features that provide flexibility and customization.

> **Important APIs**: [RatingsControl class](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.ratingscontrol)

![Example of Ratings Control](images/rating_rs2_doc_ratings_intro.png)

In this article, we describe some key scenarios that the ratings control supports. Each scenario includes an example to provide context, and code that shows how to achieve the scenario.

### Editable rating with placeholder value

Perhaps the most common way to use the ratings control is to display an average rating while still allowing the user to enter their own rating value. In this scenario, the ratings control is initially set to reflect the average satisfaction rating of all users of a particular service or type of content (such as a music, videos, books, etc.). It remains in this state until a user interacts with the control with the goal of individually rating an item. This interaction changes the state of the ratings control to reflect the user's personal satisfaction rating.

#### Initial average rating state
![Initial Average Rating State](images/rating_rs2_doc_movie_aggregate.png)

#### Representation of user rating once set

![Representation of User Rating Once Set](images/rating_rs2_doc_movie_user.png)

```XAML
<RatingsControl x:Name="MyRatings" ValueChanged="RatingChanged"/>
```

```csharp
private void RatingChanged(RatingsControl sender, object args)
{
    if (sender.Value == null)
    {
        MyRatings.Caption = "(" + SomeWebService.HowManyPreviousRatings() + ")";
    }

    else
    {
        MyRatings.Caption = "Your rating";
    }
}
```

### Read-only rating mode

Sometimes you need to show ratings of secondary content, such as that displayed in recommended content or when displaying a list of comments and their corresponding ratings. In this case, the user shouldn’t be able to edit the rating, so you can make the control read-only.
The read only mode is also the recommended way of using the ratings control when it is used in very large virtualized lists of content, for both UI design and performance reasons.


![Read-Only Long List](images/rating_rs2_doc_reviews.png)

To do this you would do the following:

```XAML
<RatingsControl IsReadOnly="True"/>
```

## Additional functionality

The ratings control has many additional features which can be used. Details for using these features can be found in our MSDN reference documentation.
Here is a non-comprehensive list of additional functionality:
-   Great long list performance
-   Compact sizing for tight UI scenarios
-   Continuous value fill and rating
-   Spacing customization
-   Disable growth animations
-   Customization of the number of stars
