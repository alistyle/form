# form

---

通用表单样式。可基于此表单样式构建各类功能表单。

---

## 演示

> 演示中还引用了 [alistyle/button](https://github.com/alistyle/button) 和 [alistyle/tiptext](https://github.com/alistyle/tiptext) 。

<link type="text/css" rel="stylesheet" media="screen" href="src/form.css">

### 基本用法

````html
<form class="ali-form" name="" method="post" action="" id="">
    <fieldset>
        <legend>表单标题</legend>

        <div class="ali-form-item ali-form-item-error">
            <label for="" class="ali-label">表单项文本</label>
            <div class="ali-form-text">一个个文字文字</div>
        </div>

        <div class="ali-form-item">
            <label for="" class="ali-label">
                <span class="ali-form-required">*</span>表单项文本
            </label>
            <input class="ali-input" type="text"> <span class="ali-form-other"><a href="#">添加备注</a></span>
            <div class="ali-form-explain">默认文案。</div>
        </div>

        <div class="ali-form-item ali-form-item-error">
            <label for="" class="ali-label">表单项文本</label>
            <input class="ali-input ali-input-large" type="text"> <span class="ali-form-other"><a href="#">表单项其他</a></span>
            <div class="ali-form-explain ali-tiptext ali-tiptext-error">
                <i class="ali-tiptext-icon iconfont" title="出错">&#xF045;</i>
                此在DOM上保存属性值，请使用data-xxx的形式。
            </div>
        </div>

        <div class="ali-form-item ali-form-item-error">
            <label for="" class="ali-label">表单项文本</label>
            <input class="ali-input" type="text"> <span class="ali-form-other"><a href="#">表单项其他</a></span>
            <div class="ali-form-explain ali-tiptext ali-tiptext-error">
                <i class="ali-tiptext-icon iconfont" title="出错">&#xF045;</i>
                ali-form-item-focus 的效果。
            </div>
        </div>

        <div class="ali-form-item ali-form-item-success">
            <label for="" class="ali-label">表单项文本</label>
            <textarea class="ali-textarea">一二三四五六七八九十</textarea>
            <div class="ali-form-explain ali-tiptext ali-tiptext-success">
                <i class="ali-tiptext-icon iconfont" title="成功">&#xF049;</i>
                成功文案。
            </div>
        </div>

        <div class="ali-form-item">
            <label for="" class="ali-label">下拉选择</label>
            <select id="province" name="province">
                <option value="">
                请选择
                </option>
                <option value="北京">
                北京
                </option>
                <option value="上海">
                上海
                </option>
                <option value="天津">
                天津
                </option>
                <option value="浙江">
                浙江
                </option>
            </select>
            <div class="ali-form-explain">更多地区即将开通，敬请期待。</div>
        </div>

        <div class="ali-form-item">
            <label for="" class="ali-label ali-label-reset">不可用input</label>
            <input class="ali-input ali-input-disable" type="text" disabled>
            <div class="ali-form-explain">目前不可用</div>
        </div>

        <div class="ali-form-item">
            <label for="" class="ali-label">验证码</label>
            <input class="ali-input ali-input-checkcode" type="text" data-explain="请输入右图中字符，不区分大小写。" maxlength="4" autocomplete="off" value="" name="fourcode">
            <img class="ali-checkcode-imgcode-img" align="absMiddle" alt="请输入您看到的内容" src="https://omeo.alipay.com/service/checkcode?sessionID=82012ab6b1f4ed9e675fb9092a25cb3b&r=0.9321065918075809"  title="点击刷新图片校验码">
            <a href="#">看不清，换一张</a>
            <div class="ali-form-explain">请输入右图中字符，不区分大小写。</div>
        </div>

        <div class="ali-form-item">
            <label for="test">
                <input class="ali-checkbox" id="test" value="" type="checkbox">
                我已阅读并接受自主缴费服务协议
            </label>
        </div>

        <div class="ali-form-item">
            <input type="submit" class="ali-button ali-button-morange" value="确定">
            <input type="button" class="ali-button ali-button-mwhite" value="取消">
        </div>
    </fieldset>
</form>
````

和 arale/validator 配合使用：http://aralejs.org/validator/examples/with-alice-form.html