# Awesome-AI-Video-Enhancement

# Top AI Video Enhancement Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Super-Resolution, Restoration & Frame Interpolation*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **AI Video Enhancement**. These tools enable creators, archivists, and enterprises to upscale, denoise, deblur, and interpolate video—restoring degraded footage and generating plausible detail where pixels are missing.

**Examples** include Topaz Video AI, Runway, CapCut, Descript, Wondershare Filmora, HitPaw, AVCLabs, Remini, Cutout.pro, and Deep-Image.ai (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, temporal consistency, and open model weights—ideal for researchers, video engineers, and developers seeking transparent, vendor-independent enhancement pipelines.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Topaz Video AI](https://www.topazlabs.com/topaz-video-ai)**  
  Desktop application for AI-powered upscaling, denoising, deinterlacing, frame interpolation, stabilization, and SDR-to-HDR conversion. Features model catalog (Proteus, Iris, Nyx, Rhea, Artemis) organized by problem type. Local rendering with optional cloud processing. $59/month subscription. Requires 6 GB VRAM minimum, 8 GB+ recommended .

- **[Runway](https://runwayml.com/)**  
  Cloud-based AI video generation and editing platform. Features upscaling, frame interpolation, inpainting, and generative video models. Web-based with API access.

- **[CapCut](https://www.capcut.com/)**  
  Free video editor with AI enhancement tools including upscaling, background removal, and motion tracking. Mobile and desktop apps with cloud sync.

- **[Descript](https://www.descript.com/)**  
  AI-powered video and podcast editor with Studio Sound audio enhancement and video upscaling. Text-based editing workflow for efficient content production.

- **[Wondershare Filmora](https://filmora.wondershare.com/)**  
  Consumer video editor with AI upscaling, denoising, and motion tracking. Windows and macOS with paid subscription.

- **[HitPaw](https://www.hitpaw.com/)**  
  AI video enhancer with upscaling, denoising, and colorization. Desktop application with batch processing.

- **[AVCLabs](https://www.avclabs.com/)**  
  Desktop AI video enhancement with upscaling, denoising, face enhancement, colorization, interpolation, and SDR-to-HDR. Detail Balance control to pull processing back toward source. Batch queues for local processing .

- **[Remini](https://remini.ai/)**  
  Mobile app for photo and video enhancement. Over 100 million photos revitalized. Uses deep learning for face restoration, sharpening, and upscaling. Subscription-based with weekly/yearly plans .

- **[Cutout.pro](https://www.cutout.pro/)**  
  AI visual design platform with video enhancement, background removal, and upscaling. API access available.

- **[Deep-Image.ai](https://deep-image.ai/)**  
  AI image and video enhancement platform with upscaling, denoising, and sharpening. API-first architecture.

## Open-Source GitHub Projects

- **[SeedVR2](https://github.com/ByteDance-Seed/SeedVR2)**  
  Diffusion transformer model (Apache-2.0) from ByteDance research team for video restoration in a single inference step. Features adaptive window attention that dynamically adjusts to output resolution rather than fixed window size. Requires ComfyUI, model weight management, and VRAM allocation. Batch size ≥5 needed for temporal consistency—lower batch sizes produce visible flicker. **The model behind many commercial upscalers** .

- **[RVR (Real-time Video Restoration)](https://github.com/Holiday/RVR)**  
  One-step generative streaming real-time video restoration (Apache-2.0). **First generative VR model to reach real-time 1080p streaming on consumer GPU** — ≈26 FPS on RTX 5090, 31 FPS at QHD, 14 FPS at 4K on single H100 . Features mask-free shifted-window self-attention (1.62× throughput gain over full-attention teacher), Restoration-aware Autoencoder (removes 3D-VAE bottleneck), causal chunk-wise streaming (bounds temporal cost), and kernel-agnostic portability across PyTorch SDPA, FlashAttention-2/3, SageAttention, and xFormers . Built on Wan2.2-TI2V-5B backbone.

- **[Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)**  
  Practical algorithms for general image and video restoration (BSD-3-Clause). 36,472 GitHub stars. Ships portable executables for Windows, Linux, and macOS running on Intel, AMD, and NVIDIA GPUs via ncnn-Vulkan . **AnimeVideo-v3** is the video-specific model tuned for anime content—3× faster than Real-CUGAN at Full HD. **RealESRGAN_x4plus_anime_6B** for compact anime-image upscaling. Python inference supports tiling for low-VRAM GPUs .

- **[video2x](https://github.com/k4yt3x/video2x)**  
  Machine-learning video super-resolution and frame interpolation framework (AGPL-3.0). 20,913 GitHub stars. **Full pipeline**: extract frames → upscale → interpolate → reassemble with audio. Supports Real-ESRGAN, Real-CUGAN, RIFE, Anime4K v4, and custom MPV-compatible GLSL shaders. Qt6 GUI and Windows installer. Requires Vulkan GPU (works on Intel, AMD, NVIDIA) .

- **[BasicSR](https://github.com/XPixelGroup/BasicSR)**  
  Open-source image and video restoration toolbox (Apache-2.0). 8k GitHub stars. Includes EDSR, RCAN, SRResNet, SRGAN, ESRGAN, EDVR, BasicVSR, SwinIR, ECBSR, StyleGAN2, and DFDNet . The foundation for many ESRGAN derivatives.

- **[LTX2.3-ICEdit-Insight](https://github.com/Valiant-Cat/LTX2-ICEdit-Insight)**  
  Task-aware video restoration and editing model family built on LTX-2.3 DiT-based audio-video foundation model. Four practical routes: **Video Restoration** (degradation recovery, compression cleanup), **Video HD Enhancement** (super-resolution, detail reconstruction), **Watermark Removal** (logo cleanup, occlusion-aware background reconstruction), **Subtitle Removal** (hard subtitle removal with temporally stable inpainting). Operates in latent video space preserving global structure, camera motion, object identity, and temporal consistency. Uses TADA (Task-Aware Decoupled Adapter), FGLC (Flow-Guided Latent Consistency), and PMTR (Progressive Multi-Task Routing) .

- **[vsrvrt](https://pypi.org/project/vsrvrt/)**  
  VapourSynth plugin for RVRT (Recurrent Video Restoration Transformer) (open-source). Features **Deblur** (gopro, dvd models), **SuperRes** (reds, vimeo_bi, vimeo_bd models, 4x scale), and **Denoise** with chunked processing. Tiling controls for memory management—HxW=256×256 ideal, temporal windows 16-64 safe. Super-resolution is extremely memory-hungry: expect poor quality below 16 GB VRAM .

- **[local-upscaler](https://pypi.org/project/local-upscaler/)**  
  Offline frame-by-frame upscaling tool (open-source). Split → upscale each frame → re-encode + mux audio. Features `--fps` for motion-interpolated frames (smoother motion, same duration, audio in sync), `--scale`, `--sharpen`, `--deblur` (NAFNet), `--face` (GFPGAN face restore), and batch folder processing. **Warning: frames upscaled independently can shimmer between frames**—temporal model needed to fully remove that .

- **[video-super-resolution](https://github.com/Alhamwis/video-super-resolution)**  
  PyTorch-based video enhancement using ESRGAN, Real-ESRGAN, and SRCNN (open-source). Multiple scale factors (2x, 3x, 4x). Side-by-side comparison tool for different enhancement methods. Note: simplified PyTorch implementation may not achieve full quality .

- **[Free AI Video Upscaler](https://github.com/sbhattacharyya/free-ai-video-upscaler)**  
  Browser-based client-side video upscaling using WebGPU + WebCodecs. 250,000 monthly active users with zero server cost. Uses WebSR SDK with Anime4K CNN models. Pipeline: demux → decode → process → encode → mux via Streams API .

### Additional Strong Open-Source Options

- **[RIFE](https://github.com/hzwer/ECCV2022-RIFE)** — Real-time intermediate flow estimation for frame interpolation (MIT). Integrated into video2x.
- **[waifu2x](https://github.com/nihui/waifu2x-ncnn-vulkan)** — Popular anime upscaling tool (MIT) with ncnn-Vulkan backend.
- **[Real-CUGAN](https://github.com/bilibili/ailab)** — Bilibili's anime-tuned upscaler (MIT). Slower than Real-ESRGAN AnimeVideo-v3 at Full HD .
- **[Anime4K](https://github.com/bloc97/Anime4K)** — Real-time anime upscaling (MIT). GLSL shaders for MPV, MPC-HC, and other players.
- **[GFPGAN](https://github.com/TencentARC/GFPGAN)** — Face restoration for post-upscaling enhancement (Apache-2.0).
- **[CodeFormer](https://github.com/sczhou/CodeFormer)** — Transformer-based face restoration (NTU S-Lab License).
- Community **n8n** workflows for batch video enhancement pipelines and quality gating.

**Frameworks for building custom systems**: Combine **SeedVR2** or **RVR** as the temporal-consistent restoration engine with **Real-ESRGAN** for frame-level super-resolution, **video2x** for full pipeline orchestration, **vsrvrt** for VapourSynth-based processing, and **FFmpeg** for muxing/demuxing—creating a fully self-hosted, enterprise-grade video enhancement platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- AI video enhancement tools processing footage must comply with copyright and content licensing requirements.
- **Frame-by-frame upscaling can cause temporal shimmer.** Independent frame processing introduces flicker that temporal models (SeedVR2, RVR, RVRT) are designed to eliminate. For production work, prioritize temporal consistency over single-frame sharpness .
- **Temporal consistency requires batch processing.** SeedVR2 needs batch size ≥5 (ideally more) to maintain motion coherence. Lower batch sizes produce visible flicker .
- **Open-source assumes VRAM to spare.** Frame-by-frame inference on long clips occupies consumer GPUs for hours. Low-VRAM cards force tiling that slows processing further. The "free" route is the most expensive in hours if hardware or Python tolerance is missing .
- **Licenses point different directions.** video2x is AGPL-3.0 (obligations if embedded in a service you sell); Real-ESRGAN is BSD-3-Clause (permissive). Check the LICENSE file, not the marketing page .
- **Enhancement generates plausible detail, not recovered truth.** Modern models reconstruct convincing textures and scenery but can drift on faces and text at aggressive scale factors. A 2× pass is the safer default than 4× on important footage .

---

**Made for video editors, archivists, content creators, and developers building transparent video enhancement solutions.**  
Let's make AI Video Enhancement more open, data-driven, and temporally consistent.
