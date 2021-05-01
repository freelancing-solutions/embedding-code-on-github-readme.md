### How to embed code on github profile readme.md using Markdown Syntax

### FENCED CODE BLOCKS
    Markdown coverts text with four leading spaces into a code block; with GFM you can
    wrap your code with ``` to create a code block without the leading spaces. Add an
    optional language identifier and your code will get syntax highlighting.
    
```python
    @ndb.tasklet
    def can_add_member(self, uid: str, plan_id: str, start_date: date) -> any:
        user_valid: typing.Union[None, bool] = yield self.is_user_valid(uid=uid)
        plan_exist: typing.Union[None, bool] = yield self.plan_exist(plan_id=plan_id)
        date_valid: typing.Union[None, bool] = yield self.start_date_valid(start_date=start_date)

        if isinstance(user_valid, bool) and isinstance(plan_exist, bool) and isinstance(date_valid, bool):
            return user_valid and plan_exist and date_valid
        message: str = "Unable to verify input data, due to database error, please try again later"
        raise DataServiceError(message)
```

#### Conclusion 
    Using this method you can basically add any repository code without any problems.
