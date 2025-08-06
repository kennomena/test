# Quick ComfyUI Video Optimization Steps

## 🚀 Immediate Actions (Apply Now for 2-3x Speed Boost)

### 1. Change Sampler Settings
In your KSampler node:
- **Steps**: Change to `15` (from 25-50)
- **CFG Scale**: Change to `7.0` (from 10-15) 
- **Sampler**: Select `dpmpp_2m_karras`
- **Scheduler**: Select `karras`

### 2. Adjust Resolution 
In your video generation nodes:
- **Width**: `768` (instead of 1024+)
- **Height**: `768` (instead of 1024+)
- You can upscale later if needed

### 3. Extend Video Length
In your AnimateDiff/Video node:
- **Frame Count**: Change to `72` (from 24) = 6 seconds at 12fps
- **Context Length**: Set to `16` 
- **FPS**: Keep at `12` or `8` for longer videos

## 🔧 Advanced Optimizations (For Even Better Results)

### 4. Model Selection
Consider switching to faster models:
- **Current**: SDXL models
- **Faster Option**: SD 1.5 + AnimateDiff
- **Fastest Option**: LCM or SDXL-Turbo models

### 5. Memory Management
Add these settings if available:
- Enable **Model CPU Offload**
- Use **FP16 Precision** 
- Enable **Tiled VAE** for large videos

### 6. For Much Longer Videos (15-30 seconds)
- **Frame Count**: `144-360` frames
- **Batch Processing**: Generate in segments
- **Use SVD**: Stable Video Diffusion for native longer generation

## 📊 Expected Results

| Setting | Before | After | Improvement |
|---------|--------|-------|-------------|
| **Speed** | Slow generation | 2-3x faster | 40-60% time reduction |
| **Length** | 5 seconds (24 frames) | 6-15 seconds (72-180 frames) | 3-6x longer |
| **Quality** | High | Maintained | Same or better |
| **VRAM** | High usage | Reduced | 30-50% less memory |

## 🎯 Priority Order

1. **First**: Change sampler to 15 steps, CFG 7, DPM++ 2M Karras
2. **Second**: Increase frame count to 72
3. **Third**: Optimize resolution (768x768)
4. **Fourth**: Consider faster model alternatives
5. **Fifth**: Enable advanced memory optimizations

## ⚡ Emergency Speed Mode

For extremely fast testing:
- **Steps**: `8-10`
- **CFG**: `5-6`
- **Resolution**: `512x512`
- **Frames**: `48` (4 seconds)
- **Model**: LCM or Turbo variants

This will generate in under 2 minutes instead of 10+ minutes!

## 🎬 For Professional Results

Balance speed and quality:
- **Steps**: `20`
- **CFG**: `8`
- **Resolution**: `768x768`
- **Frames**: `120` (10 seconds at 12fps)
- **Upscale**: Separate step if needed

## Troubleshooting

**If still slow:**
- Check VRAM usage (should be under 12GB)
- Close other applications
- Use CPU offload for models
- Generate shorter segments and combine

**If quality drops:**
- Increase steps to 20
- Use CFG 8-9
- Keep higher resolution
- Use better base models

Apply these changes one at a time to see the impact on your specific setup!