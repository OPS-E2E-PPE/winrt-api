---
-api-id: P:Windows.AI.MachineLearning.Preview.LearningModelDescriptionPreview.InputFeatures
-api-type: winrt property
---

<!-- Property syntax.
public IIterable<ILearningModelVariableDescriptorPreview> InputFeatures { get; }
-->

# Windows.AI.MachineLearning.Preview.LearningModelDescriptionPreview.InputFeatures

## -description
Gets the input descriptions for the model.

## -property-value
The input descriptions for the model, keyed by name of input. 

## -remarks

## -see-also

## -examples
 ```csharp
public void Evaluator()
{
    var modelFile = await Windows.ApplicationModel.Package.Current.InstalledLocation.GetFileAsync("model.onnx");
    LearningModelPreview model = await LearningModelPreview.LoadModelFromStorageFileAsync(modelFile);
	
	// Retrieve the first input feature which is an image
    ILearningModelVariableDescriptorPreview inputImageFeatureDescription = model.Description.InputFeatures.First(feature=>feature.ModelFeatureKind == LearningModelFeatureKindPreview.Image);
 
 }
```

