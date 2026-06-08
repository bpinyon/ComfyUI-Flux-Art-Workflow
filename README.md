# Flux ComfyUI Art Workflow

This is a ComfyUI workflow I use to create painterly AI artwork similar to the included example image.

## Included Files

- 'ComfyUI-Flux-Art-Workflow.json'
- 'Example_Output.png'
- 'README.md'

'Example_Output.png' was generated from the included workflow using the default prompt and seed.

## Requirements

- ComfyUI
- Flux model:
  - 'flux1-dev.safetensors'
- VAE:
  - 'ae.safetensors'
- CLIP / text encoders:
  - 't5xxl_fp16.safetensors'
  - 'clip_l.safetensors'

## DualCLIPLoader Settings

- Type: 'flux'
- Device: 'default'

## Custom Nodes

This workflow uses mostly standard ComfyUI nodes.

Known custom node:

- 'SaveImageExtended'
  - Package: 'thedyze/save-image-extended-comfyui'

If this node is missing, install it through ComfyUI Manager or from the custom node repository.

## Workflow Settings

Default image size:

- Width: '1216'
- Height: '832'
- Batch size: '1'

Sampling settings:

- Sampler: 'euler'
- Scheduler: 'simple'
- Steps: '25'
- Denoise: '1.0'
- Flux guidance: '3.5'
- ModelSamplingFlux max shift: '1.15'
- ModelSamplingFlux base shift: '0.5'
- Seed: '694314603778170'

The seed may be changed to create new variations.

## Sample Prompt

A majestic ship battling towering waves beneath a storm-lashed sky, rendered as a dramatic Romantic seascape in oil paint. The sea is depicted with luminous, translucent layers, its surging crests tipped with white foam. Powerful light breaks through turbulent clouds, casting warm golden highlights across the dark water. The scene conveys motion, peril, and awe, with delicate brushwork, atmospheric depth, and rich oil-on-canvas texture.

## How to Use

1. Download 'ComfyUI-Flux-Art-Workflow.json'.
2. Open ComfyUI.
3. Drag the JSON file onto the ComfyUI canvas.
4. Install any missing custom nodes.
5. Confirm the model paths match your local setup.
6. Queue the prompt.

## Notes

Using the same workflow, prompt, and seed should produce a similar or matching result, but exact output may vary depending on ComfyUI version, model files, node versions, GPU, precision settings, sampler behavior, and resolution.

This workflow is shared for learning and experimentation.