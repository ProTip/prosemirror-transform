This module defines a way to transform documents. Transforming happens
in `Step`s, which are atomic, well-defined modifications to a
document. [Applying](#transform.Step.apply) a step produces a new
document.

Each step provides a [position map](#transform.PosMap) that maps
positions in the old document to position in the transformed document.
Steps can be [inverted](#transform.Step.invert) to create a step that
undoes their effect, and chained together in a convenience object
called a `Transform`.

This module does not depend on the browser API being available (i.e.
you can load it into any JavaScript environment).

You can read more about transformations in
[this guide](guide/transform.md).

### Steps

@Step
@StepResult
@ReplaceStep
@ReplaceAroundStep
@AddMarkStep
@RemoveMarkStep

### Position Mapping

@Mappable
@MapResult
@PosMap
@Mapping

### Transform Helpers

@Transform
@replaceStep
@liftTarget
@findWrapping
@canSplit
@joinable
@joinPoint
@insertPoint