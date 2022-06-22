# WNNX Models

wnnx is a new model format which exports models directly from pytorch without onnx. It can be infered via **wnn** framework, the infer lib is also incrediablly simple and insamely small to serveral kbs.

Even though, **wnn** can achieve a extremly fast speed and low memory consumption in both X86 and arm platform.

**wnnx_models** contains some popular models which exports from pytorch. It can be viewed using:

```
pip install wnetron
wnetron .
```

When wnnx merged by `netron` official repo, you can also view *wnnx* model with `netron` as well.


## Results

- `SimpleFC`:

![](https://raw.githubusercontent.com/jinfagang/public_images/master/20220622155647.png)

- `MobilenetV3`:

![](https://raw.githubusercontent.com/jinfagang/public_images/master/20220622155829.png)

- `DynamicLayernorm`:

![](https://raw.githubusercontent.com/jinfagang/public_images/master/20220622160247.png)


As you can see, wnnx can be fully replace onnx as an option to inference model. It has many strength compare with onnx:

- Powered with flatbuffer, instead using protobuf which is heavy;
- Easy to convert from trained model via pytorch;
- Without **any** glu ops, the whole graph is extremly clean;
- Can be efficiently inferenced via **wnn**.


