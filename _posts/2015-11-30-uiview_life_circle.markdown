---
layout: post
title:  "UIView Life Circle"
date:   2015-11-30 11:01:22
categories: objc
---
{% highlight objc %}
- (instancetype)initWithCoder:(NSCoder *)aDecoder {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    if (self = [super initWithCoder:aDecoder]) {

    }
    return self;
}

- (void)willMoveToSuperview:(UIView *)newSuperview {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super willMoveToSuperview:newSuperview];
}

- (void)invalidateIntrinsicContentSize {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super invalidateIntrinsicContentSize];
}

- (void)didMoveToSuperview {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super didMoveToSuperview];
}

- (void)awakeFromNib {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    NSLog(@"lineWidth: %f", self.lineWidth);
    [super awakeFromNib];
}

- (void)willMoveToWindow:(UIWindow *)newWindow {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super willMoveToWindow:newWindow];
}

- (BOOL)needsUpdateConstraints {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    return [super needsUpdateConstraints];
}

- (void)didMoveToWindow {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super didMoveToWindow];
}

- (void)setNeedsLayout {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super setNeedsLayout];
}

- (void)updateConstraints {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super updateConstraints];
}

- (void)layoutSubviews {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super layoutSubviews];
}

- (void)drawRect:(CGRect)rect {
    NSLog(@"%s", __PRETTY_FUNCTION__);
    [super drawRect:rect];
}
{% endhighlight %}