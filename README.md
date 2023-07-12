	.file	"smallt.cpp"
	.intel_syntax noprefix
	.section .rdata,"dr"
__ZStL19piecewise_construct:
	.space 1
.lcomm __ZStL8__ioinit,1,1
	.def	___main;	.scl	2;	.type	32;	.endef
	.text
	.globl	_main
	.def	_main;	.scl	2;	.type	32;	.endef
_main:
LFB1445: 
	.cfi_startproc
	lea	ecx, [esp+4]
	.cfi_def_cfa 1, 0
	and	esp, -16
	push	DWORD PTR [ecx-4]
	push	ebp
	.cfi_escape 0x10,0x5,0x2,0x75,0
	mov	ebp, esp
	push	ecx
	.cfi_escape 0xf,0x3,0x75,0x7c,0x6
	sub	esp, 36
	call	___main
	mov	DWORD PTR [ebp-12], 10
	mov	DWORD PTR [ebp-16], 25
	mov	edx, DWORD PTR [ebp-12]
	mov	eax, DWORD PTR [ebp-16]
	add	eax, edx
	mov	DWORD PTR [esp], eax
	mov	ecx, OFFSET FLAT:__ZSt4cout
	call	__ZNSolsEi
	sub	esp, 4
	mov	eax, 0
	mov	ecx, DWORD PTR [ebp-4]
	.cfi_def_cfa 1, 0
	leave
	.cfi_restore 5
	lea	esp, [ecx-4]
	.cfi_def_cfa 4, 4
	ret
	.cfi_endproc
LFE1445:
	.def	___tcf_0;	.scl	3;	.type	32;	.endef
___tcf_0:
LFB1870:
	.cfi_startproc
	push	ebp
	.cfi_def_cfa_offset 8
	.cfi_offset 5, -8
	mov	ebp, esp
	.cfi_def_cfa_register 5
	sub	esp, 8
	mov	ecx, OFFSET FLAT:__ZStL8__ioinit
	call	__ZNSt8ios_base4InitD1Ev
	leave
	.cfi_restore 5
	.cfi_def_cfa 4, 4
	ret
	.cfi_endproc
LFE1870:
	.def	__Z41__static_initialization_and_destruction_0ii;	.scl	3;	.type	32;	.endef
__Z41__static_initialization_and_destruction_0ii:
LFB1869:
	.cfi_startproc
	push	ebp
	.cfi_def_cfa_offset 8
	.cfi_offset 5, -8
	mov	ebp, esp
	.cfi_def_cfa_register 5
	sub	esp, 24
	cmp	DWORD PTR [ebp+8], 1
	jne	L6
	cmp	DWORD PTR [ebp+12], 65535
	jne	L6
	mov	ecx, OFFSET FLAT:__ZStL8__ioinit
	call	__ZNSt8ios_base4InitC1Ev
	mov	DWORD PTR [esp], OFFSET FLAT:___tcf_0
	call	_atexit
L6:
	nop
	leave
	.cfi_restore 5
	.cfi_def_cfa 4, 4
	ret
	.cfi_endproc
LFE1869:
	.def	__GLOBAL__sub_I_main;	.scl	3;	.type	32;	.endef
__GLOBAL__sub_I_main:
LFB1871:
	.cfi_startproc
	push	ebp
	.cfi_def_cfa_offset 8
	.cfi_offset 5, -8
	mov	ebp, esp
	.cfi_def_cfa_register 5
	sub	esp, 24
	mov	DWORD PTR [esp+4], 65535
	mov	DWORD PTR [esp], 1
	call	__Z41__static_initialization_and_destruction_0ii
	leave
	.cfi_restore 5
	.cfi_def_cfa 4, 4
	ret
	.cfi_endproc
LFE1871:
	.section	.ctors,"w"
	.align 4
	.long	__GLOBAL__sub_I_main
	.ident	"GCC: (MinGW.org GCC-6.3.0-1) 6.3.0"
	.def	__ZNSolsEi;	.scl	2;	.type	32;	.endef
	.def	__ZNSt8ios_base4InitD1Ev;	.scl	2;	.type	32;	.endef
	.def	__ZNSt8ios_base4InitC1Ev;	.scl	2;	.type	32;	.endef
	.def	_atexit;	.scl	2;	.type	32;	.endef















; ModuleID = 'smallt.cpp'
source_filename = "smallt.cpp"
target datalayout = "e-m:w-p270:32:32-p271:32:32-p272:64:64-i64:64-f80:128-n8:16:32:64-S128"
target triple = "x86_64-w64-windows-gnu"

%"class.std::ios_base::Init" = type { i8 }
%"class.std::basic_ostream" = type { ptr, %"class.std::basic_ios" }
%"class.std::basic_ios" = type { %"class.std::ios_base", ptr, i8, i8, ptr, ptr, ptr, ptr }
%"class.std::ios_base" = type { ptr, i64, i64, i32, i32, i32, ptr, %"struct.std::ios_base::_Words", [8 x %"struct.std::ios_base::_Words"], i32, ptr, %"class.std::locale" }
%"struct.std::ios_base::_Words" = type <{ ptr, i32, [4 x i8] }>
%"class.std::locale" = type { ptr }

@_ZStL8__ioinit = internal global %"class.std::ios_base::Init" zeroinitializer, align 1
@_ZSt4cout = external global %"class.std::basic_ostream", align 8
@llvm.global_ctors = appending global [1 x { i32, ptr, ptr }] [{ i32, ptr, ptr } { i32 65535, ptr @_GLOBAL__sub_I_smallt.cpp, ptr null }]

; Function Attrs: noinline uwtable
define internal void @__cxx_global_var_init() #0 {
  call void @_ZNSt8ios_base4InitC1Ev(ptr noundef nonnull align 1 dereferenceable(1) @_ZStL8__ioinit)
  %1 = call i32 @atexit(ptr @__dtor__ZStL8__ioinit) #3
  ret void
}

declare dso_local void @_ZNSt8ios_base4InitC1Ev(ptr noundef nonnull align 1 dereferenceable(1)) unnamed_addr #1

; Function Attrs: nounwind
declare dso_local void @_ZNSt8ios_base4InitD1Ev(ptr noundef nonnull align 1 dereferenceable(1)) unnamed_addr #2

; Function Attrs: noinline uwtable
define internal void @__dtor__ZStL8__ioinit() #0 {
  call void @_ZNSt8ios_base4InitD1Ev(ptr @_ZStL8__ioinit)
  ret void
}

; Function Attrs: nounwind
declare dso_local i32 @atexit(ptr) #3

; Function Attrs: mustprogress noinline norecurse optnone uwtable
define dso_local noundef i32 @main() #4 {
  %1 = alloca i32, align 4
  %2 = alloca i32, align 4
  %3 = alloca i32, align 4
  store i32 0, ptr %1, align 4
  store i32 10, ptr %2, align 4
  store i32 25, ptr %3, align 4
  %4 = load i32, ptr %2, align 4
  %5 = load i32, ptr %3, align 4
  %6 = add nsw i32 %4, %5
  %7 = call noundef nonnull align 8 dereferenceable(8) ptr @_ZNSolsEi(ptr noundef nonnull align 8 dereferenceable(8) @_ZSt4cout, i32 noundef %6)
  ret i32 0
}

declare dso_local noundef nonnull align 8 dereferenceable(8) ptr @_ZNSolsEi(ptr noundef nonnull align 8 dereferenceable(8), i32 noundef) #1

; Function Attrs: noinline uwtable
define internal void @_GLOBAL__sub_I_smallt.cpp() #0 {
  call void @__cxx_global_var_init()
  ret void
}

attributes #0 = { noinline uwtable "min-legal-vector-width"="0" "no-trapping-math"="true" "stack-protector-buffer-size"="8" "target-cpu"="x86-64" "target-features"="+cx8,+fxsr,+mmx,+sse,+sse2,+x87" "tune-cpu"="generic" }
attributes #1 = { "no-trapping-math"="true" "stack-protector-buffer-size"="8" "target-cpu"="x86-64" "target-features"="+cx8,+fxsr,+mmx,+sse,+sse2,+x87" "tune-cpu"="generic" }
attributes #2 = { nounwind "no-trapping-math"="true" "stack-protector-buffer-size"="8" "target-cpu"="x86-64" "target-features"="+cx8,+fxsr,+mmx,+sse,+sse2,+x87" "tune-cpu"="generic" }
attributes #3 = { nounwind }
attributes #4 = { mustprogress noinline norecurse optnone uwtable "min-legal-vector-width"="0" "no-trapping-math"="true" "stack-protector-buffer-size"="8" "target-cpu"="x86-64" "target-features"="+cx8,+fxsr,+mmx,+sse,+sse2,+x87" "tune-cpu"="generic" }

!llvm.module.flags = !{!0, !1, !2}
!llvm.ident = !{!3}

!0 = !{i32 1, !"wchar_size", i32 2}
!1 = !{i32 8, !"PIC Level", i32 2}
!2 = !{i32 7, !"uwtable", i32 2}
!3 = !{!"clang version 16.0.0"}

















	.text
	.def	@feat.00;
	.scl	3;
	.type	0;
	.endef
	.globl	@feat.00
.set @feat.00, 0
	.intel_syntax noprefix
	.file	"smallt.cpp"
	.def	__cxx_global_var_init;
	.scl	3;
	.type	32;
	.endef
	.p2align	4, 0x90                         # -- Begin function __cxx_global_var_init
__cxx_global_var_init:                  # @__cxx_global_var_init
.seh_proc __cxx_global_var_init
# %bb.0:
	sub	rsp, 40
	.seh_stackalloc 40
	.seh_endprologue
	lea	rcx, [rip + _ZStL8__ioinit]
	call	_ZNSt8ios_base4InitC1Ev
	lea	rcx, [rip + __dtor__ZStL8__ioinit]
	call	atexit
	nop
	add	rsp, 40
	ret
	.seh_endproc
                                        # -- End function
	.def	__dtor__ZStL8__ioinit;
	.scl	3;
	.type	32;
	.endef
	.p2align	4, 0x90                         # -- Begin function __dtor__ZStL8__ioinit
__dtor__ZStL8__ioinit:                  # @__dtor__ZStL8__ioinit
.seh_proc __dtor__ZStL8__ioinit
# %bb.0:
	sub	rsp, 40
	.seh_stackalloc 40
	.seh_endprologue
	lea	rcx, [rip + _ZStL8__ioinit]
	call	_ZNSt8ios_base4InitD1Ev
	nop
	add	rsp, 40
	ret
	.seh_endproc
                                        # -- End function
	.def	main;
	.scl	2;
	.type	32;
	.endef
	.globl	main                            # -- Begin function main
	.p2align	4, 0x90
main:                                   # @main
.seh_proc main
# %bb.0:
	push	rbp
	.seh_pushreg rbp
	sub	rsp, 48
	.seh_stackalloc 48
	lea	rbp, [rsp + 48]
	.seh_setframe rbp, 48
	.seh_endprologue
	call	__main
	mov	dword ptr [rbp - 4], 0
	mov	dword ptr [rbp - 8], 10
	mov	dword ptr [rbp - 12], 25
	mov	edx, dword ptr [rbp - 8]
	add	edx, dword ptr [rbp - 12]
	mov	rcx, qword ptr [rip + .refptr._ZSt4cout]
	call	_ZNSolsEi
	xor	eax, eax
	add	rsp, 48
	pop	rbp
	ret
	.seh_endproc
                                        # -- End function
	.def	_GLOBAL__sub_I_smallt.cpp;
	.scl	3;
	.type	32;
	.endef
	.p2align	4, 0x90                         # -- Begin function _GLOBAL__sub_I_smallt.cpp
_GLOBAL__sub_I_smallt.cpp:              # @_GLOBAL__sub_I_smallt.cpp
.seh_proc _GLOBAL__sub_I_smallt.cpp
# %bb.0:
	sub	rsp, 40
	.seh_stackalloc 40
	.seh_endprologue
	call	__cxx_global_var_init
	nop
	add	rsp, 40
	ret
	.seh_endproc
                                        # -- End function
	.lcomm	_ZStL8__ioinit,1                # @_ZStL8__ioinit
	.section	.ctors,"dw"
	.p2align	3, 0x0
	.quad	_GLOBAL__sub_I_smallt.cpp
	.section	.rdata$.refptr._ZSt4cout,"dr",discard,.refptr._ZSt4cout
	.p2align	3, 0x0
	.globl	.refptr._ZSt4cout
.refptr._ZSt4cout:
	.quad	_ZSt4cout
	.addrsig
	.addrsig_sym __cxx_global_var_init
	.addrsig_sym __dtor__ZStL8__ioinit
	.addrsig_sym atexit
	.addrsig_sym _ZNSolsEi
	.addrsig_sym _GLOBAL__sub_I_smallt.cpp
	.addrsig_sym _ZStL8__ioinit
	.addrsig_sym _ZSt4cout


 


