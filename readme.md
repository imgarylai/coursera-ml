# submit issues

if octave > 4.0.0

replace
```
str=[str str0(pos0(i)+1:pos(i)-1) sprintf('_0x%X_',str0(pos(i)))];
```
by
```
str=[str str0(pos0(i)+1:pos(i)-1) sprintf('_0x%X_',toascii(str0(pos(i))))];
```
and replace
```
str=sprintf('x0x%X_%s',char(str(1)),str(2:end));
```
```
str=sprintf('x0x%X_%s',toascii(str(1)),str(2:end));
```
[ref](https://learner.coursera.help/hc/en-us/community/posts/204693179-linear-regression-submit-error)
