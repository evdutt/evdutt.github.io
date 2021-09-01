This post will probably be old news to seasoned modellers, but it's worth repeating even for those of us who have been burned before when creating such models.

For the love of all that is good in this world, get your data sources perfected before embarking on a prescriptive model.

There are four types of model:
1) Descriptive: what happened?
2) Diagnostic: why did it happen?
3) Predictive: what is going to happen?
4) Prescriptive: what should we do?

They are in that order for a reason. If your company's data is not yet reliable enough to do descriptive modelling, **do not** skip ahead to prescriptive modelling. If you do so, you will be in for a world of hurt when your model has erratic behavior and fails to produce any insights of value. Prescriptive models are the most dangerous for two reasons: first, they are designed to run downhill as fast as possible. If your data has errors which the model takes at face value as accurate, it will absolutely exploit those errors to optimize its objective function. And then it will tell you to do something that you probably should not do.

Predictive modelling is a bit less dangerous, though it can still absolutely eat your lunch if you rely on these predictions for big decisions.

Diagnostic modelling is again a bit less dangerous, and here you start to get clues that your underlying data is wrong. You may have a business sense for why something happened, and if your model says otherwise, this may start to raise some alarm bells.

Descriptive modelling is where you're most likely to notice data errors - which is exactly what you want to do. You want to see things that don't look right, and go fix them at the source, be they a collection or a calcultion error.

What you absolutely do not want to do is feed a black box model (most predictive and prescriptive models) bad data, because those models will obscure and run away with that bad data for weeks, months, or years until something terrible happens. Even worse if you're ensembling predictive and prescriptive models, for example by predicting costs and then optimizing to reduce them.

Check your data using statistical methods for outliers and other oddities or weird distributions. Check your data for missing values. Check it for numbers that are too round, or that have non-randomness when you expect randomness, or values that occur more frequently than you'd expect. Plot your data. Play with it first. Describe what happened. Then work your way up the chain of model maturity.

*Consult with subject matter experts - they have spent years honing their guts!*

In summary, garbage in, garbage out (GIGO). Be wary.
