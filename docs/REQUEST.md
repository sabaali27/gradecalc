# Request from the Head of Studies

> **From:** Head of Studies, Department of Computer Science
> **To:** Development team
>
> Students keep emailing us to ask what their final grade will be. Could we
> have a small web service where you enter the assessment components of a
> course and get the final score and letter grade, following our grading
> policy?
>
> It has to be correct — final grades are legally binding.

## Grading policy (notes from the study office)

- Each assessment component has a weight in percent.
- Letter grades: A 89–100, B 77–88, C 65–76, D 53–64, E 41–52, F 0–40.
- Late work loses 10 points per day.
- Some components, such as the exam, are mandatory.
- Work that is not handed in gets no points.

## Integration contract (from the student-records team — do not change)

Other systems will call this code, so the public API is fixed:

```python
from gradecalc.models import Component, CourseResult
from gradecalc.grades import course_result

Component(name: str, weight: float, score: float | None,
          days_late: int = 0, mandatory: bool = False)
CourseResult(total: int, letter: str)

course_result(components: list[Component]) -> CourseResult
```
