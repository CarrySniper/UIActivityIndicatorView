# UIActivityIndicatorView

百度经验：http://jingyan.baidu.com/article/f7ff0bfc27c73b2e26bb13ba.html
##代码
```
#import "ViewController.h"

@interface ViewController ()

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
    
    //1.初始化
    UIActivityIndicatorView *aiv = [[UIActivityIndicatorView alloc] init];
    //2.设置位置，中心为self.view的中心。可以不设置frame，因为宽高是系统限制的。
    aiv.center = self.view.center;
    //3.添加到self.view上
    [self.view addSubview:aiv];
    
    
    //设置风格
    /**
     *  UIActivityIndicatorViewStyleWhiteLarge      白、大号
     *  UIActivityIndicatorViewStyleWhite           白
     *  UIActivityIndicatorViewStyleGray            灰
     */
    aiv.activityIndicatorViewStyle = UIActivityIndicatorViewStyleWhiteLarge;
    //设置颜色
    aiv.color = [UIColor redColor];
    //设置停止时是否隐藏
    aiv.hidesWhenStopped = YES;
    
    [aiv startAnimating];//开始动画
//    [aiv stopAnimating];//停止动画
    
    //获取指示器动画状态
    [aiv isAnimating];
    
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
}

@end

```
