---
title: "ARM 組み込み | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "arm_neon/vsetq_lane_p8"
  - "armintr/_arm_uxtb"
  - "arm_neon/vld4_lane_p8"
  - "arm_neon/vrshrn_n_s64"
  - "arm_neon/vsli_n_u32"
  - "arm_neon/vsraq_n_u16"
  - "arm_neon/vcgt_f32"
  - "armintr/__iso_volatile_store32"
  - "arm_neon/vceqq_f32"
  - "armintr/_arm_smlal"
  - "arm_neon/vmull_n_s32"
  - "arm_neon/vmax_s8"
  - "arm_neon/vmvn_u32"
  - "arm_neon/vrshl_u32"
  - "arm_neon/int32x2_t"
  - "arm_neon/vdupq_n_p8"
  - "arm_neon/vpmax_u16"
  - "arm_neon/vtrnq_s32"
  - "arm_neon/vset_lane_f32"
  - "arm_neon/vrev64_s8"
  - "arm_neon/vtrnq_p8"
  - "arm_neon/vqshlq_u64"
  - "arm_neon/vld1q_dup_s64"
  - "arm_neon/vmovq_n_u64"
  - "arm_neon/vqshrn_n_u16"
  - "arm_neon/vhadd_s32"
  - "arm_neon/vrhaddq_u32"
  - "arm_neon/vst1q_p8"
  - "arm_neon/vshrn_n_s16"
  - "arm_neon/vget_high_f32"
  - "arm_neon/vuzpq_s16"
  - "arm_neon/vand_u16"
  - "arm_neon/vmulq_s32"
  - "arm_neon/vrsraq_n_s64"
  - "arm_neon/vceqq_s8"
  - "arm_neon/uint64x1x3_t"
  - "arm_neon/veor_u32"
  - "armintr/_arm_pkhtb"
  - "arm_neon/vorrq_u16"
  - "arm_neon/vpaddl_s8"
  - "arm_neon/vmla_n_s16"
  - "arm_neon/vqdmlal_lane_s32"
  - "arm_neon/vshlq_n_u8"
  - "arm_neon/vst2_lane_p8"
  - "arm_neon/vld3q_u16"
  - "arm_neon/vandq_u8"
  - "arm_neon/vst1_u64"
  - "arm_neon/vaddq_s64"
  - "arm_neon/vuzpq_u32"
  - "arm_neon/vld3_lane_p8"
  - "arm_neon/vminq_s32"
  - "arm_neon/vabd_u16"
  - "arm_neon/vdup_n_u32"
  - "arm_neon/vmul_p8"
  - "arm_neon/vsra_n_u16"
  - "arm_neon/vst3q_u16"
  - "arm_neon/int32x2x3_t"
  - "arm_neon/vld2_dup_u16"
  - "arm_neon/vrhaddq_u8"
  - "arm_neon/vhadd_u8"
  - "arm_neon/vgetq_lane_s32"
  - "arm_neon/vcleq_u16"
  - "arm_neon/vabdq_s8"
  - "arm_neon/vrev16q_u8"
  - "arm_neon/vqshlu_n_s64"
  - "arm_neon/vcvt_n_s32_f32"
  - "arm_neon/vqrshrn_n_s64"
  - "arm_neon/vst1q_p16"
  - "arm_neon/vgetq_lane_s16"
  - "arm_neon/vtstq_u32"
  - "arm_neon/vmlsl_n_s16"
  - "arm_neon/vcge_s8"
  - "arm_neon/vshr_n_s16"
  - "armintr/_arm_rbit"
  - "arm_neon/vmls_u32"
  - "arm_neon/vmls_lane_u32"
  - "arm_neon/vcvtq_n_s32_f32"
  - "arm_neon/vqshl_n_s8"
  - "arm_neon/vst1q_s16"
  - "armintr/__emit"
  - "arm_neon/vshlq_s64"
  - "arm_neon/vuzp_s8"
  - "arm_neon/vld1q_lane_s64"
  - "arm_neon/veorq_s32"
  - "arm_neon/vaddq_u64"
  - "arm_neon/vceq_s32"
  - "arm_neon/vmovn_u16"
  - "arm_neon/vabal_s8"
  - "arm_neon/vabsq_f32"
  - "armintr/_arm_smuad"
  - "arm_neon/veor_u8"
  - "arm_neon/int16x4_t"
  - "arm_neon/vsraq_n_s16"
  - "arm_neon/vshlq_s8"
  - "arm_neon/vcreate_u32"
  - "arm_neon/vzipq_s8"
  - "arm_neon/vst3q_u8"
  - "arm_neon/int64x1x4_t"
  - "armintr/__iso_volatile_store16"
  - "arm_neon/vst4_lane_p16"
  - "arm_neon/vld1_dup_p16"
  - "arm_neon/vhadd_s16"
  - "arm_neon/vtbl2_s8"
  - "arm_neon/veorq_u32"
  - "arm_neon/vqdmlal_lane_s16"
  - "arm_neon/vrsra_n_u8"
  - "arm_neon/vbslq_u16"
  - "arm_neon/vget_low_s64"
  - "arm_neon/vceq_u16"
  - "arm_neon/vdupq_lane_u32"
  - "arm_neon/vabdl_u32"
  - "arm_neon/vmlal_s32"
  - "arm_neon/vst1_lane_u8"
  - "arm_neon/vld4q_f16"
  - "arm_neon/vqdmlsl_s32"
  - "arm_neon/vqrdmulh_s32"
  - "arm_neon/vqrshl_u8"
  - "arm_neon/uint32x4x4_t"
  - "arm_neon/vabaq_u16"
  - "arm_neon/vcnt_p8"
  - "arm_neon/vld3q_s16"
  - "arm_neon/vshl_n_u32"
  - "arm_neon/vrev64q_u16"
  - "arm_neon/vextq_s64"
  - "arm_neon/vhsubq_s8"
  - "arm_neon/vld2_dup_u8"
  - "arm_neon/vst3_s16"
  - "arm_neon/vorn_u16"
  - "arm_neon/vst4_f16"
  - "arm_neon/vpadalq_u8"
  - "armintr/__iso_volatile_load8"
  - "arm_neon/vmovl_u16"
  - "arm_neon/vld4q_u32"
  - "arm_neon/vcgt_u32"
  - "arm_neon/vmlaq_n_u32"
  - "arm_neon/vrsra_n_u64"
  - "arm_neon/vst4_s8"
  - "arm_neon/vcvtq_n_f32_u32"
  - "arm_neon/vst2q_u16"
  - "arm_neon/vqshrn_n_s16"
  - "arm_neon/vld4_s16"
  - "arm_neon/uint16x8x4_t"
  - "arm_neon/vrsqrte_u32"
  - "arm_neon/vcltq_s8"
  - "arm_neon/vst3_u16"
  - "arm_neon/vst2_f32"
  - "arm_neon/vld2_u64"
  - "arm_neon/vst1_u16"
  - "arm_neon/vmls_s16"
  - "arm_neon/vqrshlq_s32"
  - "arm_neon/vqdmull_s16"
  - "arm_neon/vld2_lane_p16"
  - "arm_neon/vpaddlq_u8"
  - "arm_neon/vcvt_n_f32_u32"
  - "arm_neon/vcgtq_u8"
  - "arm_neon/vshl_s32"
  - "arm_neon/vtbx3_p8"
  - "arm_neon/vld3_dup_s32"
  - "arm_neon/int16x4x3_t"
  - "arm_neon/vcale_f32"
  - "arm_neon/vqabsq_s32"
  - "arm_neon/vmulq_u16"
  - "arm_neon/vst1_s8"
  - "arm_neon/vclt_u8"
  - "armintr/_arm_sxtb16"
  - "arm_neon/vshr_n_s8"
  - "arm_neon/vst1_lane_f16"
  - "arm_neon/vorn_s64"
  - "armintr/_arm_usub8"
  - "arm_neon/vst4_lane_f32"
  - "arm_neon/vmls_lane_u16"
  - "arm_neon/vpaddl_u32"
  - "arm_neon/vdup_lane_u64"
  - "arm_neon/vsri_n_p16"
  - "arm_neon/vqrshlq_u64"
  - "arm_neon/vclz_s16"
  - "arm_neon/vsra_n_u32"
  - "arm_neon/vabaq_s8"
  - "arm_neon/vst2_lane_s8"
  - "arm_neon/vcvt_n_u32_f32"
  - "arm_neon/vst3_u32"
  - "arm_neon/vcvtq_f32_u32"
  - "arm_neon/vraddhn_s64"
  - "armintr/_arm_uqsax"
  - "arm_neon/vshl_u8"
  - "armintr/_arm_uqadd16"
  - "arm_neon/vrsra_n_u16"
  - "arm_neon/vrshl_u64"
  - "arm_neon/int32x4x3_t"
  - "arm_neon/vmull_u8"
  - "arm_neon/vcombine_u64"
  - "arm_neon/vmull_u16"
  - "arm_neon/vld1_dup_s8"
  - "armintr/_CountLeadingSigns64"
  - "arm_neon/vqshlq_n_s32"
  - "arm_neon/vrecpe_f32"
  - "arm_neon/vsri_n_u32"
  - "arm_neon/vrsraq_n_s8"
  - "arm_neon/vsetq_lane_s16"
  - "arm_neon/vget_high_u32"
  - "arm_neon/vmlal_u32"
  - "arm_neon/vdupq_lane_s16"
  - "arm_neon/vsubq_u64"
  - "arm_neon/vext_p8"
  - "arm_neon/vshl_u16"
  - "arm_neon/vmls_n_u16"
  - "arm_neon/vmull_s16"
  - "arm_neon/vmovq_n_s64"
  - "arm_neon/vaddq_f32"
  - "arm_neon/vshl_n_s16"
  - "arm_neon/vext_p16"
  - "arm_neon/vextq_u32"
  - "arm_neon/vld1_p8"
  - "arm_neon/veor_s32"
  - "arm_neon/int16x8x4_t"
  - "arm_neon/vst1q_u16"
  - "arm_neon/vzipq_p8"
  - "arm_neon/int32x4x4_t"
  - "arm_neon/vqdmulhq_lane_s32"
  - "arm_neon/vst3_lane_u32"
  - "arm_neon/vhsubq_s32"
  - "armintr/__static_assert"
  - "arm_neon/vst3q_lane_u16"
  - "arm_neon/vpmin_u32"
  - "arm_neon/vrev64q_p16"
  - "arm_neon/vcleq_f32"
  - "arm_neon/vhsub_u16"
  - "arm_neon/vld2_lane_s32"
  - "arm_neon/vmlsl_s32"
  - "armintr/_arm_rev"
  - "arm_neon/vcgeq_s16"
  - "arm_neon/vmulq_s8"
  - "arm_neon/vsri_n_s8"
  - "arm_neon/vpadd_f32"
  - "arm_neon/vld1q_lane_f16"
  - "arm_neon/vmls_u16"
  - "arm_neon/vld1_lane_f32"
  - "arm_neon/vmlaq_lane_s16"
  - "arm_neon/vqadd_u32"
  - "arm_neon/vmul_n_s32"
  - "arm_neon/vld1q_dup_p8"
  - "arm_neon/vtrnq_s8"
  - "arm_neon/vbslq_p8"
  - "arm_neon/vget_lane_s8"
  - "arm_neon/vext_u16"
  - "arm_neon/vsubq_s16"
  - "arm_neon/vld4_lane_s8"
  - "arm_neon/uint32x2x2_t"
  - "arm_neon/vdup_n_s8"
  - "arm_neon/vld4_lane_u16"
  - "arm_neon/vmovq_n_s16"
  - "arm_neon/vst4q_s32"
  - "arm_neon/vst2q_f16"
  - "arm_neon/vbslq_s16"
  - "arm_neon/vand_u64"
  - "arm_neon/poly16_t"
  - "arm_neon/vaba_u16"
  - "arm_neon/vqshlq_s64"
  - "armintr/_arm_uxth"
  - "arm_neon/vst2_lane_s16"
  - "arm_neon/vand_u8"
  - "arm_neon/int8x16x3_t"
  - "arm_neon/vrev64_u16"
  - "arm_neon/vld2_lane_s16"
  - "arm_neon/vabaq_s16"
  - "arm_neon/vsli_n_u8"
  - "arm_neon/vsraq_n_u64"
  - "arm_neon/vmlsl_s16"
  - "arm_neon/vmovn_u64"
  - "arm_neon/vld4_f32"
  - "arm_neon/vst2q_f32"
  - "arm_neon/vtbx3_u8"
  - "arm_neon/vcombine_s8"
  - "arm_neon/vqdmulhq_s32"
  - "arm_neon/vgetq_lane_p8"
  - "armintr/_arm_smusd"
  - "arm_neon/vpmax_u32"
  - "arm_neon/vceq_f32"
  - "arm_neon/vsri_n_p8"
  - "arm_neon/vhsubq_u8"
  - "arm_neon/vuzp_s16"
  - "arm_neon/uint32x2x4_t"
  - "arm_neon/vst4_lane_s32"
  - "arm_neon/vsli_n_p8"
  - "arm_neon/vld3_lane_f16"
  - "arm_neon/vbic_u64"
  - "arm_neon/vmlal_u16"
  - "arm_neon/vmvn_s8"
  - "arm_neon/vtstq_s8"
  - "arm_neon/vmaxq_s32"
  - "arm_neon/vqmovn_u64"
  - "armintr/_arm_ssax"
  - "arm_neon/vext_u32"
  - "arm_neon/vld1_dup_u64"
  - "arm_neon/vmlal_n_s16"
  - "armintr/_arm_smulbb"
  - "arm_neon/vqrdmulhq_lane_s16"
  - "arm_neon/vdup_n_p8"
  - "arm_neon/vaba_s8"
  - "arm_neon/vrshrq_n_s32"
  - "arm_neon/vmvnq_s32"
  - "arm_neon/vpadal_s32"
  - "arm_neon/vqshl_s16"
  - "arm_neon/vtrn_p8"
  - "arm_neon/vzip_s16"
  - "arm_neon/vcge_f32"
  - "armintr/_arm_sxtab16"
  - "arm_neon/vst1q_lane_u64"
  - "arm_neon/vqrshlq_u16"
  - "arm_neon/int8x8_t"
  - "arm_neon/vorr_u8"
  - "arm_neon/vrev64_f32"
  - "arm_neon/vpaddlq_s16"
  - "arm_neon/vdupq_lane_u64"
  - "arm_neon/vcltq_u16"
  - "arm_neon/vst3_lane_f32"
  - "arm_neon/vld2_dup_f32"
  - "armintr/_arm_smmul"
  - "arm_neon/vbsl_s16"
  - "arm_neon/vld1_lane_u8"
  - "arm_neon/vld2q_lane_u16"
  - "arm_neon/vqshlu_n_s32"
  - "armintr/_arm_smlalbt"
  - "arm_neon/vmla_s8"
  - "arm_neon/vsli_n_p16"
  - "arm_neon/vmla_u8"
  - "arm_neon/vqaddq_s16"
  - "arm_neon/vld3_p16"
  - "arm_neon/uint64x2x4_t"
  - "arm_neon/vcnt_u8"
  - "arm_neon/vcltq_u8"
  - "arm_neon/vtbx1_p8"
  - "arm_neon/vrev32q_u16"
  - "arm_neon/vld1_lane_u16"
  - "arm_neon/vqadd_s16"
  - "arm_neon/vcnt_s8"
  - "armintr/_MulUnsignedHigh"
  - "arm_neon/vsliq_n_u8"
  - "arm_neon/vpmin_s16"
  - "armintr/__iso_volatile_load16"
  - "arm_neon/vst2_lane_f32"
  - "arm_neon/vqsubq_s32"
  - "arm_neon/vqshl_s32"
  - "arm_neon/vsraq_n_u32"
  - "arm_neon/vcreate_s32"
  - "arm_neon/vld3q_lane_u32"
  - "arm_neon/vaddq_u16"
  - "arm_neon/vand_s32"
  - "arm_neon/vbicq_s32"
  - "armintr/_arm_smulbt"
  - "arm_neon/vrsra_n_s8"
  - "arm_neon/vshrq_n_u32"
  - "arm_neon/vld4_f16"
  - "arm_neon/vcagtq_f32"
  - "arm_neon/vaddw_u32"
  - "armintr/_arm_uxtah"
  - "arm_neon/vtstq_u8"
  - "arm_neon/vld1_dup_u16"
  - "arm_neon/int16x4x4_t"
  - "arm_neon/vqshluq_n_s8"
  - "arm_neon/vqdmulhq_n_s32"
  - "arm_neon/vst1_s64"
  - "arm_neon/vrsubhn_u16"
  - "arm_neon/vld4_dup_p16"
  - "arm_neon/vmlaq_s32"
  - "arm_neon/vnegq_s32"
  - "arm_neon/vst2q_u8"
  - "arm_neon/vget_low_s32"
  - "arm_neon/vorn_u32"
  - "arm_neon/vld1q_s8"
  - "arm_neon/vandq_s64"
  - "arm_neon/vmvn_p8"
  - "arm_neon/vabdl_s16"
  - "arm_neon/vqshl_u32"
  - "arm_neon/vld3_dup_u16"
  - "arm_neon/vmov_n_f32"
  - "arm_neon/vcvt_f32_u32"
  - "arm_neon/vrhadd_s8"
  - "arm_neon/vpadal_u32"
  - "armintr/_arm_ubfx"
  - "arm_neon/vcgt_s8"
  - "arm_neon/vget_lane_f32"
  - "arm_neon/vcge_s16"
  - "arm_neon/vmov_n_s64"
  - "arm_neon/vmulq_n_f32"
  - "arm_neon/vpadalq_u32"
  - "armintr/_arm_smlaldx"
  - "arm_neon/vtst_u16"
  - "arm_neon/vmls_n_s16"
  - "arm_neon/vcombine_f32"
  - "arm_neon/vld1q_p16"
  - "armintr/_arm_ssat"
  - "arm_neon/vextq_s8"
  - "arm_neon/vmax_u32"
  - "arm_neon/vqsubq_s64"
  - "arm_neon/vcltq_s16"
  - "arm_neon/vst2q_s8"
  - "arm_neon/vpmax_u8"
  - "arm_neon/vld4_dup_p8"
  - "arm_neon/vrshr_n_u64"
  - "arm_neon/vqrshrun_n_s16"
  - "arm_neon/vget_low_u64"
  - "arm_neon/vst2q_s32"
  - "arm_neon/vst4_s32"
  - "arm_neon/vrshrq_n_u8"
  - "arm_neon/vdupq_n_u64"
  - "arm_neon/vsriq_n_u8"
  - "arm_neon/vdupq_lane_u8"
  - "arm_neon/vsriq_n_s64"
  - "arm_neon/vget_low_u8"
  - "arm_neon/vst1_lane_p16"
  - "arm_neon/vld1q_lane_u8"
  - "arm_neon/vcgt_s32"
  - "arm_neon/vst1_lane_u32"
  - "arm_neon/vzipq_p16"
  - "arm_neon/vmvn_u16"
  - "arm_neon/vld1q_lane_u16"
  - "armintr/_MoveToCoprocessor64"
  - "arm_neon/vdup_n_u16"
  - "arm_neon/vzipq_f32"
  - "arm_neon/vshl_s16"
  - "arm_neon/vmlaq_n_s16"
  - "arm_neon/vget_lane_s64"
  - "arm_neon/vld1q_lane_f32"
  - "arm_neon/vnegq_s16"
  - "armintr/_arm_usax"
  - "arm_neon/vabd_s16"
  - "arm_neon/vmovq_n_u32"
  - "arm_neon/vshlq_n_u16"
  - "armintr/_CountLeadingSigns"
  - "arm_neon/vld3q_f16"
  - "arm_neon/vceqq_u32"
  - "arm_neon/int8x8x2_t"
  - "arm_neon/vst2_s64"
  - "arm_neon/vst4q_lane_s16"
  - "arm_neon/vorn_s32"
  - "arm_neon/vcle_f32"
  - "arm_neon/vld1_p16"
  - "arm_neon/vtrn_u32"
  - "arm_neon/vbsl_s32"
  - "arm_neon/float32x2_t"
  - "arm_neon/vmvn_s32"
  - "arm_neon/vqdmlsl_lane_s16"
  - "arm_neon/vtbl3_s8"
  - "arm_neon/vsra_n_u8"
  - "arm_neon/vcvtq_u32_f32"
  - "arm_neon/vst1_p8"
  - "arm_neon/vrev64_p16"
  - "armintr/__ldrexd"
  - "arm_neon/vcgeq_u8"
  - "arm_neon/vmlal_n_s32"
  - "arm_neon/vst1q_lane_p8"
  - "arm_neon/vpadalq_s32"
  - "arm_neon/vtstq_p8"
  - "arm_neon/vld4_lane_u8"
  - "armintr/_arm_ssub16"
  - "arm_neon/vpaddlq_u16"
  - "armintr/_arm_udiv"
  - "arm_neon/vld1_lane_p8"
  - "arm_neon/vst1q_u32"
  - "arm_neon/vld1_f32"
  - "arm_neon/uint64x2x2_t"
  - "arm_neon/vqsubq_u64"
  - "arm_neon/vld4q_s32"
  - "arm_neon/vceq_s16"
  - "arm_neon/vst3_s64"
  - "arm_neon/vext_s8"
  - "armintr/_arm_smlsd"
  - "arm_neon/vpadal_s16"
  - "arm_neon/vbic_s32"
  - "arm_neon/vld1_dup_u8"
  - "arm_neon/vclt_f32"
  - "arm_neon/vrev64_s16"
  - "arm_neon/vrshlq_s64"
  - "arm_neon/vdupq_n_s64"
  - "arm_neon/vuzp_p16"
  - "arm_neon/vld3_dup_p16"
  - "arm_neon/vcreate_s8"
  - "armintr/_arm_smlatt"
  - "arm_neon/vtst_s32"
  - "arm_neon/vshrq_n_s64"
  - "arm_neon/vqshlq_n_s64"
  - "arm_neon/vqshlu_n_s16"
  - "arm_neon/vcleq_s16"
  - "arm_neon/vmull_lane_s16"
  - "arm_neon/int32x4_t"
  - "arm_neon/vqadd_s8"
  - "arm_neon/vld2q_f16"
  - "arm_neon/vld2q_lane_p16"
  - "arm_neon/vadd_u32"
  - "arm_neon/vcntq_u8"
  - "arm_neon/vst1_f32"
  - "arm_neon/vmaxq_u32"
  - "arm_neon/vsub_u64"
  - "arm_neon/vsubl_s32"
  - "arm_neon/poly16x4_t"
  - "arm_neon/vgetq_lane_u16"
  - "arm_neon/vdup_lane_s32"
  - "arm_neon/vrhadd_s32"
  - "arm_neon/veorq_u8"
  - "arm_neon/vclzq_s8"
  - "arm_neon/vsliq_n_s64"
  - "arm_neon/vpadalq_s16"
  - "arm_neon/vmla_n_f32"
  - "arm_neon/vcgt_u16"
  - "armintr/_arm_usada8"
  - "arm_neon/vabd_u32"
  - "arm_neon/vgetq_lane_s8"
  - "arm_neon/vqshlq_n_u64"
  - "arm_neon/vabaq_u32"
  - "armintr/_arm_uhsax"
  - "arm_neon/vmulq_f32"
  - "arm_neon/vld3_dup_s16"
  - "arm_neon/vst3_f16"
  - "arm_neon/vrshrq_n_s64"
  - "armintr/__rdpmccntr64"
  - "arm_neon/vclsq_s32"
  - "arm_neon/vmax_u16"
  - "arm_neon/vmvnq_p8"
  - "arm_neon/veor_u16"
  - "arm_neon/vqshrn_n_u32"
  - "arm_neon/vextq_u64"
  - "arm_neon/vld1q_f32"
  - "arm_neon/vget_low_u32"
  - "arm_neon/vhaddq_s32"
  - "arm_neon/vminq_u16"
  - "arm_neon/vqrdmulhq_lane_s32"
  - "arm_neon/vmla_s16"
  - "arm_neon/vadd_s16"
  - "arm_neon/vbsl_u16"
  - "arm_neon/vhsub_s8"
  - "arm_neon/vld4q_lane_p16"
  - "arm_neon/vld1_s16"
  - "arm_neon/vst2q_lane_p16"
  - "arm_neon/vld2_dup_s8"
  - "arm_neon/vst3q_s16"
  - "arm_neon/vcgeq_u32"
  - "arm_neon/vabdq_s16"
  - "arm_neon/vrhadd_u16"
  - "arm_neon/vqshlq_n_u32"
  - "arm_neon/vst4q_lane_u32"
  - "arm_neon/vrsraq_n_u64"
  - "arm_neon/vmlsq_n_s32"
  - "arm_neon/vld4_u8"
  - "arm_neon/vld2_f16"
  - "arm_neon/vqshlq_u8"
  - "arm_neon/vorrq_u64"
  - "arm_neon/vmin_u16"
  - "arm_neon/vext_u8"
  - "arm_neon/vpaddl_s32"
  - "arm_neon/vshlq_u64"
  - "arm_neon/vst2q_lane_f16"
  - "armintr/_arm_sbfx"
  - "arm_neon/vld3_dup_f16"
  - "armintr/_arm_uhasx"
  - "arm_neon/vst2_lane_u8"
  - "armintr/_arm_smultb"
  - "arm_neon/vdup_n_p16"
  - "arm_neon/vtrnq_u32"
  - "arm_neon/vrshlq_u8"
  - "arm_neon/vld4_lane_p16"
  - "arm_neon/vsraq_n_s32"
  - "arm_neon/vclt_s16"
  - "arm_neon/vzip_u8"
  - "arm_neon/vld3_lane_s16"
  - "arm_neon/vceqq_s32"
  - "arm_neon/vld3_dup_f32"
  - "arm_neon/vld4q_lane_s32"
  - "arm_neon/poly8x16x4_t"
  - "arm_neon/uint64x1x2_t"
  - "arm_neon/vqdmlal_n_s16"
  - "arm_neon/vld2_dup_f16"
  - "arm_neon/vshrq_n_s32"
  - "arm_neon/vcleq_s8"
  - "arm_neon/vld3_s32"
  - "arm_neon/vqrshlq_s64"
  - "arm_neon/vbsl_f32"
  - "arm_neon/vext_s64"
  - "arm_neon/vabaq_s32"
  - "arm_neon/vmulq_s16"
  - "arm_neon/vld3_lane_u16"
  - "arm_neon/vld3q_lane_u16"
  - "armintr/_arm_smlaltt"
  - "arm_neon/poly8x8x2_t"
  - "arm_neon/vst3q_u32"
  - "armintr/_arm_smlsdx"
  - "arm_neon/vqrshl_s64"
  - "arm_neon/vextq_p8"
  - "armintr/_arm_uhsub16"
  - "arm_neon/vld3q_p8"
  - "armintr/_arm_smlawt"
  - "armintr/_arm_smlawb"
  - "arm_neon/vdupq_lane_s8"
  - "arm_neon/vaddl_s16"
  - "arm_neon/vcombine_p16"
  - "arm_neon/vzipq_u32"
  - "arm_neon/poly16x8_t"
  - "arm_neon/vshlq_n_s32"
  - "arm_neon/vrshl_s8"
  - "arm_neon/vst2_u64"
  - "arm_neon/vrev64q_s8"
  - "arm_neon/vst2q_lane_s32"
  - "arm_neon/vld2_dup_s16"
  - "arm_neon/vclt_u16"
  - "arm_neon/vuzp_p8"
  - "arm_neon/vshrq_n_s16"
  - "arm_neon/vst3_u64"
  - "arm_neon/vpmin_u16"
  - "arm_neon/vld3q_lane_s32"
  - "arm_neon/vmlal_s16"
  - "arm_neon/poly16x4x4_t"
  - "arm_neon/vorr_u16"
  - "arm_neon/vsliq_n_s16"
  - "arm_neon/vaddl_u8"
  - "arm_neon/vld4_dup_s32"
  - "arm_neon/vld2_f32"
  - "arm_neon/vclt_u32"
  - "arm_neon/vmull_lane_u16"
  - "arm_neon/vsubw_u32"
  - "arm_neon/vld2_dup_s32"
  - "arm_neon/vuzp_s32"
  - "arm_neon/vcge_s32"
  - "arm_neon/vdup_lane_p16"
  - "arm_neon/vpmin_s8"
  - "arm_neon/vpaddlq_u32"
  - "arm_neon/vmlaq_n_s32"
  - "arm_neon/vshrn_n_u64"
  - "arm_neon/vrshr_n_u16"
  - "arm_neon/vld1_s64"
  - "arm_neon/vbsl_u64"
  - "armintr/_arm_smlad"
  - "arm_neon/vqsub_s16"
  - "arm_neon/vld4_p8"
  - "arm_neon/vqdmulh_lane_s32"
  - "arm_neon/vld3_dup_s64"
  - "arm_neon/vornq_s32"
  - "arm_neon/vpadd_u8"
  - "arm_neon/vld3_lane_p16"
  - "arm_neon/uint64x1x4_t"
  - "arm_neon/vld3_u16"
  - "armintr/_arm_shsax"
  - "arm_neon/vabdq_u16"
  - "arm_neon/vcgtq_f32"
  - "arm_neon/vsubq_s8"
  - "arm_neon/vget_low_f16"
  - "arm_neon/vld4_dup_u64"
  - "arm_neon/vst3_lane_s8"
  - "armintr/_arm_ssat16"
  - "arm_neon/vmlaq_f32"
  - "arm_neon/vsri_n_s32"
  - "arm_neon/vmax_u8"
  - "arm_neon/vqadd_u8"
  - "armintr/_arm_uqsub8"
  - "armintr/_arm_clz"
  - "arm_neon/vcgtq_s32"
  - "arm_neon/vraddhn_s32"
  - "arm_neon/vzip_s8"
  - "arm_neon/veorq_s16"
  - "arm_neon/vsetq_lane_s32"
  - "arm_neon/vmul_n_u16"
  - "armintr/_ReadBankedReg"
  - "arm_neon/vld1q_u8"
  - "arm_neon/vld4_p16"
  - "arm_neon/int64x2x2_t"
  - "arm_neon/vmaxq_s8"
  - "arm_neon/vpmax_s16"
  - "arm_neon/vshlq_u16"
  - "arm_neon/vtrnq_p16"
  - "arm_neon/vabal_u16"
  - "arm_neon/vld2_lane_u16"
  - "arm_neon/vrev32_u8"
  - "arm_neon/vrshl_s32"
  - "arm_neon/vget_low_f32"
  - "arm_neon/vld2_s8"
  - "arm_neon/vclzq_s16"
  - "arm_neon/vqdmulhq_n_s16"
  - "arm_neon/vset_lane_u64"
  - "arm_neon/vld2_dup_p16"
  - "arm_neon/vpaddlq_s32"
  - "arm_neon/vld2q_p8"
  - "arm_neon/vst3_lane_u8"
  - "arm_neon/vld4_dup_f32"
  - "arm_neon/vld2_s64"
  - "arm_neon/vmls_u8"
  - "arm_neon/vtbx4_u8"
  - "arm_neon/vsetq_lane_f32"
  - "arm_neon/vcvt_s32_f32"
  - "arm_neon/vst3q_s32"
  - "arm_neon/vmlsq_s8"
  - "arm_neon/vmlaq_n_u16"
  - "armintr/__iso_volatile_load64"
  - "arm_neon/vcgt_u8"
  - "arm_neon/vld2_dup_p8"
  - "arm_neon/vmov_n_u8"
  - "armintr/_arm_sasx"
  - "arm_neon/vmovq_n_p16"
  - "arm_neon/vmlaq_u32"
  - "arm_neon/vst3_f32"
  - "arm_neon/int32x2x4_t"
  - "arm_neon/vld1q_lane_u64"
  - "arm_neon/vclz_u16"
  - "arm_neon/uint8x8_t"
  - "arm_neon/vsub_u32"
  - "arm_neon/vorn_u8"
  - "armintr/__wfe"
  - "arm_neon/vget_high_s16"
  - "arm_neon/vzip_p8"
  - "arm_neon/vmlal_lane_s16"
  - "arm_neon/vmulq_u8"
  - "armintr/_isunordered"
  - "arm_neon/vld1_dup_f32"
  - "arm_neon/vld4_lane_s16"
  - "arm_neon/vdupq_n_s16"
  - "arm_neon/vst3q_p16"
  - "arm_neon/vst1_lane_f32"
  - "arm_neon/float32x4x3_t"
  - "arm_neon/vand_s8"
  - "arm_neon/float32x2x4_t"
  - "arm_neon/vld3_p8"
  - "arm_neon/vmlaq_lane_u16"
  - "armintr/_arm_uqsub16"
  - "arm_neon/vget_high_s32"
  - "arm_neon/vshl_n_s32"
  - "arm_neon/vornq_s8"
  - "arm_neon/vmlsl_n_u32"
  - "arm_neon/vqshlq_n_s8"
  - "arm_neon/int32x2x2_t"
  - "arm_neon/int16x4x2_t"
  - "arm_neon/vceqq_u8"
  - "arm_neon/vcreate_f16"
  - "arm_neon/vorn_s16"
  - "arm_neon/vqmovn_s32"
  - "arm_neon/vextq_u8"
  - "arm_neon/vld4_s32"
  - "armintr/_WriteStatusReg"
  - "arm_neon/uint8x16_t"
  - "arm_neon/vshrn_n_s64"
  - "arm_neon/vmul_n_u32"
  - "arm_neon/vabdl_u8"
  - "arm_neon/vtbx3_s8"
  - "arm_neon/vaddhn_s16"
  - "arm_neon/vld3q_s8"
  - "arm_neon/vmlsl_n_u16"
  - "arm_neon/vrev64q_s32"
  - "arm_neon/int16x8_t"
  - "arm_neon/vext_s32"
  - "arm_neon/vdupq_n_f32"
  - "arm_neon/vld1q_lane_s32"
  - "arm_neon/vqrshlq_u32"
  - "arm_neon/vtbl2_u8"
  - "arm_neon/vgetq_lane_u8"
  - "arm_neon/veorq_u64"
  - "arm_neon/vcntq_s8"
  - "arm_neon/vbslq_p16"
  - "arm_neon/vqnegq_s32"
  - "arm_neon/vaddw_s32"
  - "arm_neon/vmov_n_p8"
  - "arm_neon/vmull_p8"
  - "arm_neon/vld1_lane_u32"
  - "arm_neon/vcombine_s16"
  - "arm_neon/vqshrn_n_s64"
  - "arm_neon/vceqq_s16"
  - "arm_neon/vld4q_p16"
  - "armintr/_ReadStatusReg"
  - "armintr/_arm_qdadd"
  - "arm_neon/uint32x4x2_t"
  - "arm_neon/vcleq_u8"
  - "armintr/_arm_sxtah"
  - "arm_neon/vrhaddq_s32"
  - "arm_neon/vset_lane_s64"
  - "arm_neon/vld4_s64"
  - "armintr/_DAddSatInt"
  - "arm_neon/vorr_s8"
  - "arm_neon/vst2_u32"
  - "arm_neon/vshll_n_u16"
  - "arm_neon/vld2_dup_u32"
  - "arm_neon/vst3q_lane_s32"
  - "arm_neon/vst3q_p8"
  - "armintr/_MoveFromCoprocessor"
  - "arm_neon/uint32x4_t"
  - "arm_neon/vuzpq_s8"
  - "arm_neon/vrecps_f32"
  - "arm_neon/vst1_lane_s8"
  - "arm_neon/vtbx1_s8"
  - "arm_neon/uint16x8x3_t"
  - "arm_neon/vpaddl_s16"
  - "arm_neon/vsubq_s64"
  - "arm_neon/vrsraq_n_u8"
  - "arm_neon/vqadd_s64"
  - "arm_neon/vst4_lane_s16"
  - "arm_neon/vqadd_u16"
  - "arm_neon/vset_lane_u32"
  - "arm_neon/vand_u32"
  - "arm_neon/vrsqrtsq_f32"
  - "arm_neon/vqaddq_u32"
  - "arm_neon/vsra_n_s64"
  - "armintr/_arm_umlal"
  - "arm_neon/vcvt_f32_f16"
  - "arm_neon/vget_lane_u32"
  - "arm_neon/vbsl_s8"
  - "arm_neon/vrshlq_u32"
  - "arm_neon/vqdmull_lane_s16"
  - "arm_neon/vabsq_s32"
  - "arm_neon/vld3_s8"
  - "arm_neon/vst3q_lane_s16"
  - "arm_neon/vld2q_lane_s16"
  - "arm_neon/vst1_lane_s64"
  - "arm_neon/vmov_n_u16"
  - "arm_neon/vst4_lane_u8"
  - "arm_neon/vshll_n_u32"
  - "arm_neon/vqabs_s8"
  - "arm_neon/vmvnq_u8"
  - "arm_neon/vpadalq_u16"
  - "arm_neon/vbsl_p16"
  - "arm_neon/vqrshrn_n_u16"
  - "arm_neon/vld3q_u32"
  - "arm_neon/vcgeq_f32"
  - "armintr/__iso_volatile_load32"
  - "arm_neon/vrecpe_u32"
  - "arm_neon/vld2_dup_u64"
  - "arm_neon/vld3q_f32"
  - "armintr/_arm_shsub8"
  - "arm_neon/vdup_lane_s64"
  - "arm_neon/vqrshl_s8"
  - "arm_neon/vsliq_n_u16"
  - "arm_neon/vld1q_u16"
  - "arm_neon/vorr_u32"
  - "arm_neon/vqrshl_s32"
  - "armintr/__dmb"
  - "arm_neon/veorq_s8"
  - "arm_neon/vld1_u16"
  - "arm_neon/vmov_n_u32"
  - "arm_neon/vhsub_s16"
  - "arm_neon/vst4q_lane_u16"
  - "arm_neon/vbsl_u8"
  - "armintr/_arm_uxtab"
  - "arm_neon/vld2q_lane_f32"
  - "arm_neon/vst2_p8"
  - "armintr/_arm_smmla"
  - "arm_neon/vaddw_u16"
  - "arm_neon/vmlal_s8"
  - "arm_neon/vtst_u32"
  - "arm_neon/vtbl4_u8"
  - "arm_neon/vcvt_n_f32_s32"
  - "arm_neon/vcageq_f32"
  - "arm_neon/vget_low_s16"
  - "arm_neon/vdupq_n_u8"
  - "arm_neon/vorn_s8"
  - "arm_neon/uint8x16x3_t"
  - "arm_neon/vabdq_u32"
  - "arm_neon/vrev64_p8"
  - "arm_neon/vqsubq_s8"
  - "armintr/_arm_smlabb"
  - "arm_neon/vbicq_s64"
  - "arm_neon/vmaxq_u16"
  - "arm_neon/vdup_n_u8"
  - "arm_neon/veor_s8"
  - "arm_neon/int16x8x2_t"
  - "arm_neon/vcvtq_s32_f32"
  - "arm_neon/vtrn_u16"
  - "arm_neon/vbslq_s32"
  - "arm_neon/vld1q_dup_u32"
  - "arm_neon/vmul_n_f32"
  - "arm_neon/vqrshl_u32"
  - "arm_neon/vqsubq_s16"
  - "arm_neon/vst2_lane_f16"
  - "armintr/_arm_smulwt"
  - "arm_neon/vrshrn_n_u32"
  - "arm_neon/vget_high_p16"
  - "arm_neon/vqadd_u64"
  - "arm_neon/vsli_n_s32"
  - "arm_neon/vhadd_u32"
  - "arm_neon/vmlsl_lane_u16"
  - "arm_neon/vclzq_u32"
  - "arm_neon/vqshrun_n_s64"
  - "arm_neon/vrev64q_u32"
  - "arm_neon/vqshrun_n_s16"
  - "arm_neon/vrev32q_s8"
  - "armintr/_arm_shasx"
  - "arm_neon/vaddl_s8"
  - "armintr/_arm_smull"
  - "arm_neon/vabaq_u8"
  - "armintr/_arm_revsh"
  - "arm_neon/vsubq_f32"
  - "arm_neon/poly16x4x2_t"
  - "arm_neon/poly8x8x3_t"
  - "arm_neon/vsubhn_s64"
  - "arm_neon/vcle_u16"
  - "arm_neon/poly8x16x3_t"
  - "arm_neon/vqdmlsl_n_s16"
  - "arm_neon/vqshl_u64"
  - "arm_neon/vcge_u16"
  - "armintr/_arm_uasx"
  - "arm_neon/vmovl_s32"
  - "arm_neon/vst1q_lane_u16"
  - "arm_neon/vbic_u32"
  - "arm_neon/vld2_s16"
  - "armintr/_arm_qasx"
  - "arm_neon/vorrq_u8"
  - "arm_neon/vst2_s32"
  - "armintr/_WriteBankedReg"
  - "arm_neon/veorq_s64"
  - "arm_neon/vld4_lane_f32"
  - "arm_neon/vcreate_u8"
  - "arm_neon/vset_lane_u8"
  - "arm_neon/vandq_u16"
  - "arm_neon/vrsubhn_s64"
  - "arm_neon/vst1q_lane_p16"
  - "arm_neon/uint8x8x2_t"
  - "arm_neon/vmlsl_s8"
  - "arm_neon/vmax_s32"
  - "arm_neon/uint32x4x3_t"
  - "arm_neon/vld4_dup_u16"
  - "arm_neon/vabs_s32"
  - "arm_neon/vld3_dup_u32"
  - "arm_neon/vrshl_u16"
  - "arm_neon/vcle_u8"
  - "arm_neon/vqshl_n_u16"
  - "arm_neon/vbic_s8"
  - "arm_neon/float32x4x2_t"
  - "arm_neon/vmls_f32"
  - "arm_neon/vshll_n_u8"
  - "arm_neon/vminq_s8"
  - "arm_neon/vmlsq_lane_f32"
  - "arm_neon/vst1q_f16"
  - "arm_neon/vst1_lane_u64"
  - "arm_neon/vrhadd_u8"
  - "arm_neon/vclt_s32"
  - "arm_neon/vst2_p16"
  - "arm_neon/vrshrq_n_u16"
  - "arm_neon/vneg_s32"
  - "arm_neon/vmovl_s16"
  - "arm_neon/vqshlq_s8"
  - "arm_neon/vld1_s8"
  - "arm_neon/vqdmulh_s32"
  - "arm_neon/vcls_s8"
  - "armintr/__trap"
  - "arm_neon/vuzp_u32"
  - "armintr/_CopyInt64FromDouble"
  - "arm_neon/int8x16x2_t"
  - "arm_neon/vmovn_s32"
  - "arm_neon/vget_high_s8"
  - "arm_neon/veor_s64"
  - "armintr/_arm_uadd8"
  - "arm_neon/vrev16_u8"
  - "arm_neon/vbicq_u64"
  - "arm_neon/vst4_lane_f16"
  - "arm_neon/vst3_s32"
  - "arm_neon/poly8x8_t"
  - "arm_neon/vtstq_u16"
  - "arm_neon/vld1_lane_s8"
  - "arm_neon/float32x4x4_t"
  - "arm_neon/vst2_s16"
  - "arm_neon/vqrdmulhq_s32"
  - "arm_neon/vqdmulhq_s16"
  - "arm_neon/vrshrq_n_s8"
  - "arm_neon/vcle_s32"
  - "arm_neon/vtbl3_p8"
  - "arm_neon/vbslq_u8"
  - "arm_neon/vst4_u64"
  - "armintr/_arm_umaal"
  - "arm_neon/vshll_n_s8"
  - "arm_neon/vcvt_u32_f32"
  - "arm_neon/vld4q_p8"
  - "arm_neon/vsetq_lane_u16"
  - "arm_neon/vabd_u8"
  - "arm_neon/vclz_u8"
  - "arm_neon/vsubq_u32"
  - "arm_neon/vld1q_lane_p16"
  - "arm_neon/vcgtq_s16"
  - "arm_neon/vmla_lane_s32"
  - "arm_neon/vshlq_n_s64"
  - "arm_neon/vbsl_u32"
  - "arm_neon/vqshlq_s16"
  - "armintr/_arm_qadd8"
  - "arm_neon/vrshr_n_s32"
  - "armintr/_CountOneBits64"
  - "arm_neon/vceq_u32"
  - "arm_neon/vbsl_p8"
  - "arm_neon/uint16x8x2_t"
  - "arm_neon/vsli_n_s16"
  - "arm_neon/vmla_n_s32"
  - "arm_neon/vld4_dup_u32"
  - "arm_neon/vshrq_n_s8"
  - "arm_neon/vqaddq_s8"
  - "arm_neon/vshl_n_u64"
  - "arm_neon/vtbl2_p8"
  - "arm_neon/vcleq_u32"
  - "arm_neon/vqsub_u32"
  - "arm_neon/vmovl_u8"
  - "arm_neon/vmlal_u8"
  - "arm_neon/vmul_s8"
  - "armintr/_MoveFromCoprocessor64"
  - "arm_neon/vrsraq_n_s16"
  - "arm_neon/vdupq_n_u32"
  - "arm_neon/vmov_n_s16"
  - "arm_neon/vst4_lane_p8"
  - "arm_neon/vld1_s32"
  - "arm_neon/vst4_p8"
  - "arm_neon/vsriq_n_u32"
  - "arm_neon/vqdmull_n_s16"
  - "arm_neon/vshlq_u32"
  - "arm_neon/vld3_u8"
  - "armintr/_arm_usub16"
  - "arm_neon/vmlsq_lane_s16"
  - "arm_neon/vmovq_n_s8"
  - "arm_neon/int32x4x2_t"
  - "arm_neon/vld4q_u8"
  - "arm_neon/poly16x8x2_t"
  - "arm_neon/vld1q_u64"
  - "arm_neon/vld3q_lane_s16"
  - "arm_neon/int64x1x2_t"
  - "arm_neon/vshlq_n_s8"
  - "arm_neon/vrshl_s64"
  - "arm_neon/vqshl_n_u8"
  - "armintr/_arm_qadd"
  - "armintr/_DSubSatInt"
  - "armintr/_arm_usat16"
  - "arm_neon/vmull_s8"
  - "arm_neon/vsub_s8"
  - "arm_neon/vmovq_n_u16"
  - "arm_neon/vst4_u16"
  - "arm_neon/vmlsl_lane_u32"
  - "arm_neon/vsliq_n_p16"
  - "arm_neon/vmovn_u32"
  - "arm_neon/vbic_u16"
  - "arm_neon/vtbx2_p8"
  - "arm_neon/vrsubhn_s32"
  - "armintr/_SubSatInt"
  - "arm_neon/vst3_u8"
  - "arm_neon/vdupq_n_s32"
  - "arm_neon/vcntq_p8"
  - "arm_neon/vst4_f32"
  - "arm_neon/vbic_s64"
  - "arm_neon/vld3_s64"
  - "arm_neon/vrsra_n_s64"
  - "arm_neon/vqabsq_s16"
  - "arm_neon/vsriq_n_p8"
  - "arm_neon/vst2_lane_p16"
  - "arm_neon/vabsq_s16"
  - "arm_neon/vcombine_u8"
  - "arm_neon/vld2q_p16"
  - "armintr/_CountOneBits"
  - "armintr/__prefetch"
  - "arm_neon/vld3_dup_u64"
  - "arm_neon/vld2q_s16"
  - "arm_neon/vget_low_p16"
  - "arm_neon/vuzpq_u8"
  - "arm_neon/vrev32q_s16"
  - "armintr/_AddSatInt"
  - "arm_neon/uint16x4x2_t"
  - "arm_neon/vmov_n_s32"
  - "arm_neon/vaddl_u16"
  - "arm_neon/vqaddq_s64"
  - "arm_neon/vmlaq_u16"
  - "arm_neon/vsli_n_s8"
  - "armintr/_arm_sxth"
  - "arm_neon/vorr_s32"
  - "arm_neon/vsra_n_u64"
  - "arm_neon/vst2_f16"
  - "arm_neon/vcombine_u16"
  - "arm_neon/vabs_s16"
  - "arm_neon/vsubhn_s32"
  - "arm_neon/vst1q_lane_u32"
  - "arm_neon/vst3_p8"
  - "arm_neon/vqshrun_n_s32"
  - "arm_neon/vcreate_s64"
  - "arm_neon/vld4q_lane_s16"
  - "arm_neon/vzipq_u16"
  - "arm_neon/vmin_s32"
  - "armintr/_CopyInt32FromFloat"
  - "arm_neon/vcgtq_u32"
  - "arm_neon/vabdl_s32"
  - "arm_neon/vqshlq_n_u16"
  - "arm_neon/int8x16x4_t"
  - "arm_neon/vqrdmulh_n_s32"
  - "arm_neon/vqaddq_u64"
  - "arm_neon/vhaddq_s8"
  - "arm_neon/vshll_n_s16"
  - "arm_neon/vuzp_u8"
  - "arm_neon/vaddl_u32"
  - "arm_neon/vld4q_s16"
  - "arm_neon/vqmovun_s16"
  - "arm_neon/vld1q_lane_s8"
  - "arm_neon/vld2_lane_u32"
  - "arm_neon/vrshr_n_s8"
  - "arm_neon/vmlaq_s16"
  - "armintr/_CopyFloatFromInt32"
  - "arm_neon/vmul_f32"
  - "arm_neon/vmlaq_n_f32"
  - "arm_neon/vst4_s16"
  - "arm_neon/vld1_dup_s32"
  - "arm_neon/vmul_u16"
  - "arm_neon/vhaddq_s16"
  - "arm_neon/vst1q_lane_f32"
  - "arm_neon/vrhaddq_u16"
  - "arm_neon/vbicq_u32"
  - "arm_neon/vrev32_s8"
  - "arm_neon/vmlaq_s8"
  - "arm_neon/vmin_s16"
  - "arm_neon/vst3_lane_p16"
  - "arm_neon/vst2q_lane_f32"
  - "arm_neon/vld4q_lane_f32"
  - "arm_neon/vget_low_u16"
  - "arm_neon/vqsub_s32"
  - "arm_neon/vtbl1_s8"
  - "arm_neon/vmovn_s64"
  - "arm_neon/vpmax_s8"
  - "arm_neon/int8x16_t"
  - "arm_neon/vpmin_u8"
  - "arm_neon/vdup_lane_p8"
  - "arm_neon/vsetq_lane_u64"
  - "arm_neon/vuzpq_u16"
  - "arm_neon/vcgeq_u16"
  - "arm_neon/uint8x16x2_t"
  - "armintr/_arm_rev16"
  - "armintr/_arm_sxtb"
  - "arm_neon/vsliq_n_u64"
  - "arm_neon/vmovq_n_u8"
  - "arm_neon/vshlq_n_u32"
  - "arm_neon/vcombine_s64"
  - "armintr/_arm_qsax"
  - "arm_neon/vmin_f32"
  - "armintr/_arm_sadd16"
  - "arm_neon/vmlsq_n_s16"
  - "arm_neon/vorr_u64"
  - "arm_neon/vqrshrun_n_s64"
  - "arm_neon/vld2q_lane_s32"
  - "arm_neon/vgetq_lane_p16"
  - "arm_neon/vrev32_s16"
  - "arm_neon/vqshl_u16"
  - "arm_neon/vtrn_s8"
  - "arm_neon/vst1q_lane_s64"
  - "arm_neon/vtbl4_p8"
  - "arm_neon/vst1_p16"
  - "arm_neon/vmvn_u8"
  - "arm_neon/vld2_lane_u8"
  - "arm_neon/vld2q_u16"
  - "arm_neon/vmovl_s8"
  - "arm_neon/vbslq_u64"
  - "arm_neon/vmls_s8"
  - "arm_neon/vld3q_p16"
  - "arm_neon/vtbl3_u8"
  - "arm_neon/vabs_f32"
  - "arm_neon/vsraq_n_s8"
  - "arm_neon/vqadd_s32"
  - "arm_neon/vmulq_n_s16"
  - "arm_neon/vst3q_s8"
  - "arm_neon/vaddhn_s64"
  - "arm_neon/vmul_n_s16"
  - "arm_neon/vtbl1_p8"
  - "arm_neon/uint64x2x3_t"
  - "arm_neon/vmlsq_s32"
  - "arm_neon/vld2q_lane_u32"
  - "arm_neon/vaddq_u8"
  - "arm_neon/vcombine_f16"
  - "arm_neon/vandq_s16"
  - "arm_neon/vst4q_lane_p16"
  - "arm_neon/vsri_n_u8"
  - "arm_neon/vst3_lane_p8"
  - "arm_neon/vst3_lane_s16"
  - "arm_neon/vdup_n_s16"
  - "arm_neon/vbicq_s8"
  - "arm_neon/vdup_lane_u8"
  - "arm_neon/vst4q_lane_s32"
  - "arm_neon/vqrshl_u16"
  - "arm_neon/vrsra_n_u32"
  - "arm_neon/vdupq_lane_p8"
  - "arm_neon/vld3_lane_u8"
  - "arm_neon/vqrdmulh_n_s16"
  - "arm_neon/vpmin_s32"
  - "armintr/__cps"
  - "arm_neon/vshl_u32"
  - "armintr/_arm_uadd16"
  - "arm_neon/vld3_s16"
  - "arm_neon/vcvt_f32_s32"
  - "arm_neon/vshlq_n_u64"
  - "arm_neon/vrev64q_u8"
  - "arm_neon/vextq_u16"
  - "arm_neon/vsubl_s16"
  - "arm_neon/vget_lane_p8"
  - "arm_neon/vabal_s16"
  - "arm_neon/vrecpeq_u32"
  - "arm_neon/vminq_u8"
  - "arm_neon/veor_s16"
  - "arm_neon/vmull_n_u16"
  - "arm_neon/vshl_n_u8"
  - "arm_neon/vrev32q_u8"
  - "arm_neon/vandq_s8"
  - "arm_neon/vrshlq_s16"
  - "arm_neon/vst4q_p16"
  - "arm_neon/vandq_s32"
  - "armintr/_MoveToCoprocessor2"
  - "arm_neon/vqdmlsl_lane_s32"
  - "arm_neon/vld1q_s64"
  - "arm_neon/vmull_n_s16"
  - "arm_neon/vneg_s16"
  - "arm_neon/vqshluq_n_s64"
  - "arm_neon/vst2_lane_s32"
  - "arm_neon/vmvnq_u16"
  - "arm_neon/vshll_n_s32"
  - "arm_neon/vld3_dup_s8"
  - "arm_neon/vtstq_s32"
  - "arm_neon/vmlsl_u32"
  - "arm_neon/vqdmulhq_lane_s16"
  - "arm_neon/vaddl_s32"
  - "armintr/_CountLeadingZeros"
  - "arm_neon/vqrshrn_n_s16"
  - "arm_neon/vmla_lane_u32"
  - "arm_neon/vst1_u8"
  - "arm_neon/vshl_u64"
  - "arm_neon/vshr_n_u8"
  - "arm_neon/vmull_lane_s32"
  - "arm_neon/vmlal_lane_u32"
  - "arm_neon/vsubl_s8"
  - "arm_neon/float32x2x2_t"
  - "armintr/_arm_bfc"
  - "arm_neon/vaddq_s16"
  - "arm_neon/vmlal_lane_s32"
  - "arm_neon/vpadd_u16"
  - "arm_neon/vst2q_lane_u16"
  - "arm_neon/vld4_s8"
  - "arm_neon/vst1q_s8"
  - "arm_neon/vshrq_n_u64"
  - "arm_neon/vsli_n_u16"
  - "arm_neon/vqrdmulh_lane_s32"
  - "arm_neon/vst4_lane_u16"
  - "arm_neon/vabdq_f32"
  - "arm_neon/vld2_lane_f16"
  - "arm_neon/vqsub_u64"
  - "arm_neon/vsub_f32"
  - "arm_neon/vld1q_s16"
  - "arm_neon/vmaxq_s16"
  - "arm_neon/vcombine_u32"
  - "arm_neon/vrsraq_n_u32"
  - "armintr/_arm_smusdx"
  - "arm_neon/vrev16_s8"
  - "arm_neon/vqdmulh_n_s32"
  - "arm_neon/vmul_s32"
  - "arm_neon/vabdq_s32"
  - "arm_neon/veor_u64"
  - "arm_neon/vmlsl_n_s32"
  - "arm_neon/vsub_s16"
  - "arm_neon/vadd_u16"
  - "arm_neon/vsriq_n_u16"
  - "arm_neon/vmla_u32"
  - "arm_neon/vuzpq_s32"
  - "arm_neon/vst4q_s8"
  - "arm_neon/vaddhn_u32"
  - "arm_neon/vmlaq_lane_f32"
  - "arm_neon/vld3_lane_s8"
  - "arm_neon/vsliq_n_u32"
  - "arm_neon/vqrshlq_s8"
  - "arm_neon/vqdmlal_n_s32"
  - "arm_neon/uint8x16x4_t"
  - "arm_neon/vcgtq_u16"
  - "arm_neon/vandq_u32"
  - "arm_neon/vld4q_lane_u32"
  - "arm_neon/vzip_p16"
  - "arm_neon/vget_low_p8"
  - "armintr/_arm_shadd8"
  - "arm_neon/vmovn_s16"
  - "arm_neon/vcge_u8"
  - "arm_neon/vld2q_f32"
  - "arm_neon/vaba_u32"
  - "armintr/__iso_volatile_store8"
  - "arm_neon/vst2q_p16"
  - "arm_neon/vmul_s16"
  - "arm_neon/vand_s16"
  - "arm_neon/vtbx4_p8"
  - "arm_neon/vceq_u8"
  - "arm_neon/vrhaddq_s16"
  - "arm_neon/vgetq_lane_f32"
  - "arm_neon/vqshl_s8"
  - "arm_neon/vbslq_f32"
  - "arm_neon/vrsqrts_f32"
  - "arm_neon/vld2q_s8"
  - "arm_neon/vtbl1_u8"
  - "arm_neon/vtst_u8"
  - "arm_neon/vrev64q_f32"
  - "arm_neon/vcle_s8"
  - "arm_neon/vsetq_lane_p16"
  - "arm_neon/vcreate_p16"
  - "arm_neon/vabal_s32"
  - "armintr/_arm_smlald"
  - "arm_neon/vmla_f32"
  - "arm_neon/vtbx2_s8"
  - "arm_neon/int64x1x3_t"
  - "arm_neon/vclz_s8"
  - "arm_neon/vorr_s16"
  - "arm_neon/vornq_s64"
  - "arm_neon/vst1q_u64"
  - "arm_neon/vdupq_n_s8"
  - "armintr/_arm_sadd8"
  - "arm_neon/vextq_s32"
  - "armintr/_arm_smuadx"
  - "armintr/_arm_qsub"
  - "arm_neon/vadd_f32"
  - "arm_neon/vrshrq_n_s16"
  - "arm_neon/vqsub_s8"
  - "arm_neon/vld3_f32"
  - "arm_neon/vhadd_s8"
  - "arm_neon/vmull_n_u32"
  - "arm_neon/vdup_n_u64"
  - "arm_neon/vsubw_s32"
  - "armintr/_arm_sxtab"
  - "armintr/_arm_uxtb16"
  - "arm_neon/vmvn_s16"
  - "arm_neon/vst1_lane_s16"
  - "arm_neon/vqrdmulhq_n_s32"
  - "arm_neon/vsriq_n_s32"
  - "arm_neon/poly8x16x2_t"
  - "arm_neon/vadd_u8"
  - "arm_neon/vuzpq_p8"
  - "arm_neon/vst2q_p8"
  - "armintr/__wfi"
  - "arm_neon/vget_high_u16"
  - "arm_neon/vqrshl_u64"
  - "arm_neon/vld1_dup_s64"
  - "arm_neon/vqrshrn_n_s32"
  - "arm_neon/vrshr_n_s64"
  - "arm_neon/vst3_s8"
  - "arm_neon/poly16x4x3_t"
  - "arm_neon/vqrdmulh_lane_s16"
  - "arm_neon/vmvnq_u32"
  - "arm_neon/vqsubq_u32"
  - "arm_neon/vmovq_n_p8"
  - "arm_neon/vtrn_s16"
  - "arm_neon/vld2q_u32"
  - "arm_neon/vqsubq_u16"
  - "arm_neon/vrsqrteq_u32"
  - "arm_neon/vadd_u64"
  - "armintr/_arm_usat"
  - "arm_neon/vcvtq_n_u32_f32"
  - "arm_neon/vaddq_s8"
  - "arm_neon/vrsraq_n_u16"
  - "arm_neon/vqabs_s16"
  - "arm_neon/vsra_n_s8"
  - "arm_neon/vsra_n_s16"
  - "arm_neon/vqshlq_n_u8"
  - "arm_neon/vpadal_s8"
  - "arm_neon/vmlal_n_u16"
  - "armintr/_CopyDoubleFromInt64"
  - "arm_neon/vaddw_u8"
  - "arm_neon/vmulq_n_s32"
  - "arm_neon/vqaddq_s32"
  - "arm_neon/vmla_lane_f32"
  - "arm_neon/vmlaq_lane_s32"
  - "arm_neon/vld1q_dup_u64"
  - "arm_neon/uint16x8_t"
  - "arm_neon/vld2_s32"
  - "arm_neon/vcltq_f32"
  - "arm_neon/vst4q_f32"
  - "arm_neon/vsri_n_u16"
  - "arm_neon/vshlq_s32"
  - "arm_neon/vgetq_lane_u32"
  - "arm_neon/vld1q_dup_f16"
  - "arm_neon/vrev64q_s16"
  - "arm_neon/vrshrq_n_u32"
  - "arm_neon/vld2q_s32"
  - "arm_neon/vcgtq_s8"
  - "arm_neon/vsubhn_u64"
  - "arm_neon/vmls_n_s32"
  - "armintr/_arm_smmlar"
  - "arm_neon/vld3_dup_u8"
  - "arm_neon/vld3q_lane_p16"
  - "arm_neon/vld2_dup_s64"
  - "arm_neon/vqabs_s32"
  - "arm_neon/vqaddq_u8"
  - "arm_neon/vminq_u32"
  - "arm_neon/vpaddl_u16"
  - "arm_neon/vaba_s16"
  - "arm_neon/vmul_u32"
  - "arm_neon/vst1_lane_u16"
  - "arm_neon/vcreate_f32"
  - "arm_neon/vcvt_f16_f32"
  - "arm_neon/vset_lane_s32"
  - "arm_neon/vshl_s8"
  - "arm_neon/vcgt_s16"
  - "arm_neon/vtrn_f32"
  - "arm_neon/vget_high_s64"
  - "arm_neon/vld3_dup_p8"
  - "arm_neon/vcreate_u64"
  - "arm_neon/vext_u64"
  - "arm_neon/vld1q_dup_s16"
  - "arm_neon/vget_lane_s16"
  - "arm_neon/vqdmlal_s16"
  - "arm_neon/vld2_p16"
  - "arm_neon/vld4_u16"
  - "armintr/_arm_smlalbb"
  - "arm_neon/vrev64_u8"
  - "arm_neon/vbslq_s64"
  - "arm_neon/vsubw_u16"
  - "arm_neon/vrsubhn_u32"
  - "arm_neon/vabdq_u8"
  - "arm_neon/vmls_n_u32"
  - "arm_neon/vshr_n_s32"
  - "arm_neon/vmulq_n_u32"
  - "arm_neon/vst3_p16"
  - "arm_neon/vrev32_u16"
  - "arm_neon/int8x8x3_t"
  - "arm_neon/vst2q_lane_u32"
  - "arm_neon/vextq_p16"
  - "arm_neon/vtrnq_f32"
  - "armintr/_arm_smultt"
  - "arm_neon/vqneg_s8"
  - "arm_neon/vmlsq_lane_s32"
  - "arm_neon/vmov_n_p16"
  - "arm_neon/vraddhn_u64"
  - "arm_neon/vrhadd_u32"
  - "arm_neon/vrev64_u32"
  - "arm_neon/vrshrn_n_s32"
  - "arm_neon/vld4q_f32"
  - "arm_neon/vst2_s8"
  - "arm_neon/vrsqrteq_f32"
  - "arm_neon/uint16x4_t"
  - "arm_neon/vget_low_s8"
  - "arm_neon/vst2_lane_u32"
  - "arm_neon/vhsub_s32"
  - "arm_neon/vqdmull_lane_s32"
  - "armintr/_arm_smulwb"
  - "arm_neon/vmlsl_u8"
  - "arm_neon/vdup_lane_s16"
  - "arm_neon/vtbx4_s8"
  - "arm_neon/vld4q_lane_u16"
  - "arm_neon/vget_high_u8"
  - "arm_neon/vclzq_s32"
  - "arm_neon/vld1q_dup_f32"
  - "arm_neon/vtrn_u8"
  - "arm_neon/vqabsq_s8"
  - "arm_neon/vdup_lane_f32"
  - "arm_neon/vqrdmulh_s16"
  - "arm_neon/vst4_u32"
  - "arm_neon/vdup_lane_u32"
  - "arm_neon/vst4_u8"
  - "arm_neon/vmovq_n_s32"
  - "arm_neon/vld2_lane_s8"
  - "arm_neon/vld3_u32"
  - "arm_neon/vsubl_u16"
  - "arm_neon/vqshlu_n_s8"
  - "arm_neon/float32x4_t"
  - "arm_neon/vqshl_n_s32"
  - "arm_neon/float32x2x3_t"
  - "armintr/__hvc"
  - "arm_neon/vst1q_lane_f16"
  - "arm_neon/vmvnq_s16"
  - "arm_neon/vst3q_lane_f32"
  - "arm_neon/vld1q_dup_u8"
  - "arm_neon/vmlsq_s16"
  - "arm_neon/vget_lane_u8"
  - "arm_neon/vld1_lane_s32"
  - "arm_neon/vst4q_s16"
  - "armintr/_arm_qsub8"
  - "arm_neon/vorrq_s32"
  - "arm_neon/vsriq_n_s8"
  - "arm_neon/vqshrn_n_u64"
  - "arm_neon/vdup_n_s32"
  - "armintr/_arm_uhsub8"
  - "arm_neon/vld3_lane_s32"
  - "arm_neon/vbsl_s64"
  - "arm_neon/vld1_dup_f16"
  - "arm_neon/vsli_n_u64"
  - "arm_neon/vraddhn_u32"
  - "arm_neon/vsub_u16"
  - "arm_neon/vcltq_u32"
  - "arm_neon/vminq_f32"
  - "arm_neon/vshl_n_s64"
  - "arm_neon/vld4_u32"
  - "arm_neon/vld1_u32"
  - "arm_neon/vaddhn_u16"
  - "arm_neon/vcvtq_n_f32_s32"
  - "arm_neon/vorn_u64"
  - "arm_neon/vsubhn_u16"
  - "arm_neon/int64x1_t"
  - "arm_neon/vst1q_lane_s8"
  - "arm_neon/vld1q_dup_s32"
  - "arm_neon/vrev32_p8"
  - "arm_neon/vst3q_lane_p16"
  - "arm_neon/vrecpeq_f32"
  - "arm_neon/int8x8x4_t"
  - "arm_neon/vshr_n_u32"
  - "arm_neon/vdupq_lane_s64"
  - "arm_neon/vpaddlq_s8"
  - "arm_neon/vqshl_n_u32"
  - "arm_neon/vmul_u8"
  - "arm_neon/vtbx2_u8"
  - "arm_neon/vshr_n_u64"
  - "arm_neon/vqrshlq_s16"
  - "arm_neon/vst3_lane_u16"
  - "arm_neon/vqsub_u8"
  - "arm_neon/vrsra_n_s16"
  - "arm_neon/vaba_s32"
  - "arm_neon/vsri_n_u64"
  - "arm_neon/vst3q_lane_u32"
  - "arm_neon/vmlsq_n_u32"
  - "arm_neon/poly8x16_t"
  - "arm_neon/vld2_u8"
  - "armintr/_arm_smmulr"
  - "arm_neon/vtst_s16"
  - "armintr/_arm_smmls"
  - "arm_neon/vqdmulh_s16"
  - "arm_neon/vtrnq_u8"
  - "arm_neon/vset_lane_p8"
  - "arm_neon/vmlsl_u16"
  - "arm_neon/vshrn_n_u16"
  - "arm_neon/vld1_dup_p8"
  - "arm_neon/vrev16q_s8"
  - "arm_neon/vmov_n_s8"
  - "arm_neon/vld1_u64"
  - "arm_neon/vpmin_f32"
  - "arm_neon/vmla_n_u16"
  - "arm_neon/vst1_f16"
  - "arm_neon/vqdmlsl_s16"
  - "arm_neon/vmin_u32"
  - "armintr/_arm_qsub16"
  - "arm_neon/vcage_f32"
  - "arm_neon/vornq_u32"
  - "arm_neon/vpadd_s16"
  - "arm_neon/vld1_u8"
  - "arm_neon/vhsubq_s16"
  - "arm_neon/vld1_dup_u32"
  - "arm_neon/vld4_u64"
  - "armintr/_MulHigh"
  - "arm_neon/vmaxq_u8"
  - "arm_neon/vget_lane_u16"
  - "arm_neon/vld2q_u8"
  - "arm_neon/vld1q_dup_p16"
  - "arm_neon/vsraq_n_u8"
  - "arm_neon/vqdmlsl_n_s32"
  - "arm_neon/vst1_s16"
  - "arm_neon/vst1q_s32"
  - "arm_neon/vmaxq_f32"
  - "arm_neon/vqdmulh_lane_s16"
  - "armintr/__isb"
  - "arm_neon/vuzpq_p16"
  - "arm_neon/vmls_lane_s16"
  - "arm_neon/vtbl4_s8"
  - "arm_neon/vst1_lane_p8"
  - "arm_neon/vsubw_s8"
  - "arm_neon/vmin_u8"
  - "arm_neon/vzip_u16"
  - "arm_neon/vld4q_u16"
  - "arm_neon/vshrn_n_s32"
  - "arm_neon/vpadal_u16"
  - "arm_neon/vorrq_s8"
  - "arm_neon/vrshlq_u64"
  - "arm_neon/vst3_lane_s32"
  - "arm_neon/vqshluq_n_s32"
  - "armintr/_arm_shsub16"
  - "arm_neon/vst1_u32"
  - "arm_neon/vrhadd_s16"
  - "arm_neon/vzipq_s32"
  - "arm_neon/vshrq_n_u16"
  - "arm_neon/vcls_s32"
  - "arm_neon/vceq_s8"
  - "arm_neon/vld2q_lane_f16"
  - "arm_neon/vst4q_u8"
  - "arm_neon/vraddhn_u16"
  - "arm_neon/vget_lane_u64"
  - "armintr/_arm_smlsld"
  - "arm_neon/vld3_u64"
  - "arm_neon/vld1_lane_s16"
  - "arm_neon/vabd_f32"
  - "arm_neon/vdupq_n_u16"
  - "armintr/__iso_volatile_store64"
  - "arm_neon/vqsubq_u8"
  - "arm_neon/poly16x8x3_t"
  - "arm_neon/vcltq_s32"
  - "arm_neon/vqnegq_s16"
  - "arm_neon/vqsub_u16"
  - "arm_neon/vaddq_s32"
  - "arm_neon/vqshl_n_s64"
  - "arm_neon/vabdl_s8"
  - "arm_neon/vclsq_s16"
  - "arm_neon/vpaddl_u8"
  - "arm_neon/vmlsq_n_u16"
  - "armintr/_arm_uqadd8"
  - "arm_neon/vhsub_u32"
  - "arm_neon/vset_lane_s16"
  - "arm_neon/vsubl_u32"
  - "arm_neon/vld3_lane_f32"
  - "arm_neon/vcle_s16"
  - "arm_neon/vmovl_u32"
  - "arm_neon/vst3_lane_f16"
  - "arm_neon/vcaltq_f32"
  - "arm_neon/vsubq_s32"
  - "arm_neon/vand_s64"
  - "arm_neon/vst2_u8"
  - "arm_neon/vcombine_p8"
  - "arm_neon/vqdmlal_s32"
  - "arm_neon/vsub_s32"
  - "armintr/_arm_uxtab16"
  - "arm_neon/vmlsq_n_f32"
  - "armintr/_arm_qdsub"
  - "arm_neon/vhaddq_u32"
  - "arm_neon/vhsubq_u16"
  - "arm_neon/vmlsq_lane_u16"
  - "arm_neon/vst4_s64"
  - "armintr/_CountLeadingOnes"
  - "armintr/_arm_smlabt"
  - "arm_neon/vcombine_s32"
  - "arm_neon/vld4_lane_f16"
  - "arm_neon/vadd_s64"
  - "arm_neon/vorrq_u32"
  - "armintr/__sev"
  - "arm_neon/vdupq_lane_s32"
  - "arm_neon/vrecpsq_f32"
  - "arm_neon/vbicq_u16"
  - "arm_neon/vld1_lane_p16"
  - "arm_neon/vrshr_n_u32"
  - "arm_neon/vcgeq_s32"
  - "arm_neon/vld4_dup_s16"
  - "arm_neon/vld1q_p8"
  - "arm_neon/vrshlq_u16"
  - "arm_neon/vmlaq_lane_u32"
  - "arm_neon/vsub_s64"
  - "arm_neon/vcreate_u16"
  - "arm_neon/vget_lane_s32"
  - "arm_neon/vuzp_f32"
  - "arm_neon/vld2_lane_p8"
  - "arm_neon/vuzp_u16"
  - "arm_neon/vorrq_s16"
  - "armintr/_arm_smlaltb"
  - "arm_neon/vrshrn_n_s16"
  - "arm_neon/vabd_s8"
  - "arm_neon/vnegq_s8"
  - "arm_neon/vst4q_u16"
  - "arm_neon/vst1q_lane_s32"
  - "arm_neon/vst1_lane_s32"
  - "arm_neon/vmla_u16"
  - "arm_neon/vmls_lane_s32"
  - "arm_neon/vtst_s8"
  - "arm_neon/vcgeq_s8"
  - "arm_neon/poly8x8x4_t"
  - "arm_neon/vqsub_s64"
  - "armintr/_arm_uqasx"
  - "arm_neon/vld1_lane_u64"
  - "arm_neon/vminq_s16"
  - "arm_neon/vmulq_u32"
  - "arm_neon/vqrshlq_u8"
  - "arm_neon/vdupq_n_p16"
  - "arm_neon/vld4_dup_f16"
  - "arm_neon/vcls_s16"
  - "arm_neon/vmov_n_u64"
  - "arm_neon/vmla_s32"
  - "arm_neon/vrshl_s16"
  - "arm_neon/vcalt_f32"
  - "arm_neon/int64x2x3_t"
  - "arm_neon/vsub_u8"
  - "arm_neon/vzipq_u8"
  - "arm_neon/vrshrn_n_u64"
  - "arm_neon/vrshlq_s32"
  - "arm_neon/vorr_s64"
  - "arm_neon/vqrshl_s16"
  - "arm_neon/vceqq_u16"
  - "arm_neon/vmulq_n_u16"
  - "arm_neon/vmlaq_u8"
  - "arm_neon/vsri_n_s64"
  - "arm_neon/vld3q_u8"
  - "arm_neon/vld1_dup_s16"
  - "arm_neon/vld1q_s32"
  - "arm_neon/vsri_n_s16"
  - "arm_neon/vshlq_u8"
  - "arm_neon/vsli_n_s64"
  - "arm_neon/vmull_lane_u32"
  - "arm_neon/vshl_s64"
  - "arm_neon/vcreate_s16"
  - "arm_neon/uint8x8x4_t"
  - "arm_neon/vqshrn_n_s32"
  - "arm_neon/vqshlq_u32"
  - "arm_neon/vmlal_n_u32"
  - "arm_neon/vtrnq_s16"
  - "arm_neon/vshr_n_s64"
  - "arm_neon/vst2_u16"
  - "arm_neon/vtrn_s32"
  - "arm_neon/vsubhn_u32"
  - "arm_neon/vbicq_s16"
  - "arm_neon/vsetq_lane_s8"
  - "arm_neon/vrsubhn_s16"
  - "arm_neon/vhsub_u8"
  - "arm_neon/vcleq_s32"
  - "arm_neon/vld4_dup_s8"
  - "arm_neon/vmull_u32"
  - "arm_neon/vrshr_n_s16"
  - "arm_neon/vst1q_lane_s16"
  - "arm_neon/vmlsq_lane_u32"
  - "arm_neon/vnegq_f32"
  - "arm_neon/vmin_s8"
  - "arm_neon/vrev16_p8"
  - "arm_neon/vbic_u8"
  - "arm_neon/vclzq_u16"
  - "arm_neon/vcge_u32"
  - "arm_neon/vget_high_u64"
  - "arm_neon/vabsq_s8"
  - "arm_neon/vhaddq_u16"
  - "arm_neon/vsraq_n_s64"
  - "arm_neon/vld2_u32"
  - "arm_neon/vld2_lane_f32"
  - "arm_neon/vqrshrn_n_u32"
  - "arm_neon/vbslq_s8"
  - "armintr/_CountLeadingZeros64"
  - "arm_neon/vbicq_u8"
  - "arm_neon/vdup_lane_s8"
  - "arm_neon/vpadd_s32"
  - "arm_neon/vld3q_lane_f16"
  - "arm_neon/vaba_u8"
  - "arm_neon/vqshlq_u16"
  - "arm_neon/vst1q_u8"
  - "arm_neon/vst4q_lane_f16"
  - "arm_neon/vshl_n_u16"
  - "armintr/_arm_smladx"
  - "arm_neon/vmla_lane_s16"
  - "arm_neon/vornq_u8"
  - "arm_neon/vqneg_s32"
  - "arm_neon/vadd_s8"
  - "arm_neon/vcle_u32"
  - "arm_neon/vclzq_u8"
  - "arm_neon/vtbx1_u8"
  - "armintr/_CountLeadingOnes64"
  - "armintr/__dsb"
  - "arm_neon/vaddq_u32"
  - "arm_neon/vclsq_s8"
  - "arm_neon/vdup_n_s64"
  - "arm_neon/vmax_s16"
  - "arm_neon/vst2q_u32"
  - "arm_neon/vsetq_lane_s64"
  - "arm_neon/vtst_p8"
  - "arm_neon/vabs_s8"
  - "arm_neon/vqshl_n_s16"
  - "arm_neon/vqrshrn_n_u64"
  - "arm_neon/vaddw_s8"
  - "armintr/_arm_uhadd16"
  - "arm_neon/vsriq_n_p16"
  - "arm_neon/vld4_lane_u32"
  - "arm_neon/vneg_f32"
  - "armintr/_MoveToCoprocessor"
  - "arm_neon/vmvnq_s8"
  - "arm_neon/vld1q_lane_p8"
  - "arm_neon/uint32x2x3_t"
  - "arm_neon/vrshrn_n_u16"
  - "arm_neon/vld3_f16"
  - "arm_neon/vsriq_n_s16"
  - "arm_neon/vshlq_n_s16"
  - "arm_neon/vabal_u8"
  - "arm_neon/vqshluq_n_s16"
  - "arm_neon/vst2_lane_u16"
  - "arm_neon/vbic_s16"
  - "arm_neon/vqshl_n_u64"
  - "arm_neon/vcagt_f32"
  - "arm_neon/vpadalq_s8"
  - "arm_neon/vclz_s32"
  - "arm_neon/vld1_lane_s64"
  - "arm_neon/vget_high_p8"
  - "arm_neon/uint64x1_t"
  - "arm_neon/vextq_s16"
  - "arm_neon/vpadd_s8"
  - "arm_neon/vrsubhn_u64"
  - "arm_neon/vst3q_f16"
  - "arm_neon/vdupq_lane_u16"
  - "arm_neon/vrshrq_n_u64"
  - "arm_neon/vmovq_n_f32"
  - "arm_neon/vld1q_dup_u16"
  - "arm_neon/vshr_n_u16"
  - "arm_neon/uint32x2_t"
  - "armintr/_arm_umull"
  - "arm_neon/vtrnq_u16"
  - "arm_neon/vsetq_lane_u32"
  - "arm_neon/vneg_s8"
  - "arm_neon/vsetq_lane_u8"
  - "arm_neon/vst2q_lane_s16"
  - "arm_neon/vqmovun_s32"
  - "armintr/_arm_usad8"
  - "armintr/_arm_pkhbt"
  - "arm_neon/uint16x4x3_t"
  - "arm_neon/vsra_n_s32"
  - "arm_neon/vqmovun_s64"
  - "arm_neon/vld1q_dup_s8"
  - "arm_neon/vaddhn_s32"
  - "arm_neon/vpmax_f32"
  - "arm_neon/vpadd_u32"
  - "arm_neon/vhsubq_u32"
  - "arm_neon/vqrshrun_n_s32"
  - "arm_neon/vadd_s32"
  - "arm_neon/vclt_s8"
  - "arm_neon/vorrq_s64"
  - "arm_neon/vst4q_f16"
  - "arm_neon/vst1_s32"
  - "arm_neon/vceq_p8"
  - "arm_neon/vsubw_s16"
  - "arm_neon/vgetq_lane_u64"
  - "arm_neon/vmla_n_u32"
  - "arm_neon/vcvtq_f32_s32"
  - "arm_neon/vld1q_u32"
  - "arm_neon/vmax_f32"
  - "armintr/_isunorderedf"
  - "arm_neon/vrshl_u8"
  - "arm_neon/vld4_dup_s64"
  - "arm_neon/vqaddq_u16"
  - "arm_neon/vld4q_lane_f16"
  - "arm_neon/vceqq_p8"
  - "arm_neon/vsubw_u8"
  - "arm_neon/vqmovn_u16"
  - "armintr/_arm_smlsldx"
  - "arm_neon/vcreate_p8"
  - "arm_neon/vqdmull_n_s32"
  - "arm_neon/uint64x2_t"
  - "arm_neon/vmls_s32"
  - "arm_neon/vst3q_f32"
  - "armintr/_arm_bfi"
  - "armintr/_arm_qadd16"
  - "arm_neon/vrshlq_s8"
  - "arm_neon/vget_lane_p16"
  - "arm_neon/vld2_p8"
  - "arm_neon/vld3_lane_u32"
  - "armintr/_MoveFromCoprocessor2"
  - "arm_neon/vqshl_u8"
  - "arm_neon/poly8_t"
  - "arm_neon/vhadd_u16"
  - "arm_neon/vmla_lane_u16"
  - "arm_neon/vshrq_n_u8"
  - "arm_neon/vuzpq_f32"
  - "arm_neon/vmls_lane_f32"
  - "arm_neon/vqneg_s16"
  - "arm_neon/vtrn_p16"
  - "arm_neon/vshrn_n_u32"
  - "arm_neon/vaddhn_u64"
  - "arm_neon/vabal_u32"
  - "arm_neon/vld1q_lane_u32"
  - "arm_neon/vrsraq_n_s32"
  - "arm_neon/vandq_u64"
  - "arm_neon/vqdmull_s32"
  - "arm_neon/vext_s16"
  - "arm_neon/vaddw_s16"
  - "arm_neon/vrev64q_p8"
  - "arm_neon/uint8x8x3_t"
  - "arm_neon/vzip_f32"
  - "armintr/_arm_ssub8"
  - "arm_neon/uint16x4x4_t"
  - "armintr/__swi"
  - "armintr/_arm_smlatb"
  - "arm_neon/vrhaddq_s8"
  - "arm_neon/vpmax_s32"
  - "arm_neon/vqshl_s64"
  - "arm_neon/vrev16q_p8"
  - "arm_neon/vqmovn_u32"
  - "arm_neon/vld1q_f16"
  - "arm_neon/vornq_u64"
  - "arm_neon/vqshlq_n_s16"
  - "arm_neon/vld1_f16"
  - "armintr/_arm_smmlsr"
  - "arm_neon/vshlq_s16"
  - "arm_neon/vsubhn_s16"
  - "arm_neon/vmulq_p8"
  - "arm_neon/vdupq_lane_f32"
  - "armintr/_arm_shadd16"
  - "arm_neon/vornq_s16"
  - "arm_neon/vst1q_lane_u8"
  - "arm_neon/vcaleq_f32"
  - "arm_neon/vst3q_lane_f16"
  - "armintr/_arm_sdiv"
  - "arm_neon/vld2_u16"
  - "arm_neon/vdup_lane_u16"
  - "arm_neon/vst4q_lane_f32"
  - "arm_neon/vdup_n_f32"
  - "arm_neon/vsubq_u8"
  - "arm_neon/vset_lane_p16"
  - "arm_neon/vrsqrte_f32"
  - "arm_neon/vsubl_u8"
  - "arm_neon/vld3q_lane_f32"
  - "arm_neon/vqnegq_s8"
  - "arm_neon/vqmovn_s16"
  - "arm_neon/int16x8x3_t"
  - "arm_neon/veorq_u16"
  - "arm_neon/vqdmulh_n_s16"
  - "arm_neon/vhaddq_u8"
  - "arm_neon/vpadal_u8"
  - "arm_neon/vst2q_s16"
  - "arm_neon/poly16x8x4_t"
  - "arm_neon/int64x2_t"
  - "arm_neon/vmull_s32"
  - "arm_neon/vld4_lane_s32"
  - "arm_neon/vst4q_p8"
  - "arm_neon/vmlal_lane_u16"
  - "arm_neon/vclz_u32"
  - "arm_neon/vsliq_n_s8"
  - "arm_neon/vmls_n_f32"
  - "arm_neon/vmlsl_lane_s16"
  - "arm_neon/vst4q_u32"
  - "arm_neon/vld1q_lane_s16"
  - "arm_neon/vst1q_f32"
  - "arm_neon/vrshr_n_u8"
  - "arm_neon/vst1q_s64"
  - "arm_neon/vbslq_u32"
  - "arm_neon/vset_lane_s8"
  - "arm_neon/vdupq_lane_p16"
  - "arm_neon/vtstq_s16"
  - "arm_neon/vshl_n_s8"
  - "arm_neon/vqrdmulhq_n_s16"
  - "arm_neon/vget_high_f16"
  - "arm_neon/vst4_lane_u32"
  - "arm_neon/vraddhn_s16"
  - "arm_neon/vmlsl_lane_s32"
  - "arm_neon/vld3q_s32"
  - "arm_neon/vsriq_n_u64"
  - "arm_neon/vld4_dup_u8"
  - "arm_neon/vld4q_s8"
  - "arm_neon/vqmovn_s64"
  - "arm_neon/vrev32q_p8"
  - "arm_neon/vsliq_n_p8"
  - "arm_neon/vzipq_s16"
  - "arm_neon/vgetq_lane_s64"
  - "arm_neon/vst4_p16"
  - "arm_neon/vsubq_u16"
  - "arm_neon/vrev64_s32"
  - "armintr/_arm_uhadd8"
  - "arm_neon/vornq_u16"
  - "arm_neon/vst4_lane_s8"
  - "arm_neon/vabd_s32"
  - "arm_neon/vqrdmulhq_s16"
  - "arm_neon/vqshlq_s32"
  - "arm_neon/int64x2x4_t"
  - "arm_neon/vset_lane_u16"
  - "arm_neon/vrsra_n_s32"
  - "arm_neon/vabdl_u16"
  - "arm_neon/vsliq_n_s32"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "cl.exe コンパイラ, 組み込み"
  - "組み込み, ARM"
ms.assetid: d3d7dadd-7bd5-4508-8bff-371a66913e20
caps.latest.revision: 15
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 15
---
# ARM 組み込み
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Visual C\+\+ コンパイラでは、ARM アーキテクチャ上で次の組み込みが使用できるようになります。  ARM の詳細については、ARM Infocenter Web サイトで『[ARM アーキテクチャ リファレンス マニュアル](http://go.microsoft.com/fwlink/p/?LinkId=522049)』および『[ARM Assembler Tools Guide \(ARM アセンブラー ツール ガイド\)](http://go.microsoft.com/fwlink/p/?LinkId=246102)』を参照してください。  
  
##  <a name="top"></a> NEON  
 ARM の NEON ベクター命令セット拡張は、x86 および x64 アーキテクチャのプロセッサに共通する MMX と SSE ベクター命令セットの拡張に類似した単一命令複数データ \(SIMD\) 機能を提供します。  
  
 ヘッダー ファイル `arm_neon.h` に記載されているように、NEON 組み込みはサポートされています。  NEON 組み込みの Visual C\+\+ コンパイラ サポートは、ARM コンパイラのサポートと類似しています。これは、ARM Infocenter サイトの『[ARM Compiler toolchain, Version 4.1 Compiler Reference \(ARM コンパイラ ツールチェーン バージョン 4.1 コンパイラ リファレンス\)](http://go.microsoft.com/fwlink/p/?LinkId=251083)』の「Appendix G \(付録 G\)」に記載されています。  
  
 Visual C\+\+ コンパイラと ARM コンパイラの主な違いは、Visual C\+\+ コンパイラでは `_ex` および `vldX` ベクターのロードおよびストア用命令の `vstX` バリアントが追加される点です。  `_ex` バリアントは、ポインター引数の配置を指定する追加パラメーターを受け取りますが、それ以外は `_ex` の付かない命令と変わりありません。  
  
##  <a name="A"></a> ARM 固有の組み込みのリスト  
  
|\[関数名\]|命令|関数プロトタイプ|  
|-------------|--------|--------------|  
|\_arm\_smlal|SMLAL|\_\_int64 \_arm\_smlal\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_umlal|UMLAL|unsigned \_\_int64 \_arm\_umlal\(unsigned \_\_int64 \_RdHiLo, unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_clz|CLZ|unsigned int \_arm\_clz\(unsigned int \_Rm\)|  
|\_arm\_qadd|QADD|int \_arm\_qadd\(int \_Rm, int \_Rn\)|  
|\_arm\_qdadd|QDADD|int \_arm\_qdadd\(int \_Rm, int \_Rn\)|  
|\_arm\_qdsub|QDSUB|int \_arm\_qdsub\(int \_Rm, int \_Rn\)|  
|\_arm\_qsub|QSUB|int \_arm\_qsub\(int \_Rm, int \_Rn\)|  
|\_arm\_smlabb|SMLABB|int \_arm\_smlabb\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smlabt|SMLABT|int \_arm\_smlabt\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smlatb|SMLATB|int \_arm\_smlatb\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smlatt|SMLATT|int \_arm\_smlatt\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smlalbb|SMLALBB|\_\_int64 \_arm\_smlalbb\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smlalbt|SMLALBT|\_\_int64 \_arm\_smlalbt\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smlaltb|SMLALTB|\_\_int64 \_arm\_smlaltb\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smlaltt|SMLALTT|\_\_int64 \_arm\_smlaltt\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smlawb|SMLAWB|int \_arm\_smlawb\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smlawt|SMLAWT|int \_arm\_smlawt\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smulbb|SMULBB|int \_arm\_smulbb\(int \_Rn, int \_Rm\)|  
|\_arm\_smulbt|SMULBT|int \_arm\_smulbt\(int \_Rn, int \_Rm\)|  
|\_arm\_smultb|SMULTB|int \_arm\_smultb\(int \_Rn, int \_Rm\)|  
|\_arm\_smultt|SMULTT|int \_arm\_smultt\(int \_Rn, int \_Rm\)|  
|\_arm\_smulwb|SMULWB|int \_arm\_smulwb\(int \_Rn, int \_Rm\)|  
|\_arm\_smulwt|SMULWT|int \_arm\_smulwt\(int \_Rn, int \_Rm\)|  
|\_arm\_sadd16|SADD16|int \_arm\_sadd16\(int \_Rn, int \_Rm\)|  
|\_arm\_sadd8|SADD8|int \_arm\_sadd8\(int \_Rn, int \_Rm\)|  
|\_arm\_sasx|SASX|int \_arm\_sasx\(int \_Rn, int \_Rm\)|  
|\_arm\_ssax|SSAX|int \_arm\_ssax\(int \_Rn, int \_Rm\)|  
|\_arm\_ssub16|SSUB16|int \_arm\_ssub16\(int \_Rn, int \_Rm\)|  
|\_arm\_ssub8|SSUB8|int \_arm\_ssub8\(int \_Rn, int \_Rm\)|  
|\_arm\_shadd16|SHADD16|int \_arm\_shadd16\(int \_Rn, int \_Rm\)|  
|\_arm\_shadd8|SHADD8|int \_arm\_shadd8\(int \_Rn, int \_Rm\)|  
|\_arm\_shasx|SHASX|int \_arm\_shasx\(int \_Rn, int \_Rm\)|  
|\_arm\_shsax|SHSAX|int \_arm\_shsax\(int \_Rn, int \_Rm\)|  
|\_arm\_shsub16|SHSUB16|int \_arm\_shsub16\(int \_Rn, int \_Rm\)|  
|\_arm\_shsub8|SHSUB8|int \_arm\_shsub8\(int \_Rn, int \_Rm\)|  
|\_arm\_qadd16|QADD16|int \_arm\_qadd16\(int \_Rn, int \_Rm\)|  
|\_arm\_qadd8|QADD8|int \_arm\_qadd8\(int \_Rn, int \_Rm\)|  
|\_arm\_qasx|QASX|int \_arm\_qasx\(int \_Rn, int \_Rm\)|  
|\_arm\_qsax|QSAX|int \_arm\_qsax\(int \_Rn, int \_Rm\)|  
|\_arm\_qsub16|QSUB16|int \_arm\_qsub16\(int \_Rn, int \_Rm\)|  
|\_arm\_qsub8|QSUB8|int \_arm\_qsub8\(int \_Rn, int \_Rm\)|  
|\_arm\_uadd16|UADD16|unsigned int \_arm\_uadd16\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uadd8|UADD8|unsigned int \_arm\_uadd8\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uasx|UASX|unsigned int \_arm\_uasx\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_usax|USAX|unsigned int \_arm\_usax\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_usub16|USUB16|unsigned int \_arm\_usub16\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_usub8|USUB8|unsigned int \_arm\_usub8\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uhadd16|UHADD16|unsigned int \_arm\_uhadd16\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uhadd8|UHADD8|unsigned int \_arm\_uhadd8\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uhasx|UHASX|unsigned int \_arm\_uhasx\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uhsax|UHSAX|unsigned int \_arm\_uhsax\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uhsub16|UHSUB16|unsigned int \_arm\_uhsub16\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uhsub8|UHSUB8|unsigned int \_arm\_uhsub8\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uqadd16|UQADD16|unsigned int \_arm\_uqadd16\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uqadd8|UQADD8|unsigned int \_arm\_uqadd8\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uqasx|UQASX|unsigned int \_arm\_uqasx\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uqsax|UQSAX|unsigned int \_arm\_uqsax\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uqsub16|UQSUB16|unsigned int \_arm\_uqsub16\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_uqsub8|UQSUB8|unsigned int \_arm\_uqsub8\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_sxtab|SXTAB|int \_arm\_sxtab\(int \_Rn, int \_Rm, unsigned int \_Rotation\)|  
|\_arm\_sxtab16|SXTAB16|int \_arm\_sxtab16\(int \_Rn, int \_Rm, unsigned int \_Rotation\)|  
|\_arm\_sxtah|SXTAH|int \_arm\_sxtah\(int \_Rn, int \_Rm, unsigned int \_Rotation\)|  
|\_arm\_uxtab|UXTAB|unsigned int \_arm\_uxtab\(unsigned int \_Rn, unsigned int \_Rm, unsigned int \_Rotation\)|  
|\_arm\_uxtab16|UXTAB16|unsigned int \_arm\_uxta16b\(unsigned int \_Rn, unsigned int \_Rm, unsigned int \_Rotation\)|  
|\_arm\_uxtah|UXTAH|unsigned int \_arm\_uxtah\(unsigned int \_Rn, unsigned int \_Rm, unsigned int \_Rotation\)|  
|\_arm\_sxtb|SXTB|int \_arm\_sxtb\(int \_Rn, unsigned int \_Rotation\)|  
|\_arm\_sxtb16|SXTB16|int \_arm\_sxtb16\(int \_Rn, unsigned int \_Rotation\)|  
|\_arm\_sxth|SXTH|int \_arm\_sxth\(int \_Rn, unsigned int \_Rotation\)|  
|\_arm\_uxtb|UXTB|unsigned int \_arm\_uxtb\(unsigned int \_Rn, unsigned int \_Rotation\)|  
|\_arm\_uxtb16|UXTB16|unsigned int \_arm\_uxtb16\(unsigned int \_Rn, unsigned int \_Rotation\)|  
|\_arm\_uxth|UXTH|unsigned int \_arm\_uxth\(unsigned int \_Rn, unsigned int \_Rotation\)|  
|\_arm\_pkhbt|PKHBT|int \_arm\_pkhbt\(int \_Rn, int \_Rm, unsigned int \_Lsl\_imm\)|  
|\_arm\_pkhtb|PKHTB|int \_arm\_pkhtb\(int \_Rn, int \_Rm, unsigned int \_Asr\_imm\)|  
|\_arm\_usad8|USAD8|unsigned int \_arm\_usad8\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_usada8|USADA8|unsigned int \_arm\_usada8\(unsigned int \_Rn, unsigned int \_Rm, unsigned int \_Ra\)|  
|\_arm\_ssat|SSAT|int \_arm\_ssat\(unsigned int \_Sat\_imm, \_int \_Rn, \_ARMINTR\_SHIFT\_T \_Shift\_type, unsigned int \_Shift\_imm\)|  
|\_arm\_usat|USAT|int \_arm\_usat\(unsigned int \_Sat\_imm, \_int \_Rn, \_ARMINTR\_SHIFT\_T \_Shift\_type, unsigned int \_Shift\_imm\)|  
|\_arm\_ssat16|SSAT16|int \_arm\_ssat16\(unsigned int \_Sat\_imm, \_int \_Rn\)|  
|\_arm\_usat16|USAT16|int \_arm\_usat16\(unsigned int \_Sat\_imm, \_int \_Rn\)|  
|\_arm\_rev|REV|unsigned int \_arm\_rev\(unsigned int \_Rm\)|  
|\_arm\_rev16|REV16|unsigned int \_arm\_rev16\(unsigned int \_Rm\)|  
|\_arm\_revsh|REVSH|unsigned int \_arm\_revsh\(unsigned int \_Rm\)|  
|\_arm\_smlad|SMLAD|int \_arm\_smlad\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smladx|SMLADX|int \_arm\_smladx\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smlsd|SMLSD|int \_arm\_smlsd\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smlsdx|SMLSDX|int \_arm\_smlsdx\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smmla|SMMLA|int \_arm\_smmla\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smmlar|SMMLAR|int \_arm\_smmlar\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smmls|SMMLS|int \_arm\_smmls\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smmlsr|SMMLSR|int \_arm\_smmlsr\(int \_Rn, int \_Rm, int \_Ra\)|  
|\_arm\_smmul|SMMUL|int \_arm\_smmul\(int \_Rn, int \_Rm\)|  
|\_arm\_smmulr|SMMULR|int \_arm\_smmulr\(int \_Rn, int \_Rm\)|  
|\_arm\_smlald|SMLALD|\_\_int64 \_arm\_smlald\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smlaldx|SMLALDX|\_\_int64 \_arm\_smlaldx\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smlsld|SMLSLD|\_\_int64 \_arm\_smlsld\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smlsldx|SMLSLDX|\_\_int64 \_arm\_smlsldx\(\_\_int64 \_RdHiLo, int \_Rn, int \_Rm\)|  
|\_arm\_smuad|SMUAD|int \_arm\_smuad\(int \_Rn, int \_Rm\)|  
|\_arm\_smuadx|SMUADX|int \_arm\_muadxs\(int \_Rn, int \_Rm\)|  
|\_arm\_smusd|SMUSD|int \_arm\_smusd\(int \_Rn, int \_Rm\)|  
|\_arm\_smusdx|SMUSDX|int \_arm\_smusdx\(int \_Rn, int \_Rm\)|  
|\_arm\_smull|SMULL|\_\_int64 \_arm\_smull\(int \_Rn, int \_Rm\)|  
|\_arm\_umull|UMULL|unsigned \_\_int64 \_arm\_umull\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_umaal|UMAAL|unsigned \_\_int64 \_arm\_umaal\(unsigned int \_RdLo, unsigned int \_RdHi, unsigned int \_Rn, unsigned int \_Rm\)|  
|\_arm\_bfc|BFC|unsigned int \_arm\_bfc\(unsigned int \_Rd, unsigned int \_Lsb, unsigned int \_Width\)|  
|\_arm\_bfi|BFI|unsigned int \_arm\_bfi\(unsigned int \_Rd, unsigned int \_Rn, unsigned int \_Lsb, unsigned int \_Width\)|  
|\_arm\_rbit|RBIT|unsigned int \_arm\_rbit\(unsigned int \_Rm\)|  
|\_arm\_sbfx|SBFX|int \_arm\_sbfx\(int \_Rn, unsigned int \_Lsb, unsigned int \_Width\)|  
|\_arm\_ubfx|UBFX|unsigned int \_arm\_ubfx\(unsigned int \_Rn, unsigned int \_Lsb, unsigned int \_Width\)|  
|\_arm\_sdiv|SDIV|int \_arm\_sdiv\(int \_Rn, int \_Rm\)|  
|\_arm\_udiv|UDIV|unsigned int \_arm\_udiv\(unsigned int \_Rn, unsigned int \_Rm\)|  
|\_\_cps|CPS|void \_\_cps\(unsigned int \_Ops, unsigned int \_Flags, unsigned int \_Mode\)|  
|\_\_dmb|DMB|void \_\_dmb\(unsigned int `_Type`\)<br /><br /> 命令ストリームにメモリ バリア操作を挿入します。  パラメーター `_Type` で、バリアによって適用される制限の種類を指定します。<br /><br /> 強制できる制限の種類の詳細は、「[メモリ バリアの制限](#BarrierRestrictions)」を参照してください。|  
|\_\_dsb|DSB|void \_\_dsb\(unsigned int \_Type\)<br /><br /> 命令ストリームにメモリ バリア操作を挿入します。  パラメーター `_Type` で、バリアによって適用される制限の種類を指定します。<br /><br /> 強制できる制限の種類の詳細は、「[メモリ バリアの制限](#BarrierRestrictions)」を参照してください。|  
|\_\_isb|ISB|void \_\_isb\(unsigned int \_Type\)<br /><br /> 命令ストリームにメモリ バリア操作を挿入します。  パラメーター `_Type` で、バリアによって適用される制限の種類を指定します。<br /><br /> 強制できる制限の種類の詳細は、「[メモリ バリアの制限](#BarrierRestrictions)」を参照してください。|  
|\_\_emit||void \_\_emit\(unsigned \_\_int32 opcode\)<br /><br /> コンパイラから出力される命令ストリームに、指定された命令を挿入します。<br /><br /> `opcode` の値は、コンパイル時に既知の定数式である必要があります。  命令語のサイズは 16 ビットであり、`opcode` の最上位 16 ビットは無視されます。<br /><br /> コンパイラは `opcode` の内容を解釈しようとせず、挿入された命令を実行する前の CPU またはメモリの状態は保証されません。<br /><br /> コンパイラは、挿入された命令を実行した後に CPU とメモリの状態が変更されていないことを前提としています。  したがって、状態を変更する命令は、コンパイラにより生成される通常のコードに好ましくない影響を与えることがあります。<br /><br /> このため、`emit` を使用するのは、コンパイラが正常に処理できない CPU の状態 \(コプロセッサの状態など\) に影響を与える命令を挿入する場合か、次を使用して宣言されている関数を実装する場合のみとします。`declspec(naked)`|  
|\_\_hvc|HVC|unsigned int \_\_hvc\(unsigned int, ...\)|  
|\_\_iso\_volatile\_load16||\_\_int16 \_\_iso\_volatile\_load16\(const volatile \_\_int16 \*\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_iso\_volatile\_load32||\_\_int32 \_\_iso\_volatile\_load32\(const volatile \_\_int32 \*\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_iso\_volatile\_load64||\_\_int64 \_\_iso\_volatile\_load64\(const volatile \_\_int64 \*\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_iso\_volatile\_load8||\_\_int8 \_\_iso\_volatile\_load8\(const volatile \_\_int8 \*\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_iso\_volatile\_store16||void \_\_iso\_volatile\_store16\(volatile \_\_int16 \*, \_\_int16\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_iso\_volatile\_store32||void \_\_iso\_volatile\_store32\(volatile \_\_int32 \*, \_\_int32\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_iso\_volatile\_store64||void \_\_iso\_volatile\_store64\(volatile \_\_int64 \*, \_\_int64\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_iso\_volatile\_store8||void \_\_iso\_volatile\_store8\(volatile \_\_int8 \*, \_\_int8\)<br /><br /> 詳細については、「[__iso_volatile_load/store 組み込み](#IsoVolatileLoadStore)」を参照してください。|  
|\_\_ldrexd|LDREXD|\_\_int64 \_\_ldrexd\(const volatile \_\_int64 \*\)|  
|\_\_prefetch|PLD|void \_\_cdecl \_\_prefetch\(const void \*\)<br /><br /> 指定したアドレス、またはその付近のアドレスのメモリに間もなくアクセスする可能性があるという `PLD` メモリ ヒントをシステムに提供します。  システムによっては、実行時のパフォーマンスを向上させるために、そのメモリへのアクセス パターンを最適化する場合があります。  ただし、C\+\+ 言語側からすると、この関数には目に見える効果がなく、何も実行しないことがあります。|  
|\_\_rdpmccntr64||unsigned \_\_int64 \_\_rdpmccntr64\(void\)|  
|\_\_sev|SEV|void \_\_sev\(void\)|  
|\_\_static\_assert||void \_\_static\_assert\(int, const char \*\)|  
|\_\_swi|SVC|unsigned int \_\_swi\(unsigned int, ...\)|  
|\_\_trap|BKPT|int \_\_trap\(int, ...\)|  
|\_\_wfe|WFE|void \_\_wfe\(void\)|  
|\_\_wfi|WFI|void \_\_wfi\(void\)|  
|\_AddSatInt|QADD|int \_AddSatInt\(int, int\)|  
|\_CopyDoubleFromInt64||double \_CopyDoubleFromInt64\(\_\_int64\)|  
|\_CopyFloatFromInt32||float \_CopyFloatFromInt32\(\_\_int32\)|  
|\_CopyInt32FromFloat||\_\_int32 \_CopyInt32FromFloat\(float\)|  
|\_CopyInt64FromDouble||\_\_int64 \_CopyInt64FromDouble\(double\)|  
|\_CountLeadingOnes||unsigned int \_CountLeadingOnes\(unsigned long\)|  
|\_CountLeadingOnes64||unsigned int \_CountLeadingOnes64\(unsigned \_\_int64\)|  
|\_CountLeadingSigns||unsigned int \_CountLeadingSigns\(long\)|  
|\_CountLeadingSigns64||unsigned int \_CountLeadingSigns64\(\_\_int64\)|  
|\_CountLeadingZeros||unsigned int \_CountLeadingZeros\(unsigned long\)|  
|\_CountLeadingZeros64||unsigned int \_CountLeadingZeros64\(unsigned \_\_int64\)|  
|\_CountOneBits||unsigned int \_CountOneBits\(unsigned long\)|  
|\_CountOneBits64||unsigned int \_CountOneBits64\(unsigned \_\_int64\)|  
|\_DAddSatInt|QDADD|int \_DAddSatInt\(int, int\)|  
|\_DSubSatInt|QDSUB|int \_DSubSatInt\(int, int\)|  
|\_isunordered||int \_isunordered\(double, double\)|  
|\_isunorderedf||int \_isunorderedf\(float, float\)|  
|\_MoveFromCoprocessor|MRC|unsigned int \_MoveFromCoprocessor\(unsigned int, unsigned int, unsigned int, unsigned int, unsigned int\)<br /><br /> コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  詳細については、「[_MoveFromCoprocessor、_MoveFromCoprocessor2](#MoveFromCo)」を参照してください。|  
|\_MoveFromCoprocessor2|MRC2|unsigned int \_MoveFromCoprocessor2\(unsigned int, unsigned int, unsigned int, unsigned int, unsigned int\)<br /><br /> コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  詳細については、「[_MoveFromCoprocessor、_MoveFromCoprocessor2](#MoveFromCo)」を参照してください。|  
|\_MoveFromCoprocessor64|MRRC|unsigned \_\_int64 \_MoveFromCoprocessor64\(unsigned int, unsigned int, unsigned int\)<br /><br /> コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  詳細については、「[_MoveFromCoprocessor64](#MoveFromCo64)」を参照してください。|  
|\_MoveToCoprocessor|MCR|void \_MoveToCoprocessor\(unsigned int, unsigned int, unsigned int, unsigned int, unsigned int, unsigned int\)<br /><br /> コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  詳細については、「[_MoveToCoprocessor、_MoveToCoprocessor2](#MoveToCo)」を参照してください。|  
|\_MoveToCoprocessor2|MCR2|void \_MoveToCoprocessor2\(unsigned int, unsigned int, unsigned int, unsigned int, unsigned int, unsigned int\)<br /><br /> コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  詳細については、「[_MoveToCoprocessor、_MoveToCoprocessor2](#MoveToCo)」を参照してください。|  
|\_MoveToCoprocessor64|MCRR|void \_MoveToCoprocessor64\(unsigned \_\_int64, unsigned int, unsigned int, unsigned int\)<br /><br /> コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  詳細については、「[_MoveToCoprocessor64](#MoveToCo64)」を参照してください。|  
|\_MulHigh||long \_MulHigh\(long, long\)|  
|\_MulUnsignedHigh||unsigned long \_MulUnsignedHigh\(unsigned long, unsigned long\)|  
|\_ReadBankedReg|MRS|int \_ReadBankedReg\(int \_Reg\)|  
|\_ReadStatusReg|MRS|int \_ReadStatusReg\(int\)|  
|\_SubSatInt|QSUB|int \_SubSatInt\(int, int\)|  
|\_WriteBankedReg|MSR|void \_WriteBankedReg\(int \_Value, int \_Reg\)|  
|\_WriteStatusReg|MSR|void \_WriteStatusReg\(int, int, int\)|  
  
 \[[NEON](#top)\]  
  
###  <a name="BarrierRestrictions"></a> メモリ バリアの制限  
 組み込み関数 `__dmb` \(データ メモリ バリア\)、`__dsb` \(データ同期バリア\)、および `__isb` \(命令同期バリア\) では、定義済みの次の値を使用して、操作の影響を受ける共有ドメインおよびアクセスの種類の観点からメモリ バリアの制限を指定します。  
  
|制限値|説明|  
|---------|--------|  
|\_ARM\_BARRIER\_SY|システム全体、読み取りと書き込み。|  
|\_ARM\_BARRIER\_ST|システム全体、書き込みのみ。|  
|\_ARM\_BARRIER\_ISH|内部共有可能、読み取りと書き込み。|  
|\_ARM\_BARRIER\_ISHST|内部共有可能、書き込みのみ。|  
|\_ARM\_BARRIER\_NSH|共有不可、読み取りと書き込み。|  
|\_ARM\_BARRIER\_NSHST|共有不可、書き込みのみ。|  
|\_ARM\_BARRIER\_OSH|外部共有可能、読み取りと書き込み。|  
|\_ARM\_BARRIER\_OSHST|外部共有可能、書き込みのみ。|  
  
 組み込みが `__isb` の場合、現在有効な制限は \_ARM\_BARRIER\_SY のみです。その他のすべての値は、アーキテクチャによって予約されています。  
  
###  <a name="IsoVolatileLoadStore"></a> \_\_iso\_volatile\_load\/store 組み込み  
 これらの組み込み関数では、コンパイラによる最適化の対象にならないロードとストアが明示的に実行されます。  
  
```  
__int16 __iso_volatile_load16(const volatile __int16 * Location)  
__int32 __iso_volatile_load32(const volatile __int32 * Location)  
__int64 __iso_volatile_load64(const volatile __int64 * Location)  
__int8 __iso_volatile_load8(const volatile __int8 * Location)  
  
void __iso_volatile_store16(volatile __int16 * Location, __int16 Value)  
void __iso_volatile_store32(volatile __int32 * Location, __int32 Value)  
void __iso_volatile_store64(volatile __int64 * Location, __int64 Value)  
void __iso_volatile_store8(volatile __int8 * Location, __int8 Value)  
  
```  
  
 **パラメーター**  
  
 `Location`  
 読み取る、または書き込むメモリ位置のアドレスです。  
  
 `Value` \(ストア用組み込みのみ\)  
 指定されたメモリ位置に書き込む値です。  
  
 **戻り値 \(ロード用組み込みのみ\)**  
  
 `Location` で指定されたメモリ位置の値。  
  
 **コメント**  
  
 組み込みの `__iso_volatile_load8/16/32/64` および `__iso_volatile_store8/16/32/64` を使用すると、コンパイラによる最適化の対象にはならないメモリ アクセスを明示的に実行することができます。  コンパイラはこれらの操作の相対順序を削除、合成、または変更できませんが、暗黙的なハードウェア メモリ バリアを生成しません。  したがって、ハードウェアでも複数のスレッド間で観察可能なメモリ アクセスの順序が変更される場合があります。  具体的には、これらの組み込みは、**\/volatile:iso** でコンパイルされる次の式と同等です。  
  
```  
int a = __iso_volatile_load32(p);    // equivalent to: int a = *(const volatile __int32*)p;   
__iso_volatile_store32(p, a);        // equivalent to: *(volatile __int32*)p = a;  
  
```  
  
 組み込みは、volatile 変数を格納する volatile ポインターを受け取ることに注意してください。  ただし、volatile ポインターを引数として使用するための要件や推奨事項はありません。これらの操作のセマンティクスは、volatile ではない通常の型を使用する場合とまったく同じです。  
  
 **\/volatile:iso** コマンド ライン引数の詳細については、「[\/volatile \(volatile キーワードの解釈を\)](../build/reference/volatile-volatile-keyword-interpretation.md)」を参照してください。  
  
###  <a name="MoveFromCo"></a> \_MoveFromCoprocessor、\_MoveFromCoprocessor2  
 これらの組み込み関数は、コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  
  
```  
int _MoveFromCoprocessor(  
      unsigned int coproc,  
      unsigned int opcode1,  
      unsigned int crn,  
      unsigned int crm,  
      unsigned int opcode2  
);  
  
int _MoveFromCoprocessor2(  
      unsigned int coproc,  
      unsigned int opcode1,  
      unsigned int crn,  
      unsigned int crm,  
      unsigned int opcode2  
);  
  
```  
  
 **パラメーター**  
  
 `coproc`  
 コプロセッサ番号 \(範囲は 0 ～ 15\)。  
  
 `opcode1`  
 コプロセッサ固有のオペコード \(範囲は 0 ～ 7\)。  
  
 `crn`  
 コプロセッサのレジスタ番号 \(範囲は 0 ～ 15\)。これは、命令に対する最初のオペランドを指定します。  
  
 `crm`  
 コプロセッサのレジスタ番号 \(範囲は 0 ～ 15\)。これは、追加のソースまたはターゲットのオペランドを指定します。  
  
 `opcode2`  
 コプロセッサ固有の追加オペコード \(範囲は 0 ～ 7\)。  
  
 **戻り値**  
  
 コプロセッサから読み取られる値。  
  
 **コメント**  
  
 この組み込みの 5 つのすべてのパラメーターの値は、コンパイル時に既知の定数式である必要があります。  
  
 `_MoveFromCoprocessor` は MRC 命令を使用し、`_MoveFromCoprocessor2` は MRC2 を使用します。  パラメーターは、命令語に直接エンコードされたビットフィールドに対応します。  パラメーターの解釈は、コプロセッサに依存しています。  詳細については、対象のコプロセッサのマニュアルを参照してください。  
  
###  <a name="MoveFromCo64"></a> \_MoveFromCoprocessor64  
 コプロセッサのデータ転送命令を使用して、ARM コプロセッサからデータを読み取ります。  
  
```  
unsigned __int64 _MoveFromCoprocessor64(  
      unsigned int coproc,  
      unsigned int opcode1,  
      unsigned int crm,  
);  
  
```  
  
 **パラメーター**  
  
 `coproc`  
 コプロセッサ番号 \(範囲は 0 ～ 15\)。  
  
 `opcode1`  
 コプロセッサ固有のオペコード \(範囲は 0 ～ 15\)。  
  
 `crm`  
 コプロセッサのレジスタ番号 \(範囲は 0 ～ 15\)。これは、追加のソースまたはターゲットのオペランドを指定します。  
  
 **戻り値**  
  
 コプロセッサから読み取られる値。  
  
 **コメント**  
  
 この組み込みの 3 つのすべてのパラメーターの値は、コンパイル時に既知の定数式である必要があります。  
  
 `_MoveFromCoprocessor64` は MRRC 命令を使用します。  パラメーターは、命令語に直接エンコードされたビットフィールドに対応します。  パラメーターの解釈は、コプロセッサに依存しています。  詳細については、対象のコプロセッサのマニュアルを参照してください。  
  
###  <a name="MoveToCo"></a> \_MoveToCoprocessor、\_MoveToCoprocessor2  
 これらの組み込み関数は、コプロセッサのデータ転送命令を使用して、ARM コプロセッサにデータを書き込みます。  
  
```  
void _MoveToCoprocessor(  
      unsigned int value,  
      unsigned int coproc,  
      unsigned int opcode1,  
      unsigned int crn,  
      unsigned int crm,  
      unsigned int opcode2  
);  
  
void _MoveToCoprocessor2(  
      unsigned int value,  
      unsigned int coproc,  
      unsigned int opcode1,  
      unsigned int crn,  
      unsigned int crm,  
      unsigned int opcode2  
);  
  
```  
  
 **パラメーター**  
  
 `value`  
 コプロセッサに書き込まれる値。  
  
 `coproc`  
 コプロセッサ番号 \(範囲は 0 ～ 15\)。  
  
 `opcode1`  
 コプロセッサ固有のオペコード \(範囲は 0 ～ 7\)。  
  
 `crn`  
 コプロセッサのレジスタ番号 \(範囲は 0 ～ 15\)。これは、命令に対する最初のオペランドを指定します。  
  
 `crm`  
 コプロセッサのレジスタ番号 \(範囲は 0 ～ 15\)。これは、追加のソースまたはターゲットのオペランドを指定します。  
  
 `opcode2`  
 コプロセッサ固有の追加オペコード \(範囲は 0 ～ 7\)。  
  
 **戻り値**  
  
 なし。  
  
 **コメント**  
  
 この組み込みの `coproc`、`opcode1`、`crn`、`crm`、および `opcode2` の各パラメーターの値は、コンパイル時に既知の定数式である必要があります。  
  
 `_MoveToCoprocessor` は MCR 命令を使用し、`_MoveToCoprocessor2` は MCR2 を使用します。  パラメーターは、命令語に直接エンコードされたビットフィールドに対応します。  パラメーターの解釈は、コプロセッサに依存しています。  詳細については、対象のコプロセッサのマニュアルを参照してください。  
  
###  <a name="MoveToCo64"></a> \_MoveToCoprocessor64  
 これらの組み込み関数は、コプロセッサのデータ転送命令を使用して、ARM コプロセッサにデータを書き込みます。  
  
```  
void _MoveFromCoprocessor64(  
      unsigned __int64 value,  
      unsigned int coproc,  
      unsigned int opcode1,  
      unsigned int crm,  
);  
  
```  
  
 **パラメーター**  
  
 `coproc`  
 コプロセッサ番号 \(範囲は 0 ～ 15\)。  
  
 `opcode1`  
 コプロセッサ固有のオペコード \(範囲は 0 ～ 15\)。  
  
 `crm`  
 コプロセッサのレジスタ番号 \(範囲は 0 ～ 15\)。これは、追加のソースまたはターゲットのオペランドを指定します。  
  
 **戻り値**  
  
 なし。  
  
 **コメント**  
  
 この組み込みの `coproc`、`opcode1`、および `crm` の各パラメーターの値は、コンパイル時に既知の定数式である必要があります。  
  
 `_MoveFromCoprocessor64` は MCRR 命令を使用します。  パラメーターは、命令語に直接エンコードされたビットフィールドに対応します。  パラメーターの解釈は、コプロセッサに依存しています。  詳細については、対象のコプロセッサのマニュアルを参照してください。  
  
##  <a name="I"></a> 他のアーキテクチャの組み込みの ARM サポート  
 次の表は、ARM プラットフォームでサポートされている他のアーキテクチャの組み込みを示しています。  ARM の組み込みの動作が他のハードウェア アーキテクチャの動作と異なる場合は、さらに詳細な情報がメモに記載されています。  
  
|\[関数名\]|関数プロトタイプ|  
|-------------|--------------|  
|\_\_assume|void \_\_assume\(int\)|  
|\_\_code\_seg|void \_\_code\_seg\(const char \*\)|  
|\_\_debugbreak|void \_\_cdecl \_\_debugbreak\(void\)|  
|\_\_fastfail|\_\_declspec\(noreturn\) void \_\_fastfail\(unsigned int\)|  
|\_\_nop|void \_\_nop\(void\) **Note:**  ARM プラットフォームでは、ターゲット アーキテクチャで NOP 命令が実装されている場合、この関数によって同じ命令が生成されます。実装されていない場合は、プログラムまたは CPU の状態を変更しない、代わりの命令が生成されます \(`MOV r8, r8` など\)。  これは、他のハードウェア アーキテクチャの \_\_nop 組み込みと機能的には同等です。 プログラムまたは CPU の状態に影響がない命令は最適化の手法としてターゲット アーキテクチャで無視される場合があるため、命令は必ずしも CPU サイクルを消費しません。  したがって、CPU の動作について確信がない限りは、コード シーケンスの実行時間を操作する \_\_nop 組み込みを使用しないでください。  代わりに、\_\_nop 組み込みを使用して、特定の 32 ビット境界アドレスに次の命令を配置することができます。|  
|\_\_yield|void \_\_yield\(void\) **Note:**  ARM プラットフォームでは、この関数によって YIELD 命令が生成されます。この命令は、プログラムに悪い影響を与えることなく一時的に実行を中断できるタスク \(スピンロックなど\) を、スレッドが実行していることを示します。  これにより、CPU が実行サイクル中に他のタスクを実行できるようになり、実行サイクルが浪費されなくなります。|  
|\_AddressOfReturnAddress|void \* \_AddressOfReturnAddress\(void\)|  
|\_BitScanForward|unsigned char \_BitScanForward\(unsigned long \* \_Index, unsigned long \_Mask\)|  
|\_BitScanReverse|unsigned char \_BitScanReverse\(unsigned long \* \_Index, unsigned long \_Mask\)|  
|\_bittest|unsigned char \_bittest\(long const \*, long\)|  
|\_bittestandcomplement|unsigned char \_bittestandcomplement\(long \*, long\)|  
|\_bittestandreset|unsigned char \_bittestandreset\(long \*, long\)|  
|\_bittestandset|unsigned char \_bittestandset\(long \*, long\)|  
|\_byteswap\_uint64|unsigned \_\_int64 \_\_cdecl \_byteswap\_uint64\(unsigned \_\_int64\)|  
|\_byteswap\_ulong|unsigned long \_\_cdecl \_byteswap\_ulong\(unsigned long\)|  
|\_byteswap\_ushort|unsigned short \_\_cdecl \_byteswap\_ushort\(unsigned short\)|  
|\_disable|void \_\_cdecl \_disable\(void\) **Note:**  ARM プラットフォームでは、この関数によって CPSID 命令が生成されます。これは、組み込みとしてのみ使用できます。|  
|\_enable|void \_\_cdecl \_enable\(void\) **Note:**  ARM プラットフォームでは、この関数によって CPSIE 命令が生成されます。これは、組み込みとして使用できます。|  
|\_lrotl|unsigned long \_\_cdecl \_lrotl\(unsigned long, int\)|  
|\_lrotr|unsigned long \_\_cdecl \_lrotr\(unsigned long, int\)|  
|\_ReadBarrier|void \_ReadBarrier\(void\)|  
|\_ReadWriteBarrier|void \_ReadWriteBarrier\(void\)|  
|\_ReturnAddress|void \* \_ReturnAddress\(void\)|  
|\_rotl|unsigned int \_\_cdecl \_rotl\(unsigned int \_Value, int \_Shift\)|  
|\_rotl16|unsigned short \_rotl16\(unsigned short \_Value, unsigned char \_Shift\)|  
|\_rotl64|unsigned \_\_int64 \_\_cdecl \_rotl64\(unsigned \_\_int64 \_Value, int \_Shift\)|  
|\_rotl8|unsigned char \_rotl8\(unsigned char \_Value, unsigned char \_Shift\)|  
|\_rotr|unsigned int \_\_cdecl \_rotr\(unsigned int \_Value, int \_Shift\)|  
|\_rotr16|unsigned short \_rotr16\(unsigned short \_Value, unsigned char \_Shift\)|  
|\_rotr64|unsigned \_\_int64 \_\_cdecl \_rotr64\(unsigned \_\_int64 \_Value, int \_Shift\)|  
|\_rotr8|unsigned char \_rotr8\(unsigned char \_Value, unsigned char \_Shift\)|  
|\_setjmpex|int \_\_cdecl \_setjmpex\(jmp\_buf\)|  
|\_WriteBarrier|void \_WriteBarrier\(void\)|  
  
 \[[NEON](#top)\]  
  
## インタロックされた組み込み  
 インタロックされた組み込みは、アトミックな読み取り\/変更\/書き込み操作を実行するときに使用する一連の組み込みです。  一部の組み込みは、すべてのプラットフォームに共通です。  この組み込みは数が多いため、ここではその 1 つ 1 つをリストに示しますが、その定義のほとんどは重複しているため、概要で考える方が簡単です。  組み込みの名前から、その具体的な動作を推測できます。  
  
 次の表は、bittest 以外のインタロック組み込みについて、ARM サポートの概要を示しています。  テーブル内の各セルで、行の一番左のセルにある操作名と、列の一番上にある型名を `_Interlocked` の最後に付け加えると、組み込みの名前になります。  たとえば、`Xor` 行と **8** 列の交点のセルは `_InterlockedXor8` に対応し、これは完全にサポートされています。  サポートされているほとんどの関数には、オプションのサフィックス `_acq`、`_rel`、および `_nf` が用意されています。  `_acq` サフィックスは "取得" のセマンティクスを示し、`_rel` サフィックスは "解放" のセマンティクスを示します。  `_nf` \("フェンスなし"\) サフィックスは ARM で一意であり、次のセクションで説明します。  
  
||8|16|32|64|P|  
|-|-------|--------|--------|--------|-------|  
|追加|なし|なし|フル|フル|なし|  
|And|フル|フル|フル|フル|なし|  
|CompareExchange|フル|フル|フル|フル|フル|  
|Decrement|なし|フル|フル|フル|なし|  
|Exchange|Partial|Partial|Partial|Partial|Partial|  
|ExchangeAdd|フル|フル|フル|フル|なし|  
|インクリメント|なし|フル|フル|フル|なし|  
|Or|フル|フル|フル|フル|なし|  
|Xor|フル|フル|フル|フル|なし|  
  
 重要:  
  
-   **フル**: サフィックスなし、`_acq`、`_rel`、および `_nf` の各形式をサポートします。  
  
-   **Partial**: サフィックスなし、`_acq`、および `_nf` の各形式をサポートします。  
  
-   **なし**: サポートされません。  
  
###  <a name="nf_suffix"></a> \_nf \(フェンスなし\) サフィックス  
 `_nf` \("フェンスなし"\) サフィックスは、その操作に何らかのメモリ バリアとしての機能がないことを示します。  これは、すべてが何らかのバリアとして機能する他の 3 つの形式 \(サフィックスなし、`_acq`、および `_rel`\) とは対照的です。  考えられる `_nf` 形式の用途の 1 つに、複数のスレッドから同時に更新されるものの、そのスレッドの実行中には値が利用されない統計カウンターの保持があります。  
  
### インタロック組み込みのリスト  
  
|\[関数名\]|関数プロトタイプ|  
|-------------|--------------|  
|\_InterlockedAdd|long \_InterlockedAdd\(long \_volatile \*, long\)|  
|\_InterlockedAdd64|\_\_int64 \_InterlockedAdd64\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAdd64\_acq|\_\_int64 \_InterlockedAdd64\_acq\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAdd64\_nf|\_\_int64 \_InterlockedAdd64\_nf\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAdd64\_rel|\_\_int64 \_InterlockedAdd64\_rel\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAdd\_acq|long \_InterlockedAdd\_acq\(long volatile \*, long\)|  
|\_InterlockedAdd\_nf|long \_InterlockedAdd\_nf\(long volatile \*, long\)|  
|\_InterlockedAdd\_rel|long \_InterlockedAdd\_rel\(long volatile \*, long\)|  
|\_InterlockedAnd|long \_InterlockedAnd\(long volatile \*, long\)|  
|\_InterlockedAnd16|short \_InterlockedAnd16\(short volatile \*, short\)|  
|\_InterlockedAnd16\_acq|short \_InterlockedAnd16\_acq\(short volatile \*, short\)|  
|\_InterlockedAnd16\_nf|short \_InterlockedAnd16\_nf\(short volatile \*, short\)|  
|\_InterlockedAnd16\_rel|short \_InterlockedAnd16\_rel\(short volatile \*, short\)|  
|\_InterlockedAnd64|\_\_int64 \_InterlockedAnd64\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAnd64\_acq|\_\_int64 \_InterlockedAnd64\_acq\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAnd64\_nf|\_\_int64 \_InterlockedAnd64\_nf\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAnd64\_rel|\_\_int64 \_InterlockedAnd64\_rel\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedAnd8|char \_InterlockedAnd8\(char volatile \*, char\)|  
|\_InterlockedAnd8\_acq|char \_InterlockedAnd8\_acq\(char volatile \*, char\)|  
|\_InterlockedAnd8\_nf|char \_InterlockedAnd8\_nf\(char volatile \*, char\)|  
|\_InterlockedAnd8\_rel|char \_InterlockedAnd8\_rel\(char volatile \*, char\)|  
|\_InterlockedAnd\_acq|long \_InterlockedAnd\_acq\(long volatile \*, long\)|  
|\_InterlockedAnd\_nf|long \_InterlockedAnd\_nf\(long volatile \*, long\)|  
|\_InterlockedAnd\_rel|long \_InterlockedAnd\_rel\(long volatile \*, long\)|  
|\_InterlockedCompareExchange|long \_\_cdecl \_InterlockedCompareExchange\(long volatile \*, long, long\)|  
|\_InterlockedCompareExchange16|short \_InterlockedCompareExchange16\(short volatile \*, short, short\)|  
|\_InterlockedCompareExchange16\_acq|short \_InterlockedCompareExchange16\_acq\(short volatile \*, short, short\)|  
|\_InterlockedCompareExchange16\_nf|short \_InterlockedCompareExchange16\_nf\(short volatile \*, short, short\)|  
|\_InterlockedCompareExchange16\_rel|short \_InterlockedCompareExchange16\_rel\(short volatile \*, short, short\)|  
|\_InterlockedCompareExchange64|\_\_int64 \_InterlockedCompareExchange64\(\_\_int64 volatile \*, \_\_int64, \_\_int64\)|  
|\_InterlockedCompareExchange64\_acq|\_\_int64 \_InterlockedCompareExchange64\_acq\(\_\_int64 volatile \*, \_\_int64, \_\_int64\)|  
|\_InterlockedCompareExchange64\_nf|\_\_int64 \_InterlockedCompareExchange64\_nf\(\_\_int64 volatile \*, \_\_int64, \_\_int64\)|  
|\_InterlockedCompareExchange64\_rel|\_\_int64 \_InterlockedCompareExchange64\_rel\(\_\_int64 volatile \*, \_\_int64, \_\_int64\)|  
|\_InterlockedCompareExchange8|char \_InterlockedCompareExchange8\(char volatile \*, char, char\)|  
|\_InterlockedCompareExchange8\_acq|char \_InterlockedCompareExchange8\_acq\(char volatile \*, char, char\)|  
|\_InterlockedCompareExchange8\_nf|char \_InterlockedCompareExchange8\_nf\(char volatile \*, char, char\)|  
|\_InterlockedCompareExchange8\_rel|char \_InterlockedCompareExchange8\_rel\(char volatile \*, char, char\)|  
|\_InterlockedCompareExchangePointer|void \* \_InterlockedCompareExchangePointer\(void \* volatile \*, void \*, void \*\)|  
|\_InterlockedCompareExchangePointer\_acq|void \* \_InterlockedCompareExchangePointer\_acq\(void \* volatile \*, void \*, void \*\)|  
|\_InterlockedCompareExchangePointer\_nf|void \* \_InterlockedCompareExchangePointer\_nf\(void \* volatile \*, void \*, void \*\)|  
|\_InterlockedCompareExchangePointer\_rel|void \* \_InterlockedCompareExchangePointer\_rel\(void \* volatile \*, void \*, void \*\)|  
|\_InterlockedCompareExchange\_acq|long \_InterlockedCompareExchange\_acq\(long volatile \*, long, long\)|  
|\_InterlockedCompareExchange\_nf|long \_InterlockedCompareExchange\_nf\(long volatile \*, long, long\)|  
|\_InterlockedCompareExchange\_rel|long \_InterlockedCompareExchange\_rel\(long volatile \*, long, long\)|  
|\_InterlockedDecrement|long \_\_cdecl \_InterlockedDecrement\(long volatile \*\)|  
|\_InterlockedDecrement16|short \_InterlockedDecrement16\(short volatile \*\)|  
|\_InterlockedDecrement16\_acq|short \_InterlockedDecrement16\_acq\(short volatile \*\)|  
|\_InterlockedDecrement16\_nf|short \_InterlockedDecrement16\_nf\(short volatile \*\)|  
|\_InterlockedDecrement16\_rel|short \_InterlockedDecrement16\_rel\(short volatile \*\)|  
|\_InterlockedDecrement64|\_\_int64 \_InterlockedDecrement64\(\_\_int64 volatile \*\)|  
|\_InterlockedDecrement64\_acq|\_\_int64 \_InterlockedDecrement64\_acq\(\_\_int64 volatile \*\)|  
|\_InterlockedDecrement64\_nf|\_\_int64 \_InterlockedDecrement64\_nf\(\_\_int64 volatile \*\)|  
|\_InterlockedDecrement64\_rel|\_\_int64 \_InterlockedDecrement64\_rel\(\_\_int64 volatile \*\)|  
|\_InterlockedDecrement\_acq|long \_InterlockedDecrement\_acq\(long volatile \*\)|  
|\_InterlockedDecrement\_nf|long \_InterlockedDecrement\_nf\(long volatile \*\)|  
|\_InterlockedDecrement\_rel|long \_InterlockedDecrement\_rel\(long volatile \*\)|  
|\_InterlockedExchange|long \_\_cdecl \_InterlockedExchange\(long volatile \* \_Target, long\)|  
|\_InterlockedExchange16|short \_InterlockedExchange16\(short volatile \* \_Target, short\)|  
|\_InterlockedExchange16\_acq|short \_InterlockedExchange16\_acq\(short volatile \* \_Target, short\)|  
|\_InterlockedExchange16\_nf|short \_InterlockedExchange16\_nf\(short volatile \* \_Target, short\)|  
|\_InterlockedExchange64|\_\_int64 \_InterlockedExchange64\(\_\_int64 volatile \* \_Target, \_\_int64\)|  
|\_InterlockedExchange64\_acq|\_\_int64 \_InterlockedExchange64\_acq\(\_\_int64 volatile \* \_Target, \_\_int64\)|  
|\_InterlockedExchange64\_nf|\_\_int64 \_InterlockedExchange64\_nf\(\_\_int64 volatile \* \_Target, \_\_int64\)|  
|\_InterlockedExchange8|char \_InterlockedExchange8\(char volatile \* \_Target, char\)|  
|\_InterlockedExchange8\_acq|char \_InterlockedExchange8\_acq\(char volatile \* \_Target, char\)|  
|\_InterlockedExchange8\_nf|char \_InterlockedExchange8\_nf\(char volatile \* \_Target, char\)|  
|\_InterlockedExchangeAdd|long \_\_cdecl \_InterlockedExchangeAdd\(long volatile \*, long\)|  
|\_InterlockedExchangeAdd16|short \_InterlockedExchangeAdd16\(short volatile \*, short\)|  
|\_InterlockedExchangeAdd16\_acq|short \_InterlockedExchangeAdd16\_acq\(short volatile \*, short\)|  
|\_InterlockedExchangeAdd16\_nf|short \_InterlockedExchangeAdd16\_nf\(short volatile \*, short\)|  
|\_InterlockedExchangeAdd16\_rel|short \_InterlockedExchangeAdd16\_rel\(short volatile \*, short\)|  
|\_InterlockedExchangeAdd64|\_\_int64 \_InterlockedExchangeAdd64\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedExchangeAdd64\_acq|\_\_int64 \_InterlockedExchangeAdd64\_acq\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedExchangeAdd64\_nf|\_\_int64 \_InterlockedExchangeAdd64\_nf\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedExchangeAdd64\_rel|\_\_int64 \_InterlockedExchangeAdd64\_rel\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedExchangeAdd8|char \_InterlockedExchangeAdd8\(char volatile \*, char\)|  
|\_InterlockedExchangeAdd8\_acq|char \_InterlockedExchangeAdd8\_acq\(char volatile \*, char\)|  
|\_InterlockedExchangeAdd8\_nf|char \_InterlockedExchangeAdd8\_nf\(char volatile \*, char\)|  
|\_InterlockedExchangeAdd8\_rel|char \_InterlockedExchangeAdd8\_rel\(char volatile \*, char\)|  
|\_InterlockedExchangeAdd\_acq|long \_InterlockedExchangeAdd\_acq\(long volatile \*, long\)|  
|\_InterlockedExchangeAdd\_nf|long \_InterlockedExchangeAdd\_nf\(long volatile \*, long\)|  
|\_InterlockedExchangeAdd\_rel|long \_InterlockedExchangeAdd\_rel\(long volatile \*, long\)|  
|\_InterlockedExchangePointer|void \* \_InterlockedExchangePointer\(void \* volatile \* \_Target, void \*\)|  
|\_InterlockedExchangePointer\_acq|void \* \_InterlockedExchangePointer\_acq\(void \* volatile \* \_Target, void \*\)|  
|\_InterlockedExchangePointer\_nf|void \* \_InterlockedExchangePointer\_nf\(void \* volatile \* \_Target, void \*\)|  
|\_InterlockedExchange\_acq|long \_InterlockedExchange\_acq\(long volatile \* \_Target, long\)|  
|\_InterlockedExchange\_nf|long \_InterlockedExchange\_nf\(long volatile \* \_Target, long\)|  
|\_InterlockedIncrement|long \_\_cdecl \_InterlockedIncrement\(long volatile \*\)|  
|\_InterlockedIncrement16|short \_InterlockedIncrement16\(short volatile \*\)|  
|\_InterlockedIncrement16\_acq|short \_InterlockedIncrement16\_acq\(short volatile \*\)|  
|\_InterlockedIncrement16\_nf|short \_InterlockedIncrement16\_nf\(short volatile \*\)|  
|\_InterlockedIncrement16\_rel|short \_InterlockedIncrement16\_rel\(short volatile \*\)|  
|\_InterlockedIncrement64|\_\_int64 \_InterlockedIncrement64\(\_\_int64 volatile \*\)|  
|\_InterlockedIncrement64\_acq|\_\_int64 \_InterlockedIncrement64\_acq\(\_\_int64 volatile \*\)|  
|\_InterlockedIncrement64\_nf|\_\_int64 \_InterlockedIncrement64\_nf\(\_\_int64 volatile \*\)|  
|\_InterlockedIncrement64\_rel|\_\_int64 \_InterlockedIncrement64\_rel\(\_\_int64 volatile \*\)|  
|\_InterlockedIncrement\_acq|long \_InterlockedIncrement\_acq\(long volatile \*\)|  
|\_InterlockedIncrement\_nf|long \_InterlockedIncrement\_nf\(long volatile \*\)|  
|\_InterlockedIncrement\_rel|long \_InterlockedIncrement\_rel\(long volatile \*\)|  
|\_InterlockedOr|long \_InterlockedOr\(long volatile \*, long\)|  
|\_InterlockedOr16|short \_InterlockedOr16\(short volatile \*, short\)|  
|\_InterlockedOr16\_acq|short \_InterlockedOr16\_acq\(short volatile \*, short\)|  
|\_InterlockedOr16\_nf|short \_InterlockedOr16\_nf\(short volatile \*, short\)|  
|\_InterlockedOr16\_rel|short \_InterlockedOr16\_rel\(short volatile \*, short\)|  
|\_InterlockedOr64|\_\_int64 \_InterlockedOr64\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedOr64\_acq|\_\_int64 \_InterlockedOr64\_acq\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedOr64\_nf|\_\_int64 \_InterlockedOr64\_nf\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedOr64\_rel|\_\_int64 \_InterlockedOr64\_rel\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedOr8|char \_InterlockedOr8\(char volatile \*, char\)|  
|\_InterlockedOr8\_acq|char \_InterlockedOr8\_acq\(char volatile \*, char\)|  
|\_InterlockedOr8\_nf|char \_InterlockedOr8\_nf\(char volatile \*, char\)|  
|\_InterlockedOr8\_rel|char \_InterlockedOr8\_rel\(char volatile \*, char\)|  
|\_InterlockedOr\_acq|long \_InterlockedOr\_acq\(long volatile \*, long\)|  
|\_InterlockedOr\_nf|long \_InterlockedOr\_nf\(long volatile \*, long\)|  
|\_InterlockedOr\_rel|long \_InterlockedOr\_rel\(long volatile \*, long\)|  
|\_InterlockedXor|long \_InterlockedXor\(long volatile \*, long\)|  
|\_InterlockedXor16|short \_InterlockedXor16\(short volatile \*, short\)|  
|\_InterlockedXor16\_acq|short \_InterlockedXor16\_acq\(short volatile \*, short\)|  
|\_InterlockedXor16\_nf|short \_InterlockedXor16\_nf\(short volatile \*, short\)|  
|\_InterlockedXor16\_rel|short \_InterlockedXor16\_rel\(short volatile \*, short\)|  
|\_InterlockedXor64|\_\_int64 \_InterlockedXor64\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedXor64\_acq|\_\_int64 \_InterlockedXor64\_acq\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedXor64\_nf|\_\_int64 \_InterlockedXor64\_nf\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedXor64\_rel|\_\_int64 \_InterlockedXor64\_rel\(\_\_int64 volatile \*, \_\_int64\)|  
|\_InterlockedXor8|char \_InterlockedXor8\(char volatile \*, char\)|  
|\_InterlockedXor8\_acq|char \_InterlockedXor8\_acq\(char volatile \*, char\)|  
|\_InterlockedXor8\_nf|char \_InterlockedXor8\_nf\(char volatile \*, char\)|  
|\_InterlockedXor8\_rel|char \_InterlockedXor8\_rel\(char volatile \*, char\)|  
|\_InterlockedXor\_acq|long \_InterlockedXor\_acq\(long volatile \*, long\)|  
|\_InterlockedXor\_nf|long \_InterlockedXor\_nf\(long volatile \*, long\)|  
|\_InterlockedXor\_rel|long \_InterlockedXor\_rel\(long volatile \*, long\)|  
  
 \[[NEON](#top)\]  
  
### \_interlockedbittest の組み込み  
 サフィックスなしの bittest インターロック組み込みは、すべてのプラットフォームに共通です。  ARM では `_acq`、`_rel`、および`_nf` の各バリアントが追加されますが、これらのバリアントにより変更されるのは、バリアに関する操作のセマンティクスのみです \(このドキュメントの「[_nf (フェンスなし) サフィックス](#nf_suffix)」を参照\)。  
  
|\[関数名\]|関数プロトタイプ|  
|-------------|--------------|  
|\_interlockedbittestandreset|unsigned char \_interlockedbittestandreset\(long volatile \*, long\)|  
|\_interlockedbittestandreset\_acq|unsigned char \_interlockedbittestandreset\_acq\(long volatile \*, long\)|  
|\_interlockedbittestandreset\_nf|unsigned char \_interlockedbittestandreset\_nf\(long volatile \*, long\)|  
|\_interlockedbittestandreset\_rel|unsigned char \_interlockedbittestandreset\_rel\(long volatile \*, long\)|  
|\_interlockedbittestandset|unsigned char \_interlockedbittestandset\(long volatile \*, long\)|  
|\_interlockedbittestandset\_acq|unsigned char \_interlockedbittestandset\_acq\(long volatile \*, long\)|  
|\_interlockedbittestandset\_nf|unsigned char \_interlockedbittestandset\_nf\(long volatile \*, long\)|  
|\_interlockedbittestandset\_rel|unsigned char \_interlockedbittestandset\_rel\(long volatile \*, long\)|  
  
 \[[NEON](#top)\]  
  
## 参照  
 [コンパイラ組み込み](../intrinsics/compiler-intrinsics.md)   
 [ARM Assembler Reference](../Topic/ARM%20Assembler%20Reference.md)   
 [C\+\+ 言語リファレンス](../cpp/cpp-language-reference.md)