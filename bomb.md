
bomb:     file format elf32-i386


Disassembly of section .init:

08048724 <_init>:
 8048724:	53                   	push   %ebx
 8048725:	83 ec 08             	sub    $0x8,%esp
 8048728:	e8 00 00 00 00       	call   804872d <_init+0x9>
 804872d:	5b                   	pop    %ebx
 804872e:	81 c3 c7 38 00 00    	add    $0x38c7,%ebx
 8048734:	8b 83 fc ff ff ff    	mov    -0x4(%ebx),%eax
 804873a:	85 c0                	test   %eax,%eax
 804873c:	74 05                	je     8048743 <_init+0x1f>
 804873e:	e8 ed 00 00 00       	call   8048830 <__gmon_start__@plt>
 8048743:	e8 78 02 00 00       	call   80489c0 <frame_dummy>
 8048748:	e8 d3 18 00 00       	call   804a020 <__do_global_ctors_aux>
 804874d:	83 c4 08             	add    $0x8,%esp
 8048750:	5b                   	pop    %ebx
 8048751:	c3                   	ret    

Disassembly of section .plt:

08048760 <.plt>:
 8048760:	ff 35 f8 bf 04 08    	push   0x804bff8			#0x804bff8入栈
 8048766:	ff 25 fc bf 04 08    	jmp    *0x804bffc			#跳转到地址0x804bffc中存储的地址
 804876c:	00 00                	add    %al,(%eax)			#%eax指向的地址的值加上%al的值
	...

08048770 <read@plt>:
 8048770:	ff 25 00 c0 04 08    	jmp    *0x804c000
 8048776:	68 00 00 00 00       	push   $0x0
 804877b:	e9 e0 ff ff ff       	jmp    8048760 <.plt>

08048780 <fflush@plt>:
 8048780:	ff 25 04 c0 04 08    	jmp    *0x804c004
 8048786:	68 08 00 00 00       	push   $0x8
 804878b:	e9 d0 ff ff ff       	jmp    8048760 <.plt>

08048790 <fgets@plt>:
 8048790:	ff 25 08 c0 04 08    	jmp    *0x804c008
 8048796:	68 10 00 00 00       	push   $0x10
 804879b:	e9 c0 ff ff ff       	jmp    8048760 <.plt>

080487a0 <signal@plt>:
 80487a0:	ff 25 0c c0 04 08    	jmp    *0x804c00c			#跳转到地址0x804c00c中储存的地址
 80487a6:	68 18 00 00 00       	push   $0x18				#0x18入栈
 80487ab:	e9 b0 ff ff ff       	jmp    8048760 <.plt>		#跳转到地址0x8048760

080487b0 <sleep@plt>:
 80487b0:	ff 25 10 c0 04 08    	jmp    *0x804c010
 80487b6:	68 20 00 00 00       	push   $0x20
 80487bb:	e9 a0 ff ff ff       	jmp    8048760 <.plt>

080487c0 <alarm@plt>:
 80487c0:	ff 25 14 c0 04 08    	jmp    *0x804c014
 80487c6:	68 28 00 00 00       	push   $0x28
 80487cb:	e9 90 ff ff ff       	jmp    8048760 <.plt>

080487d0 <__stack_chk_fail@plt>:
 80487d0:	ff 25 18 c0 04 08    	jmp    *0x804c018
 80487d6:	68 30 00 00 00       	push   $0x30
 80487db:	e9 80 ff ff ff       	jmp    8048760 <.plt>

080487e0 <strcpy@plt>:
 80487e0:	ff 25 1c c0 04 08    	jmp    *0x804c01c
 80487e6:	68 38 00 00 00       	push   $0x38
 80487eb:	e9 70 ff ff ff       	jmp    8048760 <.plt>

080487f0 <getenv@plt>:
 80487f0:	ff 25 20 c0 04 08    	jmp    *0x804c020
 80487f6:	68 40 00 00 00       	push   $0x40
 80487fb:	e9 60 ff ff ff       	jmp    8048760 <.plt>

08048800 <puts@plt>:
 8048800:	ff 25 24 c0 04 08    	jmp    *0x804c024
 8048806:	68 48 00 00 00       	push   $0x48
 804880b:	e9 50 ff ff ff       	jmp    8048760 <.plt>

08048810 <__memmove_chk@plt>:
 8048810:	ff 25 28 c0 04 08    	jmp    *0x804c028
 8048816:	68 50 00 00 00       	push   $0x50
 804881b:	e9 40 ff ff ff       	jmp    8048760 <.plt>

08048820 <__memcpy_chk@plt>:
 8048820:	ff 25 2c c0 04 08    	jmp    *0x804c02c
 8048826:	68 58 00 00 00       	push   $0x58
 804882b:	e9 30 ff ff ff       	jmp    8048760 <.plt>

08048830 <__gmon_start__@plt>:
 8048830:	ff 25 30 c0 04 08    	jmp    *0x804c030
 8048836:	68 60 00 00 00       	push   $0x60
 804883b:	e9 20 ff ff ff       	jmp    8048760 <.plt>

08048840 <exit@plt>:
 8048840:	ff 25 34 c0 04 08    	jmp    *0x804c034
 8048846:	68 68 00 00 00       	push   $0x68
 804884b:	e9 10 ff ff ff       	jmp    8048760 <.plt>

08048850 <__libc_start_main@plt>:
 8048850:	ff 25 38 c0 04 08    	jmp    *0x804c038
 8048856:	68 70 00 00 00       	push   $0x70
 804885b:	e9 00 ff ff ff       	jmp    8048760 <.plt>

08048860 <write@plt>:
 8048860:	ff 25 3c c0 04 08    	jmp    *0x804c03c
 8048866:	68 78 00 00 00       	push   $0x78
 804886b:	e9 f0 fe ff ff       	jmp    8048760 <.plt>

08048870 <__isoc99_sscanf@plt>:
 8048870:	ff 25 40 c0 04 08    	jmp    *0x804c040
 8048876:	68 80 00 00 00       	push   $0x80
 804887b:	e9 e0 fe ff ff       	jmp    8048760 <.plt>

08048880 <fopen@plt>:
 8048880:	ff 25 44 c0 04 08    	jmp    *0x804c044
 8048886:	68 88 00 00 00       	push   $0x88
 804888b:	e9 d0 fe ff ff       	jmp    8048760 <.plt>

08048890 <__errno_location@plt>:
 8048890:	ff 25 48 c0 04 08    	jmp    *0x804c048
 8048896:	68 90 00 00 00       	push   $0x90
 804889b:	e9 c0 fe ff ff       	jmp    8048760 <.plt>

080488a0 <__printf_chk@plt>:
 80488a0:	ff 25 4c c0 04 08    	jmp    *0x804c04c
 80488a6:	68 98 00 00 00       	push   $0x98
 80488ab:	e9 b0 fe ff ff       	jmp    8048760 <.plt>

080488b0 <socket@plt>:
 80488b0:	ff 25 50 c0 04 08    	jmp    *0x804c050
 80488b6:	68 a0 00 00 00       	push   $0xa0
 80488bb:	e9 a0 fe ff ff       	jmp    8048760 <.plt>

080488c0 <__fprintf_chk@plt>:
 80488c0:	ff 25 54 c0 04 08    	jmp    *0x804c054
 80488c6:	68 a8 00 00 00       	push   $0xa8
 80488cb:	e9 90 fe ff ff       	jmp    8048760 <.plt>

080488d0 <gethostbyname@plt>:
 80488d0:	ff 25 58 c0 04 08    	jmp    *0x804c058
 80488d6:	68 b0 00 00 00       	push   $0xb0
 80488db:	e9 80 fe ff ff       	jmp    8048760 <.plt>

080488e0 <strtol@plt>:
 80488e0:	ff 25 5c c0 04 08    	jmp    *0x804c05c
 80488e6:	68 b8 00 00 00       	push   $0xb8
 80488eb:	e9 70 fe ff ff       	jmp    8048760 <.plt>

080488f0 <connect@plt>:
 80488f0:	ff 25 60 c0 04 08    	jmp    *0x804c060
 80488f6:	68 c0 00 00 00       	push   $0xc0
 80488fb:	e9 60 fe ff ff       	jmp    8048760 <.plt>

08048900 <close@plt>:
 8048900:	ff 25 64 c0 04 08    	jmp    *0x804c064
 8048906:	68 c8 00 00 00       	push   $0xc8
 804890b:	e9 50 fe ff ff       	jmp    8048760 <.plt>

08048910 <__ctype_b_loc@plt>:
 8048910:	ff 25 68 c0 04 08    	jmp    *0x804c068
 8048916:	68 d0 00 00 00       	push   $0xd0
 804891b:	e9 40 fe ff ff       	jmp    8048760 <.plt>

08048920 <__sprintf_chk@plt>:
 8048920:	ff 25 6c c0 04 08    	jmp    *0x804c06c
 8048926:	68 d8 00 00 00       	push   $0xd8
 804892b:	e9 30 fe ff ff       	jmp    8048760 <.plt>

Disassembly of section .text:

08048930 <_start>:
 8048930:	31 ed                	xor    %ebp,%ebp							#ebp异或其本身，清零
 8048932:	5e                   	pop    %esi									#
 8048933:	89 e1                	mov    %esp,%ecx
 8048935:	83 e4 f0             	and    $0xfffffff0,%esp
 8048938:	50                   	push   %eax
 8048939:	54                   	push   %esp
 804893a:	52                   	push   %edx
 804893b:	68 10 a0 04 08       	push   $0x804a010
 8048940:	68 a0 9f 04 08       	push   $0x8049fa0
 8048945:	51                   	push   %ecx
 8048946:	56                   	push   %esi
 8048947:	68 e4 89 04 08       	push   $0x80489e4
 804894c:	e8 ff fe ff ff       	call   8048850 <__libc_start_main@plt>
 8048951:	f4                   	hlt    
 8048952:	90                   	nop
 8048953:	90                   	nop
 8048954:	90                   	nop
 8048955:	90                   	nop
 8048956:	90                   	nop
 8048957:	90                   	nop
 8048958:	90                   	nop
 8048959:	90                   	nop
 804895a:	90                   	nop
 804895b:	90                   	nop
 804895c:	90                   	nop
 804895d:	90                   	nop
 804895e:	90                   	nop
 804895f:	90                   	nop

08048960 <__do_global_dtors_aux>:
 8048960:	55                   	push   %ebp
 8048961:	89 e5                	mov    %esp,%ebp
 8048963:	53                   	push   %ebx
 8048964:	83 ec 04             	sub    $0x4,%esp
 8048967:	80 3d c4 c3 04 08 00 	cmpb   $0x0,0x804c3c4
 804896e:	75 3f                	jne    80489af <__do_global_dtors_aux+0x4f>
 8048970:	a1 c8 c3 04 08       	mov    0x804c3c8,%eax
 8048975:	bb 20 bf 04 08       	mov    $0x804bf20,%ebx
 804897a:	81 eb 1c bf 04 08    	sub    $0x804bf1c,%ebx
 8048980:	c1 fb 02             	sar    $0x2,%ebx
 8048983:	83 eb 01             	sub    $0x1,%ebx
 8048986:	39 d8                	cmp    %ebx,%eax
 8048988:	73 1e                	jae    80489a8 <__do_global_dtors_aux+0x48>
 804898a:	8d b6 00 00 00 00    	lea    0x0(%esi),%esi
 8048990:	83 c0 01             	add    $0x1,%eax
 8048993:	a3 c8 c3 04 08       	mov    %eax,0x804c3c8
 8048998:	ff 14 85 1c bf 04 08 	call   *0x804bf1c(,%eax,4)
 804899f:	a1 c8 c3 04 08       	mov    0x804c3c8,%eax
 80489a4:	39 d8                	cmp    %ebx,%eax
 80489a6:	72 e8                	jb     8048990 <__do_global_dtors_aux+0x30>
 80489a8:	c6 05 c4 c3 04 08 01 	movb   $0x1,0x804c3c4
 80489af:	83 c4 04             	add    $0x4,%esp
 80489b2:	5b                   	pop    %ebx
 80489b3:	5d                   	pop    %ebp
 80489b4:	c3                   	ret    
 80489b5:	8d 74 26 00          	lea    0x0(%esi,%eiz,1),%esi
 80489b9:	8d bc 27 00 00 00 00 	lea    0x0(%edi,%eiz,1),%edi

080489c0 <frame_dummy>:
 80489c0:	55                   	push   %ebp
 80489c1:	89 e5                	mov    %esp,%ebp
 80489c3:	83 ec 18             	sub    $0x18,%esp
 80489c6:	a1 24 bf 04 08       	mov    0x804bf24,%eax
 80489cb:	85 c0                	test   %eax,%eax
 80489cd:	74 12                	je     80489e1 <frame_dummy+0x21>
 80489cf:	b8 00 00 00 00       	mov    $0x0,%eax
 80489d4:	85 c0                	test   %eax,%eax
 80489d6:	74 09                	je     80489e1 <frame_dummy+0x21>
 80489d8:	c7 04 24 24 bf 04 08 	movl   $0x804bf24,(%esp)
 80489df:	ff d0                	call   *%eax
 80489e1:	c9                   	leave  
 80489e2:	c3                   	ret    
 80489e3:	90                   	nop

080489e4 <main>:
 80489e4:	55                   	push   %ebp							#
 80489e5:	89 e5                	mov    %esp,%ebp					#初始化栈
 80489e7:	53                   	push   %ebx							#%ebx入栈
 80489e8:	83 e4 f0             	and    $0xfffffff0,%esp				#对齐
 80489eb:	83 ec 10             	sub    $0x10,%esp					#%esp向下移4字节
 80489ee:	8b 45 08             	mov    0x8(%ebp),%eax				#0x8(%ebp)加载到%eax
 80489f1:	8b 5d 0c             	mov    0xc(%ebp),%ebx				#0xc(%ebp)加载到%ebx
 80489f4:	83 f8 01             	cmp    $0x1,%eax					#比较0x1与%eax
 80489f7:	75 0c                	jne    8048a05 <main+0x21>			#如果0x1!=%eax则跳转到0x8048a05
 80489f9:	a1 a4 c3 04 08       	mov    0x804c3a4,%eax				#将地址0x804c3a4的值加载到%eax
 80489fe:	a3 d0 c3 04 08       	mov    %eax,0x804c3d0				#将%eax中的值存储到地址0x804c3d0中
 8048a03:	eb 74                	jmp    8048a79 <main+0x95>			#跳转到0x8048a79
 8048a05:	83 f8 02             	cmp    $0x2,%eax
 8048a08:	75 49                	jne    8048a53 <main+0x6f>
 8048a0a:	c7 44 24 04 88 a0 04 	movl   $0x804a088,0x4(%esp)
 8048a11:	08 
 8048a12:	8b 43 04             	mov    0x4(%ebx),%eax
 8048a15:	89 04 24             	mov    %eax,(%esp)
 8048a18:	e8 63 fe ff ff       	call   8048880 <fopen@plt>
 8048a1d:	a3 d0 c3 04 08       	mov    %eax,0x804c3d0
 8048a22:	85 c0                	test   %eax,%eax
 8048a24:	75 53                	jne    8048a79 <main+0x95>
 8048a26:	8b 43 04             	mov    0x4(%ebx),%eax
 8048a29:	89 44 24 0c          	mov    %eax,0xc(%esp)
 8048a2d:	8b 03                	mov    (%ebx),%eax
 8048a2f:	89 44 24 08          	mov    %eax,0x8(%esp)
 8048a33:	c7 44 24 04 8a a0 04 	movl   $0x804a08a,0x4(%esp)
 8048a3a:	08 
 8048a3b:	c7 04 24 01 00 00 00 	movl   $0x1,(%esp)
 8048a42:	e8 59 fe ff ff       	call   80488a0 <__printf_chk@plt>
 8048a47:	c7 04 24 08 00 00 00 	movl   $0x8,(%esp)
 8048a4e:	e8 ed fd ff ff       	call   8048840 <exit@plt>
 8048a53:	8b 03                	mov    (%ebx),%eax
 8048a55:	89 44 24 08          	mov    %eax,0x8(%esp)
 8048a59:	c7 44 24 04 a7 a0 04 	movl   $0x804a0a7,0x4(%esp)
 8048a60:	08 
 8048a61:	c7 04 24 01 00 00 00 	movl   $0x1,(%esp)
 8048a68:	e8 33 fe ff ff       	call   80488a0 <__printf_chk@plt>
 8048a6d:	c7 04 24 08 00 00 00 	movl   $0x8,(%esp)
 8048a74:	e8 c7 fd ff ff       	call   8048840 <exit@plt>
 8048a79:	e8 dd 05 00 00       	call   804905b <initialize_bomb>	#调用函数0x804905b <initialize_bomb>
 8048a7e:	c7 04 24 0c a1 04 08 	movl   $0x804a10c,(%esp)
 8048a85:	e8 76 fd ff ff       	call   8048800 <puts@plt>
 8048a8a:	c7 04 24 48 a1 04 08 	movl   $0x804a148,(%esp)
 8048a91:	e8 6a fd ff ff       	call   8048800 <puts@plt>
 8048a96:	e8 82 06 00 00       	call   804911d <read_line>			#调用函数0x804911d <read_line>
 8048a9b:	89 04 24             	mov    %eax,(%esp)					#将%eax的值存储到%esp指向的地址
 8048a9e:	e8 ad 00 00 00       	call   8048b50 <phase_1>			#调用函数0x8048b50 <phase_1>
 8048aa3:	e8 d3 07 00 00       	call   804927b <phase_defused>
 8048aa8:	c7 04 24 74 a1 04 08 	movl   $0x804a174,(%esp)
 8048aaf:	e8 4c fd ff ff       	call   8048800 <puts@plt>
 8048ab4:	e8 64 06 00 00       	call   804911d <read_line>
 8048ab9:	89 04 24             	mov    %eax,(%esp)
 8048abc:	e8 b3 00 00 00       	call   8048b74 <phase_2>			#调用函数0x8048b74 <phase_2>
 8048ac1:	e8 b5 07 00 00       	call   804927b <phase_defused>
 8048ac6:	c7 04 24 c1 a0 04 08 	movl   $0x804a0c1,(%esp)
 8048acd:	e8 2e fd ff ff       	call   8048800 <puts@plt>
 8048ad2:	e8 46 06 00 00       	call   804911d <read_line>
 8048ad7:	89 04 24             	mov    %eax,(%esp)
 8048ada:	e8 e5 00 00 00       	call   8048bc4 <phase_3>			#三阶段
 8048adf:	e8 97 07 00 00       	call   804927b <phase_defused>
 8048ae4:	c7 04 24 df a0 04 08 	movl   $0x804a0df,(%esp)
 8048aeb:	e8 10 fd ff ff       	call   8048800 <puts@plt>
 8048af0:	e8 28 06 00 00       	call   804911d <read_line>
 8048af5:	89 04 24             	mov    %eax,(%esp)
 8048af8:	e8 e2 01 00 00       	call   8048cdf <phase_4>			#四阶段
 8048afd:	e8 79 07 00 00       	call   804927b <phase_defused>
 8048b02:	c7 04 24 a0 a1 04 08 	movl   $0x804a1a0,(%esp)
 8048b09:	e8 f2 fc ff ff       	call   8048800 <puts@plt>
 8048b0e:	e8 0a 06 00 00       	call   804911d <read_line>
 8048b13:	89 04 24             	mov    %eax,(%esp)
 8048b16:	e8 26 02 00 00       	call   8048d41 <phase_5>			#五阶段
 8048b1b:	e8 5b 07 00 00       	call   804927b <phase_defused>
 8048b20:	c7 04 24 ee a0 04 08 	movl   $0x804a0ee,(%esp)
 8048b27:	e8 d4 fc ff ff       	call   8048800 <puts@plt>
 8048b2c:	e8 ec 05 00 00       	call   804911d <read_line>
 8048b31:	89 04 24             	mov    %eax,(%esp)
 8048b34:	e8 7c 02 00 00       	call   8048db5 <phase_6>			#六阶段
 8048b39:	e8 3d 07 00 00       	call   804927b <phase_defused>
 8048b3e:	b8 00 00 00 00       	mov    $0x0,%eax
 8048b43:	8b 5d fc             	mov    -0x4(%ebp),%ebx
 8048b46:	c9                   	leave  
 8048b47:	c3                   	ret    
 8048b48:	90                   	nop
 8048b49:	90                   	nop
 8048b4a:	90                   	nop
 8048b4b:	90                   	nop
 8048b4c:	90                   	nop
 8048b4d:	90                   	nop
 8048b4e:	90                   	nop
 8048b4f:	90                   	nop

08048b50 <phase_1>:
 8048b50:	83 ec 1c             	sub    $0x1c,%esp						#%esp向下移动7字节
 8048b53:	c7 44 24 04 c4 a1 04 	movl   $0x804a1c4,0x4(%esp)				#将0x804a1c4存储到0x4(%esp)
 8048b5a:	08 
 8048b5b:	8b 44 24 20          	mov    0x20(%esp),%eax					#将0x20(%esp)处的值加载到%eax
 8048b5f:	89 04 24             	mov    %eax,(%esp)						#将%eax的值存储到%esp指向的地址
 8048b62:	e8 7d 04 00 00       	call   8048fe4 <strings_not_equal>		#调用函数0x8048fe4 <strings_not_equal>
 8048b67:	85 c0                	test   %eax,%eax						#检查%eax的值是否为0
 8048b69:	74 05                	je     8048b70 <phase_1+0x20>			#为0时跳转
 8048b6b:	e8 86 05 00 00       	call   80490f6 <explode_bomb>
 8048b70:	83 c4 1c             	add    $0x1c,%esp
 8048b73:	c3                   	ret    

08048b74 <phase_2>:
 8048b74:	56                   	push   %esi
 8048b75:	53                   	push   %ebx
 8048b76:	83 ec 34             	sub    $0x34,%esp
 8048b79:	8d 44 24 18          	lea    0x18(%esp),%eax
 8048b7d:	89 44 24 04          	mov    %eax,0x4(%esp)
 8048b81:	8b 44 24 40          	mov    0x40(%esp),%eax
 8048b85:	89 04 24             	mov    %eax,(%esp)
 8048b88:	e8 9e 06 00 00       	call   804922b <read_six_numbers>		#顾名思义读六个数，返回时%eax装的输入数的个数（不是6也不会返回了，直接爆）
 8048b8d:	83 7c 24 18 00       	cmpl   $0x0,0ex18(%esp)					#第一个参数是不是0
 8048b92:	75 07                	jne    8048b9b <phase_2+0x27>			#不等于爆炸
 8048b94:	83 7c 24 1c 01       	cmpl   $0x1,0x1c(%esp)					#第二个参数是不是1
 8048b99:	74 05                	je     8048ba0 <phase_2+0x2c>			#等于不炸
 8048b9b:	e8 56 05 00 00       	call   80490f6 <explode_bomb>
 8048ba0:	8d 5c 24 20          	lea    0x20(%esp),%ebx
 8048ba4:	8d 74 24 30          	lea    0x30(%esp),%es
 8048ba8:	8b 43 f8             	mov    -0x8(%ebx),%eax					#进入循环 %ebx系列存的参数 
 8048bab:	03 43 fc             	add    -0x4(%ebx),%eax					#
 8048bae:	39 03                	cmp    %eax,(%ebx)						#(%ebx)=%eax
 8048bb0:	74 05                	je     8048bb7 <phase_2+0x43>			#等于不炸
 8048bb2:	e8 3f 05 00 00       	call   80490f6 <explode_bomb>			#
 8048bb7:	83 c3 04             	add    $0x4,%ebx						#+4
 8048bba:	39 f3                	cmp    %esi,%ebx						#
 8048bbc:	75 ea                	jne    8048ba8 <phase_2+0x34>			#等于循环结束
 8048bbe:	83 c4 34             	add    $0x34,%esp
 8048bc1:	5b                   	pop    %ebx
 8048bc2:	5e                   	pop    %esi
 8048bc3:	c3                   	ret    

08048bc4 <phase_3>:															#phase_3是一个巨大的switch case
 8048bc4:	83 ec 2c             	sub    $0x2c,%esp
 8048bc7:	8d 44 24 1c          	lea    0x1c(%esp),%eax					
 8048bcb:	89 44 24 0c          	mov    %eax,0xc(%esp)					#参数2 0x1c(%esp)
 8048bcf:	8d 44 24 18          	lea    0x18(%esp),%eax
 8048bd3:	89 44 24 08          	mov    %eax,0x8(%esp)					#参数1 0x18(%esp)
 8048bd7:	c7 44 24 04 e3 a3 04 	movl   $0x804a3e3,0x4(%esp)				#"%d %d" 不是隐藏
 8048bde:	08 
 8048bdf:	8b 44 24 30          	mov    0x30(%esp),%eax
 8048be3:	89 04 24             	mov    %eax,(%esp)
 8048be6:	e8 85 fc ff ff       	call   8048870 <__isoc99_sscanf@plt>
 8048beb:	83 f8 01             	cmp    $0x1,%eax						#参数个数大于1不爆炸
 8048bee:	7f 05                	jg     8048bf5 <phase_3+0x31>
 8048bf0:	e8 01 05 00 00       	call   80490f6 <explode_bomb>
 8048bf5:	83 7c 24 18 07       	cmpl   $0x7,0x18(%esp)					#
 8048bfa:	77 66                	ja     8048c62 <phase_3+0x9e>			#参数1大于0x7爆炸
 8048bfc:	8b 44 24 18          	mov    0x18(%esp),%eax					#参数1赋值给%eax
 8048c00:	ff 24 85 20 a2 04 08 	jmp    *0x804a220(,%eax,4)				#跳到0x804a220+4*%eax
 8048c07:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c0c:	eb 05                	jmp    8048c13 <phase_3+0x4f>
 8048c0e:	b8 4a 01 00 00       	mov    $0x14a,%eax
 8048c13:	2d d8 01 00 00       	sub    $0x1d8,%eax						#eax-0x1d8
 8048c18:	eb 05                	jmp    8048c1f <phase_3+0x5b>
 8048c1a:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c1f:	05 85 03 00 00       	add    $0x385,%eax						#%eax+0x385
 8048c24:	eb 05                	jmp    8048c2b <phase_3+0x67>
 8048c26:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c2b:	2d aa 03 00 00       	sub    $0x3aa,%eax						#%eax-0x3aa
 8048c30:	eb 05                	jmp    8048c37 <phase_3+0x73>
 8048c32:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c37:	05 aa 03 00 00       	add    $0x3aa,%eax						#%eax+0x3aa
 8048c3c:	eb 05                	jmp    8048c43 <phase_3+0x7f>
 8048c3e:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c43:	2d aa 03 00 00       	sub    $0x3aa,%eax						#%eax-0x3aa
 8048c48:	eb 05                	jmp    8048c4f <phase_3+0x8b>
 8048c4a:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c4f:	05 aa 03 00 00       	add    $0x3aa,%eax						#%eax+0x3aa
 8048c54:	eb 05                	jmp    8048c5b <phase_3+0x97>
 8048c56:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c5b:	2d aa 03 00 00       	sub    $0x3aa,%eax						#%eax-0x3aa
 8048c60:	eb 0a                	jmp    8048c6c <phase_3+0xa8>			#
 8048c62:	e8 8f 04 00 00       	call   80490f6 <explode_bomb>
 8048c67:	b8 00 00 00 00       	mov    $0x0,%eax
 8048c6c:	83 7c 24 18 05       	cmpl   $0x5,0x18(%esp)					#参数1需要小于5
 8048c71:	7f 06                	jg     8048c79 <phase_3+0xb5>			#参数1大于0x5爆炸
 8048c73:	3b 44 24 1c          	cmp    0x1c(%esp),%eax
 8048c77:	74 05                	je     8048c7e <phase_3+0xba>			#%eax等于参数2不爆炸
 8048c79:	e8 78 04 00 00       	call   80490f6 <explode_bomb>
 8048c7e:	83 c4 2c             	add    $0x2c,%esp
 8048c81:	c3                   	ret    

08048c82 <func4>:													#不是循环是递归口牙！！！
 8048c82:	83 ec 1c             	sub    $0x1c,%esp
 8048c85:	89 5c 24 10          	mov    %ebx,0x10(%esp)
 8048c89:	89 74 24 14          	mov    %esi,0x14(%esp)
 8048c8d:	89 7c 24 18          	mov    %edi,0x18(%esp)
 8048c91:	8b 74 24 20          	mov    0x20(%esp),%esi			#刚进递归%esi=8
 8048c95:	8b 5c 24 24          	mov    0x24(%esp),%ebx			#参数2是0x24(%esp)
 8048c99:	85 f6                	test   %esi,%esi				#
 8048c9b:	7e 2b                	jle    8048cc8 <func4+0x46>		#%esi==0结束递归，递归结束后多一步将%ebx置零
 8048c9d:	83 fe 01             	cmp    $0x1,%esi				#
 8048ca0:	74 2b                	je     8048ccd <func4+0x4b>		#%esi==1结束递归，但是递归结束后少了一步
 8048ca2:	89 5c 24 04          	mov    %ebx,0x4(%esp)
 8048ca6:	8d 46 ff             	lea    -0x1(%esi),%eax
 8048ca9:	89 04 24             	mov    %eax,(%esp)
 8048cac:	e8 d1 ff ff ff       	call   8048c82 <func4>
 8048cb1:	8d 3c 18             	lea    (%eax,%ebx,1),%edi
 8048cb4:	89 5c 24 04          	mov    %ebx,0x4(%esp)
 8048cb8:	83 ee 02             	sub    $0x2,%esi
 8048cbb:	89 34 24             	mov    %esi,(%esp)
 8048cbe:	e8 bf ff ff ff       	call   8048c82 <func4>
 8048cc3:	8d 1c 07             	lea    (%edi,%eax,1),%ebx
 8048cc6:	eb 05                	jmp    8048ccd <func4+0x4b>
 8048cc8:	bb 00 00 00 00       	mov    $0x0,%ebx
 8048ccd:	89 d8                	mov    %ebx,%eax				#重点在于这个%eax是多少
 8048ccf:	8b 5c 24 10          	mov    0x10(%esp),%ebx
 8048cd3:	8b 74 24 14          	mov    0x14(%esp),%esi
 8048cd7:	8b 7c 24 18          	mov    0x18(%esp),%edi
 8048cdb:	83 c4 1c             	add    $0x1c,%esp
 8048cde:	c3                   	ret    

08048cdf <phase_4>:
 8048cdf:	83 ec 2c             	sub    $0x2c,%esp
 8048ce2:	8d 44 24 18          	lea    0x18(%esp),%eax					 
 8048ce6:	89 44 24 0c          	mov    %eax,0xc(%esp)					#参数2 0x18(%esp)
 8048cea:	8d 44 24 1c          	lea    0x1c(%esp),%eax
 8048cee:	89 44 24 08          	mov    %eax,0x8(%esp)					#参数1 0x1c(%esp)
 8048cf2:	c7 44 24 04 e3 a3 04 	movl   $0x804a3e3,0x4(%esp)				#"%d %d %s" 隐藏入口
 8048cf9:	08 
 8048cfa:	8b 44 24 30          	mov    0x30(%esp),%eax
 8048cfe:	89 04 24             	mov    %eax,(%esp)
 8048d01:	e8 6a fb ff ff       	call   8048870 <__isoc99_sscanf@plt>
 8048d06:	83 f8 02             	cmp    $0x2,%eax						#
 8048d09:	75 0e                	jne    8048d19 <phase_4+0x3a>			#%eax!=0x2爆炸 参数个数!=2爆炸
 8048d0b:	8b 44 24 18          	mov    0x18(%esp),%eax
 8048d0f:	83 f8 01             	cmp    $0x1,%eax						#
 8048d12:	7e 05                	jle    8048d19 <phase_4+0x3a>			#参数2小于等于1爆炸
 8048d14:	83 f8 04             	cmp    $0x4,%eax						#
 8048d17:	7e 05                	jle    8048d1e <phase_4+0x3f>			#参数2小于等于4不炸		1<参数2<=4
 8048d19:	e8 d8 03 00 00       	call   80490f6 <explode_bomb>
 8048d1e:	8b 44 24 18          	mov    0x18(%esp),%eax
 8048d22:	89 44 24 04          	mov    %eax,0x4(%esp)
 8048d26:	c7 04 24 08 00 00 00 	movl   $0x8,(%esp)
 8048d2d:	e8 50 ff ff ff       	call   8048c82 <func4>
 8048d32:	3b 44 24 1c          	cmp    0x1c(%esp),%eax					#参数1和%eax相等不爆炸，%eax是？
 8048d36:	74 05                	je     8048d3d <phase_4+0x5e>
 8048d38:	e8 b9 03 00 00       	call   80490f6 <explode_bomb>
 8048d3d:	83 c4 2c             	add    $0x2c,%esp
 8048d40:	c3                   	ret    

08048d41 <phase_5>:
 8048d41:	83 ec 2c             	sub    $0x2c,%esp
 8048d44:	8d 44 24 1c          	lea    0x1c(%esp),%eax					#参数2: 0x1c(%esp)
 8048d48:	89 44 24 0c          	mov    %eax,0xc(%esp)
 8048d4c:	8d 44 24 18          	lea    0x18(%esp),%eax					#参数1: 0x18(%esp)
 8048d50:	89 44 24 08          	mov    %eax,0x8(%esp)
 8048d54:	c7 44 24 04 e3 a3 04 	movl   $0x804a3e3,0x4(%esp)				#"%d %d" 假隐藏
 8048d5b:	08 
 8048d5c:	8b 44 24 30          	mov    0x30(%esp),%eax
 8048d60:	89 04 24             	mov    %eax,(%esp)
 8048d63:	e8 08 fb ff ff       	call   8048870 <__isoc99_sscanf@plt>
 8048d68:	83 f8 01             	cmp    $0x1,%eax						#%eax是参数个数
 8048d6b:	7f 05                	jg     8048d72 <phase_5+0x31>			#参数个数大于1不爆炸
 8048d6d:	e8 84 03 00 00       	call   80490f6 <explode_bomb>
 8048d72:	8b 44 24 18          	mov    0x18(%esp),%eax					#将参数1加载到%eax
 8048d76:	83 e0 0f             	and    $0xf,%eax
 8048d79:	89 44 24 18          	mov    %eax,0x18(%esp)
 8048d7d:	83 f8 0f             	cmp    $0xf,%eax						#
 8048d80:	74 2a                	je     8048dac <phase_5+0x6b>			#%eax的二进制的后四位是1则爆炸，即参数1取16模余数为15
 8048d82:	b9 00 00 00 00       	mov    $0x0,%ecx
 8048d87:	ba 00 00 00 00       	mov    $0x0,%edx
 8048d8c:	83 c2 01             	add    $0x1,%edx						#循环在这里，每次循环edx+1
 8048d8f:	8b 04 85 40 a2 04 08 	mov    0x804a240(,%eax,4),%eax			#长度为16的数组，正好对应取16模
 8048d96:	01 c1                	add    %eax,%ecx
 8048d98:	83 f8 0f             	cmp    $0xf,%eax
 8048d9b:	75 ef                	jne    8048d8c <phase_5+0x4b>			#%eax==0xf退出循环 即array[6]
 8048d9d:	89 44 24 18          	mov    %eax,0x18(%esp)
 8048da1:	83 fa 0f             	cmp    $0xf,%edx						#
 8048da4:	75 06                	jne    8048dac <phase_5+0x6b>			#%edx要等于0xf 否则爆炸，也就是要循环15次
 8048da6:	3b 4c 24 1c          	cmp    0x1c(%esp),%ecx					#
 8048daa:	74 05                	je     8048db1 <phase_5+0x70>			#参数2要等于%ecx 否则爆炸
 8048dac:	e8 45 03 00 00       	call   80490f6 <explode_bomb>
 8048db1:	83 c4 2c             	add    $0x2c,%esp
 8048db4:	c3                   	ret    

08048db5 <phase_6>:															#算是看明白了，这是一个链表从小到大排序
 8048db5:	56                   	push   %esi
 8048db6:	53                   	push   %ebx
 8048db7:	83 ec 44             	sub    $0x44,%esp
 8048dba:	8d 44 24 10          	lea    0x10(%esp),%eax
 8048dbe:	89 44 24 04          	mov    %eax,0x4(%esp)
 8048dc2:	8b 44 24 50          	mov    0x50(%esp),%eax
 8048dc6:	89 04 24             	mov    %eax,(%esp)
 8048dc9:	e8 5d 04 00 00       	call   804922b <read_six_numbers>		#典中典之读6个数，
 8048dce:	be 00 00 00 00       	mov    $0x0,%esi						#参数1：0x10(%esp) 参数2：0x14(%esp)
 8048dd3:	8b 44 b4 10          	mov    0x10(%esp,%esi,4),%eax			#参数3：0x18(%esp) 参数4：0x1c(%esp)
 8048dd7:	83 e8 01             	sub    $0x1,%eax						#参数5：0x20(%esp) 参数6：0x24(%esp)
 8048dda:	83 f8 05             	cmp    $0x5,%eax						#%eax=参数1 - 1，
 8048ddd:	76 05                	jbe    8048de4 <phase_6+0x2f>			#%eax小于等于5不炸，参数1<=6。循环着发现所有参数都要满足这个约束条件
 8048ddf:	e8 12 03 00 00       	call   80490f6 <explode_bomb>
 8048de4:	83 c6 01             	add    $0x1,%esi
 8048de7:	83 fe 06             	cmp    $0x6,%esi
 8048dea:	74 33                	je     8048e1f <phase_6+0x6a>			#%esi等于6跳出循环
 8048dec:	89 f3                	mov    %esi,%ebx
 8048dee:	8b 44 9c 10          	mov    0x10(%esp,%ebx,4),%eax			#%eax=参数[%esi+1]
 8048df2:	39 44 b4 0c          	cmp    %eax,0xc(%esp,%esi,4)			#参数[%esi+2]
 8048df6:	75 05                	jne    8048dfd <phase_6+0x48>			#需要后一个参数不等于前一个参数
 8048df8:	e8 f9 02 00 00       	call   80490f6 <explode_bomb>
 8048dfd:	83 c3 01             	add    $0x1,%ebx
 8048e00:	83 fb 05             	cmp    $0x5,%ebx						#这是一个循环，要求所有的数都满足
 8048e03:	7e e9                	jle    8048dee <phase_6+0x39>			#“后一个参数不等于前一个参数”这个约束条件
 8048e05:	eb cc                	jmp    8048dd3 <phase_6+0x1e>
 8048e07:	8b 52 08             	mov    0x8(%edx),%edx					#%ecx>1多执行这段循环，%edx数组第三个数移到%edx
 8048e0a:	83 c0 01             	add    $0x1,%eax						#%eax+1
 8048e0d:	39 c8                	cmp    %ecx,%eax						#
 8048e0f:	75 f6                	jne    8048e07 <phase_6+0x52>			#循环到%ecx==%eax
 8048e11:	89 54 b4 28          	mov    %edx,0x28(%esp,%esi,4)			#
 8048e15:	83 c3 01             	add    $0x1,%ebx						#%ebx+1
 8048e18:	83 fb 06             	cmp    $0x6,%ebx						#
 8048e1b:	75 07                	jne    8048e24 <phase_6+0x6f>			#%ebx不等于6继续循环
 8048e1d:	eb 1c                	jmp    8048e3b <phase_6+0x86>
 8048e1f:	bb 00 00 00 00       	mov    $0x0,%ebx						#跳到这
 8048e24:	89 de                	mov    %ebx,%esi						#%ebx和%esi清零
 8048e26:	8b 4c 9c 10          	mov    0x10(%esp,%ebx,4),%ecx			#前有参数数组 %ecx=参数[%ebx+1]
 8048e2a:	b8 01 00 00 00       	mov    $0x1,%eax
 8048e2f:	ba 3c c1 04 08       	mov    $0x804c13c,%edx					#这是个数组
 8048e34:	83 f9 01             	cmp    $0x1,%ecx						#%ecx>1多执行一段小循环
 8048e37:	7f ce                	jg     8048e07 <phase_6+0x52>			#
 8048e39:	eb d6                	jmp    8048e11 <phase_6+0x5c>
 8048e3b:	8b 5c 24 28          	mov    0x28(%esp),%ebx					#此时%ebx=6跳到这，
 8048e3f:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8048e43:	89 43 08             	mov    %eax,0x8(%ebx)
 8048e46:	8b 54 24 30          	mov    0x30(%esp),%edx
 8048e4a:	89 50 08             	mov    %edx,0x8(%eax)
 8048e4d:	8b 44 24 34          	mov    0x34(%esp),%eax
 8048e51:	89 42 08             	mov    %eax,0x8(%edx)
 8048e54:	8b 54 24 38          	mov    0x38(%esp),%edx
 8048e58:	89 50 08             	mov    %edx,0x8(%eax)
 8048e5b:	8b 44 24 3c          	mov    0x3c(%esp),%eax
 8048e5f:	89 42 08             	mov    %eax,0x8(%edx)
 8048e62:	c7 40 08 00 00 00 00 	movl   $0x0,0x8(%eax)
 8048e69:	be 05 00 00 00       	mov    $0x5,%esi
 8048e6e:	8b 43 08             	mov    0x8(%ebx),%eax
 8048e71:	8b 10                	mov    (%eax),%edx
 8048e73:	39 13                	cmp    %edx,(%ebx)						#
 8048e75:	7e 05                	jle    8048e7c <phase_6+0xc7>			#(%ebx)要小于等于%edx，否则爆炸
 8048e77:	e8 7a 02 00 00       	call   80490f6 <explode_bomb>
 8048e7c:	8b 5b 08             	mov    0x8(%ebx),%ebx
 8048e7f:	83 ee 01             	sub    $0x1,%esi						#
 8048e82:	75 ea                	jne    8048e6e <phase_6+0xb9>			#%esi不等于1继续循环
 8048e84:	83 c4 44             	add    $0x44,%esp
 8048e87:	5b                   	pop    %ebx
 8048e88:	5e                   	pop    %esi
 8048e89:	c3                   	ret    

08048e8a <fun7>:															#这是一个巨大的二叉树
 8048e8a:	53                   	push   %ebx
 8048e8b:	83 ec 18             	sub    $0x18,%esp
 8048e8e:	8b 54 24 20          	mov    0x20(%esp),%edx					#%edx是子节点指针
 8048e92:	8b 4c 24 24          	mov    0x24(%esp),%ecx					#%ecx就是输入的参数
 8048e96:	85 d2                	test   %edx,%edx						#
 8048e98:	74 37                	je     8048ed1 <fun7+0x47>				#子节点指针等于0 return
 8048e9a:	8b 1a                	mov    (%edx),%ebx
 8048e9c:	39 cb                	cmp    %ecx,%ebx						#%ebx是root
 8048e9e:	7e 13                	jle    8048eb3 <fun7+0x29>				#参数>=root跳转
 8048ea0:	89 4c 24 04          	mov    %ecx,0x4(%esp)
 8048ea4:	8b 42 04             	mov    0x4(%edx),%eax
 8048ea7:	89 04 24             	mov    %eax,(%esp)
 8048eaa:	e8 db ff ff ff       	call   8048e8a <fun7>					#递归
 8048eaf:	01 c0                	add    %eax,%eax						#%eax*2
 8048eb1:	eb 23                	jmp    8048ed6 <fun7+0x4c>
 8048eb3:	b8 00 00 00 00       	mov    $0x0,%eax						#%eax置零
 8048eb8:	39 cb                	cmp    %ecx,%ebx						#
 8048eba:	74 1a                	je     8048ed6 <fun7+0x4c>				#参数==root return
 8048ebc:	89 4c 24 04          	mov    %ecx,0x4(%esp)					#参数>root eax*2+1
 8048ec0:	8b 42 08             	mov    0x8(%edx),%eax
 8048ec3:	89 04 24             	mov    %eax,(%esp)
 8048ec6:	e8 bf ff ff ff       	call   8048e8a <fun7>
 8048ecb:	8d 44 00 01          	lea    0x1(%eax,%eax,1),%eax			#eax*2+1
 8048ecf:	eb 05                	jmp    8048ed6 <fun7+0x4c>
 8048ed1:	b8 ff ff ff ff       	mov    $0xffffffff,%eax					#子节点指针为空返回-1
 8048ed6:	83 c4 18             	add    $0x18,%esp						#参数==root return 0
 8048ed9:	5b                   	pop    %ebx
 8048eda:	c3                   	ret    

08048edb <secret_phase>:													#宫崎英高儿子上幼儿园要打开隐藏墙壁
 8048edb:	53                   	push   %ebx
 8048edc:	83 ec 18             	sub    $0x18,%esp
 8048edf:	e8 39 02 00 00       	call   804911d <read_line>
 8048ee4:	c7 44 24 08 0a 00 00 	movl   $0xa,0x8(%esp)
 8048eeb:	00 
 8048eec:	c7 44 24 04 00 00 00 	movl   $0x0,0x4(%esp)
 8048ef3:	00 
 8048ef4:	89 04 24             	mov    %eax,(%esp)
 8048ef7:	e8 e4 f9 ff ff       	call   80488e0 <strtol@plt>
 8048efc:	89 c3                	mov    %eax,%ebx
 8048efe:	8d 40 ff             	lea    -0x1(%eax),%eax
 8048f01:	3d e8 03 00 00       	cmp    $0x3e8,%eax						#
 8048f06:	76 05                	jbe    8048f0d <secret_phase+0x32>		#参数1小于0x3e8
 8048f08:	e8 e9 01 00 00       	call   80490f6 <explode_bomb>
 8048f0d:	89 5c 24 04          	mov    %ebx,0x4(%esp)
 8048f11:	c7 04 24 88 c0 04 08 	movl   $0x804c088,(%esp)
 8048f18:	e8 6d ff ff ff       	call   8048e8a <fun7>
 8048f1d:	83 f8 03             	cmp    $0x3,%eax						#
 8048f20:	74 05                	je     8048f27 <secret_phase+0x4c>		#%eax等于3，不然就爆
 8048f22:	e8 cf 01 00 00       	call   80490f6 <explode_bomb>
 8048f27:	c7 04 24 f0 a1 04 08 	movl   $0x804a1f0,(%esp)
 8048f2e:	e8 cd f8 ff ff       	call   8048800 <puts@plt>
 8048f33:	e8 43 03 00 00       	call   804927b <phase_defused>
 8048f38:	83 c4 18             	add    $0x18,%esp
 8048f3b:	5b                   	pop    %ebx
 8048f3c:	c3                   	ret    
 8048f3d:	90                   	nop
 8048f3e:	90                   	nop
 8048f3f:	90                   	nop

08048f40 <sig_handler>:
 8048f40:	83 ec 1c             	sub    $0x1c,%esp
 8048f43:	c7 04 24 80 a2 04 08 	movl   $0x804a280,(%esp)
 8048f4a:	e8 b1 f8 ff ff       	call   8048800 <puts@plt>
 8048f4f:	c7 04 24 03 00 00 00 	movl   $0x3,(%esp)
 8048f56:	e8 55 f8 ff ff       	call   80487b0 <sleep@plt>
 8048f5b:	c7 44 24 04 42 a3 04 	movl   $0x804a342,0x4(%esp)
 8048f62:	08 
 8048f63:	c7 04 24 01 00 00 00 	movl   $0x1,(%esp)
 8048f6a:	e8 31 f9 ff ff       	call   80488a0 <__printf_chk@plt>
 8048f6f:	a1 c0 c3 04 08       	mov    0x804c3c0,%eax
 8048f74:	89 04 24             	mov    %eax,(%esp)
 8048f77:	e8 04 f8 ff ff       	call   8048780 <fflush@plt>
 8048f7c:	c7 04 24 01 00 00 00 	movl   $0x1,(%esp)
 8048f83:	e8 28 f8 ff ff       	call   80487b0 <sleep@plt>
 8048f88:	c7 04 24 4a a3 04 08 	movl   $0x804a34a,(%esp)
 8048f8f:	e8 6c f8 ff ff       	call   8048800 <puts@plt>
 8048f94:	c7 04 24 10 00 00 00 	movl   $0x10,(%esp)
 8048f9b:	e8 a0 f8 ff ff       	call   8048840 <exit@plt>

08048fa0 <invalid_phase>:
 8048fa0:	83 ec 1c             	sub    $0x1c,%esp
 8048fa3:	8b 44 24 20          	mov    0x20(%esp),%eax
 8048fa7:	89 44 24 08          	mov    %eax,0x8(%esp)
 8048fab:	c7 44 24 04 52 a3 04 	movl   $0x804a352,0x4(%esp)
 8048fb2:	08 
 8048fb3:	c7 04 24 01 00 00 00 	movl   $0x1,(%esp)
 8048fba:	e8 e1 f8 ff ff       	call   80488a0 <__printf_chk@plt>
 8048fbf:	c7 04 24 08 00 00 00 	movl   $0x8,(%esp)
 8048fc6:	e8 75 f8 ff ff       	call   8048840 <exit@plt>

08048fcb <string_length>:
 8048fcb:	8b 54 24 04          	mov    0x4(%esp),%edx						#将0x4(%esp)的值加载到%edx
 8048fcf:	b8 00 00 00 00       	mov    $0x0,%eax							#将0x0加载到%eax
 8048fd4:	80 3a 00             	cmpb   $0x0,(%edx)							#比较0x0和%edx指向的地址的值
 8048fd7:	74 09                	je     8048fe2 <string_length+0x17>			#如果(%edx)==0x0则跳转到0x8048fe2 <string_length+0x17>
 8048fd9:	83 c0 01             	add    $0x1,%eax							#%eax+0x1
 8048fdc:	80 3c 02 00          	cmpb   $0x0,(%edx,%eax,1)					#比较0x0和(%edx,%eax,1)，即%edx的后%eax个字节
 8048fe0:	75 f7                	jne    8048fd9 <string_length+0xe>			#若为0则跳转
 8048fe2:	f3 c3                	repz ret 

08048fe4 <strings_not_equal>:
 8048fe4:	83 ec 10             	sub    $0x10,%esp							#%esp向下移动4字节
 8048fe7:	89 5c 24 04          	mov    %ebx,0x4(%esp)						#将%ebx的值存储到0x4(%esp)
 8048feb:	89 74 24 08          	mov    %esi,0x8(%esp)						#将%esi的值存储到0x8(%esp)
 8048fef:	89 7c 24 0c          	mov    %edi,0xc(%esp)						#将%edi的值存储到0xc(%esp)
 8048ff3:	8b 5c 24 14          	mov    0x14(%esp),%ebx						#将0x14(%esp)的值加载到%ebx 输入的字符串的首地址
 8048ff7:	8b 74 24 18          	mov    0x18(%esp),%esi						#将0x18(%esp)的值加载到%esi 预设的字符串的首地址
 8048ffb:	89 1c 24             	mov    %ebx,(%esp)							#将%ebx的值存储到%esp指向的地址
 8048ffe:	e8 c8 ff ff ff       	call   8048fcb <string_length>				#调用函数0x8048fcb <string_length> 这里是返回输入的字符串的长度
 8049003:	89 c7                	mov    %eax,%edi							#将%eax的值加载到%edi，即0x4(%esp)起的非0字节长度
 8049005:	89 34 24             	mov    %esi,(%esp)							#将%esi的值加载到(%esp)
 8049008:	e8 be ff ff ff       	call   8048fcb <string_length>				#调用函数0x8048fcb <string_length> 这里是返回预设的字符串的长度
 804900d:	ba 01 00 00 00       	mov    $0x1,%edx
 8049012:	39 c7                	cmp    %eax,%edi							#strings_not_equal+0x2E
 8049014:	75 33                	jne    8049049 <strings_not_equal+0x65>		#%eax和%edi不相等时跳转到0x8049049 <strings_not_equal+0x65>
 8049016:	0f b6 03             	movzbl (%ebx),%eax							#将%ebx指向的地址的值拷贝到%eax，高24位补0
 8049019:	b2 00                	mov    $0x0,%dl								
 804901b:	84 c0                	test   %al,%al
 804901d:	74 2a                	je     8049049 <strings_not_equal+0x65>
 804901f:	b2 01                	mov    $0x1,%dl
 8049021:	3a 06                	cmp    (%esi),%al
 8049023:	75 24                	jne    8049049 <strings_not_equal+0x65>
 8049025:	b8 00 00 00 00       	mov    $0x0,%eax
 804902a:	eb 08                	jmp    8049034 <strings_not_equal+0x50>
 804902c:	83 c0 01             	add    $0x1,%eax							#
 804902f:	3a 14 06             	cmp    (%esi,%eax,1),%dl					#
 8049032:	75 10                	jne    8049044 <strings_not_equal+0x60>		#这里是一个循环
 8049034:	0f b6 54 03 01       	movzbl 0x1(%ebx,%eax,1),%edx				#判断各个字符是否相等
 8049039:	84 d2                	test   %dl,%dl								#
 804903b:	75 ef                	jne    804902c <strings_not_equal+0x48>		#
 804903d:	ba 00 00 00 00       	mov    $0x0,%edx
 8049042:	eb 05                	jmp    8049049 <strings_not_equal+0x65>
 8049044:	ba 01 00 00 00       	mov    $0x1,%edx							#跳转到这里代表成功了<strings_not_equal+0x60>
 8049049:	89 d0                	mov    %edx,%eax							#跳转到这里代表失败了<strings_not_equal+0x65>
 804904b:	8b 5c 24 04          	mov    0x4(%esp),%ebx
 804904f:	8b 74 24 08          	mov    0x8(%esp),%esi
 8049053:	8b 7c 24 0c          	mov    0xc(%esp),%edi
 8049057:	83 c4 10             	add    $0x10,%esp
 804905a:	c3                   	ret    

0804905b <initialize_bomb>:
 804905b:	83 ec 1c             	sub    $0x1c,%esp					#%esp向下移7字节
 804905e:	c7 44 24 04 40 8f 04 	movl   $0x8048f40,0x4(%esp)			#将地址0x8048f40的值（83 ec 1c）存储到0x4(%esp)处
 8049065:	08 
 8049066:	c7 04 24 02 00 00 00 	movl   $0x2,(%esp)					#将0x2存储到%esp
 804906d:	e8 2e f7 ff ff       	call   80487a0 <signal@plt>			#调用函数0x80487a0 <signal@plt>
 8049072:	83 c4 1c             	add    $0x1c,%esp
 8049075:	c3                   	ret    

08049076 <initialize_bomb_solve>:
 8049076:	f3 c3                	repz ret 

08049078 <blank_line>:
 8049078:	56                   	push   %esi
 8049079:	53                   	push   %ebx
 804907a:	83 ec 04             	sub    $0x4,%esp
 804907d:	8b 74 24 10          	mov    0x10(%esp),%esi
 8049081:	eb 14                	jmp    8049097 <blank_line+0x1f>
 8049083:	e8 88 f8 ff ff       	call   8048910 <__ctype_b_loc@plt>
 8049088:	83 c6 01             	add    $0x1,%esi
 804908b:	0f be db             	movsbl %bl,%ebx
 804908e:	8b 00                	mov    (%eax),%eax
 8049090:	f6 44 58 01 20       	testb  $0x20,0x1(%eax,%ebx,2)
 8049095:	74 0e                	je     80490a5 <blank_line+0x2d>
 8049097:	0f b6 1e             	movzbl (%esi),%ebx
 804909a:	84 db                	test   %bl,%bl
 804909c:	75 e5                	jne    8049083 <blank_line+0xb>
 804909e:	b8 01 00 00 00       	mov    $0x1,%eax
 80490a3:	eb 05                	jmp    80490aa <blank_line+0x32>
 80490a5:	b8 00 00 00 00       	mov    $0x0,%eax
 80490aa:	83 c4 04             	add    $0x4,%esp
 80490ad:	5b                   	pop    %ebx
 80490ae:	5e                   	pop    %esi
 80490af:	c3                   	ret    

080490b0 <skip>:
 80490b0:	53                   	push   %ebx
 80490b1:	83 ec 18             	sub    $0x18,%esp
 80490b4:	a1 d0 c3 04 08       	mov    0x804c3d0,%eax
 80490b9:	89 44 24 08          	mov    %eax,0x8(%esp)
 80490bd:	c7 44 24 04 50 00 00 	movl   $0x50,0x4(%esp)
 80490c4:	00 
 80490c5:	a1 cc c3 04 08       	mov    0x804c3cc,%eax
 80490ca:	8d 04 80             	lea    (%eax,%eax,4),%eax
 80490cd:	c1 e0 04             	shl    $0x4,%eax
 80490d0:	05 e0 c3 04 08       	add    $0x804c3e0,%eax
 80490d5:	89 04 24             	mov    %eax,(%esp)
 80490d8:	e8 b3 f6 ff ff       	call   8048790 <fgets@plt>
 80490dd:	89 c3                	mov    %eax,%ebx
 80490df:	85 c0                	test   %eax,%eax
 80490e1:	74 0c                	je     80490ef <skip+0x3f>
 80490e3:	89 04 24             	mov    %eax,(%esp)
 80490e6:	e8 8d ff ff ff       	call   8049078 <blank_line>
 80490eb:	85 c0                	test   %eax,%eax
 80490ed:	75 c5                	jne    80490b4 <skip+0x4>
 80490ef:	89 d8                	mov    %ebx,%eax
 80490f1:	83 c4 18             	add    $0x18,%esp
 80490f4:	5b                   	pop    %ebx
 80490f5:	c3                   	ret    

080490f6 <explode_bomb>:
 80490f6:	83 ec 1c             	sub    $0x1c,%esp
 80490f9:	c7 04 24 63 a3 04 08 	movl   $0x804a363,(%esp)
 8049100:	e8 fb f6 ff ff       	call   8048800 <puts@plt>
 8049105:	c7 04 24 6c a3 04 08 	movl   $0x804a36c,(%esp)
 804910c:	e8 ef f6 ff ff       	call   8048800 <puts@plt>
 8049111:	c7 04 24 08 00 00 00 	movl   $0x8,(%esp)
 8049118:	e8 23 f7 ff ff       	call   8048840 <exit@plt>

0804911d <read_line>:
 804911d:	83 ec 2c             	sub    $0x2c,%esp
 8049120:	89 5c 24 20          	mov    %ebx,0x20(%esp)
 8049124:	89 74 24 24          	mov    %esi,0x24(%esp)
 8049128:	89 7c 24 28          	mov    %edi,0x28(%esp)
 804912c:	e8 7f ff ff ff       	call   80490b0 <skip>
 8049131:	85 c0                	test   %eax,%eax
 8049133:	75 6c                	jne    80491a1 <read_line+0x84>
 8049135:	a1 a4 c3 04 08       	mov    0x804c3a4,%eax
 804913a:	39 05 d0 c3 04 08    	cmp    %eax,0x804c3d0
 8049140:	75 18                	jne    804915a <read_line+0x3d>
 8049142:	c7 04 24 83 a3 04 08 	movl   $0x804a383,(%esp)
 8049149:	e8 b2 f6 ff ff       	call   8048800 <puts@plt>
 804914e:	c7 04 24 08 00 00 00 	movl   $0x8,(%esp)
 8049155:	e8 e6 f6 ff ff       	call   8048840 <exit@plt>
 804915a:	c7 04 24 a1 a3 04 08 	movl   $0x804a3a1,(%esp)
 8049161:	e8 8a f6 ff ff       	call   80487f0 <getenv@plt>
 8049166:	85 c0                	test   %eax,%eax
 8049168:	74 0c                	je     8049176 <read_line+0x59>
 804916a:	c7 04 24 00 00 00 00 	movl   $0x0,(%esp)
 8049171:	e8 ca f6 ff ff       	call   8048840 <exit@plt>
 8049176:	a1 a4 c3 04 08       	mov    0x804c3a4,%eax
 804917b:	a3 d0 c3 04 08       	mov    %eax,0x804c3d0
 8049180:	e8 2b ff ff ff       	call   80490b0 <skip>
 8049185:	85 c0                	test   %eax,%eax
 8049187:	75 18                	jne    80491a1 <read_line+0x84>
 8049189:	c7 04 24 83 a3 04 08 	movl   $0x804a383,(%esp)
 8049190:	e8 6b f6 ff ff       	call   8048800 <puts@plt>
 8049195:	c7 04 24 00 00 00 00 	movl   $0x0,(%esp)
 804919c:	e8 9f f6 ff ff       	call   8048840 <exit@plt>
 80491a1:	8b 15 cc c3 04 08    	mov    0x804c3cc,%edx
 80491a7:	8d 1c 92             	lea    (%edx,%edx,4),%ebx
 80491aa:	c1 e3 04             	shl    $0x4,%ebx
 80491ad:	81 c3 e0 c3 04 08    	add    $0x804c3e0,%ebx
 80491b3:	89 df                	mov    %ebx,%edi
 80491b5:	b8 00 00 00 00       	mov    $0x0,%eax
 80491ba:	b9 ff ff ff ff       	mov    $0xffffffff,%ecx
 80491bf:	f2 ae                	repnz scas %es:(%edi),%al
 80491c1:	f7 d1                	not    %ecx
 80491c3:	83 e9 01             	sub    $0x1,%ecx
 80491c6:	83 f9 4e             	cmp    $0x4e,%ecx
 80491c9:	7e 37                	jle    8049202 <read_line+0xe5>
 80491cb:	c7 04 24 ac a3 04 08 	movl   $0x804a3ac,(%esp)
 80491d2:	e8 29 f6 ff ff       	call   8048800 <puts@plt>
 80491d7:	a1 cc c3 04 08       	mov    0x804c3cc,%eax
 80491dc:	8d 50 01             	lea    0x1(%eax),%edx
 80491df:	89 15 cc c3 04 08    	mov    %edx,0x804c3cc
 80491e5:	6b c0 50             	imul   $0x50,%eax,%eax
 80491e8:	05 e0 c3 04 08       	add    $0x804c3e0,%eax
 80491ed:	ba c7 a3 04 08       	mov    $0x804a3c7,%edx
 80491f2:	b9 04 00 00 00       	mov    $0x4,%ecx
 80491f7:	89 c7                	mov    %eax,%edi
 80491f9:	89 d6                	mov    %edx,%esi
 80491fb:	f3 a5                	rep movsl %ds:(%esi),%es:(%edi)
 80491fd:	e8 f4 fe ff ff       	call   80490f6 <explode_bomb>
 8049202:	8d 04 92             	lea    (%edx,%edx,4),%eax
 8049205:	c1 e0 04             	shl    $0x4,%eax
 8049208:	c6 84 01 df c3 04 08 	movb   $0x0,0x804c3df(%ecx,%eax,1)
 804920f:	00 
 8049210:	83 c2 01             	add    $0x1,%edx
 8049213:	89 15 cc c3 04 08    	mov    %edx,0x804c3cc
 8049219:	89 d8                	mov    %ebx,%eax
 804921b:	8b 5c 24 20          	mov    0x20(%esp),%ebx
 804921f:	8b 74 24 24          	mov    0x24(%esp),%esi
 8049223:	8b 7c 24 28          	mov    0x28(%esp),%edi
 8049227:	83 c4 2c             	add    $0x2c,%esp
 804922a:	c3                   	ret    

0804922b <read_six_numbers>:
 804922b:	83 ec 2c             	sub    $0x2c,%esp							#地址从高到低，参数从低到高 32位传参用栈
 804922e:	8b 44 24 34          	mov    0x34(%esp),%eax
 8049232:	8d 50 14             	lea    0x14(%eax),%edx
 8049235:	89 54 24 1c          	mov    %edx,0x1c(%esp)						#第一个参数
 8049239:	8d 50 10             	lea    0x10(%eax),%edx
 804923c:	89 54 24 18          	mov    %edx,0x18(%esp)						#第二个参数
 8049240:	8d 50 0c             	lea    0xc(%eax),%edx
 8049243:	89 54 24 14          	mov    %edx,0x14(%esp)						#第三个参数
 8049247:	8d 50 08             	lea    0x8(%eax),%edx
 804924a:	89 54 24 10          	mov    %edx,0x10(%esp)						#第四个参数
 804924e:	8d 50 04             	lea    0x4(%eax),%edx
 8049251:	89 54 24 0c          	mov    %edx,0xc(%esp)						#第五个参数
 8049255:	89 44 24 08          	mov    %eax,0x8(%esp)						#第六个参数
 8049259:	c7 44 24 04 d7 a3 04 	movl   $0x804a3d7,0x4(%esp)					#地址0x804a3d7 <read_six_numbers>存储到0x4(%esp)
 8049260:	08 
 8049261:	8b 44 24 30          	mov    0x30(%esp),%eax
 8049265:	89 04 24             	mov    %eax,(%esp)
 8049268:	e8 03 f6 ff ff       	call   8048870 <__isoc99_sscanf@plt>
 804926d:	83 f8 05             	cmp    $0x5,%eax
 8049270:	7f 05                	jg     8049277 <read_six_numbers+0x4c>		#%eax>0x5时不引爆炸弹
 8049272:	e8 7f fe ff ff       	call   80490f6 <explode_bomb>
 8049277:	83 c4 2c             	add    $0x2c,%esp
 804927a:	c3                   	ret    

0804927b <phase_defused>:														#前有隐藏
 804927b:	81 ec 8c 00 00 00    	sub    $0x8c,%esp
 8049281:	65 a1 14 00 00 00    	mov    %gs:0x14,%eax
 8049287:	89 44 24 7c          	mov    %eax,0x7c(%esp)
 804928b:	31 c0                	xor    %eax,%eax
 804928d:	83 3d cc c3 04 08 06 	cmpl   $0x6,0x804c3cc						#存的过关数量
 8049294:	75 72                	jne    8049308 <phase_defused+0x8d>
 8049296:	8d 44 24 2c          	lea    0x2c(%esp),%eax
 804929a:	89 44 24 10          	mov    %eax,0x10(%esp)
 804929e:	8d 44 24 28          	lea    0x28(%esp),%eax
 80492a2:	89 44 24 0c          	mov    %eax,0xc(%esp)
 80492a6:	8d 44 24 24          	lea    0x24(%esp),%eax
 80492aa:	89 44 24 08          	mov    %eax,0x8(%esp)
 80492ae:	c7 44 24 04 e9 a3 04 	movl   $0x804a3e9,0x4(%esp)					#"%d %d %s"
 80492b5:	08 
 80492b6:	c7 04 24 d0 c4 04 08 	movl   $0x804c4d0,(%esp)					#这里存的正是phase_4输入的内容，隐藏门从phase_4进
 80492bd:	e8 ae f5 ff ff       	call   8048870 <__isoc99_sscanf@plt>
 80492c2:	83 f8 03             	cmp    $0x3,%eax
 80492c5:	75 35                	jne    80492fc <phase_defused+0x81>
 80492c7:	c7 44 24 04 f2 a3 04 	movl   $0x804a3f2,0x4(%esp)				#需要判断是否相等的字符串"Lancer"
 80492ce:	08 
 80492cf:	8d 44 24 2c          	lea    0x2c(%esp),%eax
 80492d3:	89 04 24             	mov    %eax,(%esp)
 80492d6:	e8 09 fd ff ff       	call   8048fe4 <strings_not_equal>
 80492db:	85 c0                	test   %eax,%eax
 80492dd:	75 1d                	jne    80492fc <phase_defused+0x81>		#
 80492df:	c7 04 24 b8 a2 04 08 	movl   $0x804a2b8,(%esp)
 80492e6:	e8 15 f5 ff ff       	call   8048800 <puts@plt>
 80492eb:	c7 04 24 e0 a2 04 08 	movl   $0x804a2e0,(%esp)
 80492f2:	e8 09 f5 ff ff       	call   8048800 <puts@plt>				
 80492f7:	e8 df fb ff ff       	call   8048edb <secret_phase>			#字符串匹配进隐藏门
 80492fc:	c7 04 24 18 a3 04 08 	movl   $0x804a318,(%esp)
 8049303:	e8 f8 f4 ff ff       	call   8048800 <puts@plt>
 8049308:	8b 44 24 7c          	mov    0x7c(%esp),%eax
 804930c:	65 33 05 14 00 00 00 	xor    %gs:0x14,%eax
 8049313:	74 05                	je     804931a <phase_defused+0x9f>
 8049315:	e8 b6 f4 ff ff       	call   80487d0 <__stack_chk_fail@plt>
 804931a:	81 c4 8c 00 00 00    	add    $0x8c,%esp
 8049320:	c3                   	ret    
 8049321:	90                   	nop
 8049322:	90                   	nop
 8049323:	90                   	nop
 8049324:	90                   	nop
 8049325:	90                   	nop
 8049326:	90                   	nop
 8049327:	90                   	nop
 8049328:	90                   	nop
 8049329:	90                   	nop
 804932a:	90                   	nop
 804932b:	90                   	nop
 804932c:	90                   	nop
 804932d:	90                   	nop
 804932e:	90                   	nop
 804932f:	90                   	nop

08049330 <rio_readlineb>:
 8049330:	55                   	push   %ebp
 8049331:	57                   	push   %edi
 8049332:	56                   	push   %esi
 8049333:	53                   	push   %ebx
 8049334:	83 ec 3c             	sub    $0x3c,%esp
 8049337:	89 c3                	mov    %eax,%ebx
 8049339:	83 f9 01             	cmp    $0x1,%ecx
 804933c:	0f 86 bb 00 00 00    	jbe    80493fd <rio_readlineb+0xcd>
 8049342:	89 4c 24 1c          	mov    %ecx,0x1c(%esp)
 8049346:	89 54 24 18          	mov    %edx,0x18(%esp)
 804934a:	bd 01 00 00 00       	mov    $0x1,%ebp
 804934f:	8d 78 0c             	lea    0xc(%eax),%edi
 8049352:	eb 3c                	jmp    8049390 <rio_readlineb+0x60>
 8049354:	c7 44 24 08 00 20 00 	movl   $0x2000,0x8(%esp)
 804935b:	00 
 804935c:	89 7c 24 04          	mov    %edi,0x4(%esp)
 8049360:	8b 03                	mov    (%ebx),%eax
 8049362:	89 04 24             	mov    %eax,(%esp)
 8049365:	e8 06 f4 ff ff       	call   8048770 <read@plt>
 804936a:	89 43 04             	mov    %eax,0x4(%ebx)
 804936d:	85 c0                	test   %eax,%eax
 804936f:	79 14                	jns    8049385 <rio_readlineb+0x55>
 8049371:	e8 1a f5 ff ff       	call   8048890 <__errno_location@plt>
 8049376:	83 38 04             	cmpl   $0x4,(%eax)
 8049379:	74 15                	je     8049390 <rio_readlineb+0x60>
 804937b:	90                   	nop
 804937c:	8d 74 26 00          	lea    0x0(%esi,%eiz,1),%esi
 8049380:	e9 a0 00 00 00       	jmp    8049425 <rio_readlineb+0xf5>
 8049385:	85 c0                	test   %eax,%eax
 8049387:	0f 84 9f 00 00 00    	je     804942c <rio_readlineb+0xfc>
 804938d:	89 7b 08             	mov    %edi,0x8(%ebx)
 8049390:	8b 73 04             	mov    0x4(%ebx),%esi
 8049393:	85 f6                	test   %esi,%esi
 8049395:	7e bd                	jle    8049354 <rio_readlineb+0x24>
 8049397:	85 f6                	test   %esi,%esi
 8049399:	0f 85 96 00 00 00    	jne    8049435 <rio_readlineb+0x105>
 804939f:	c7 44 24 0c 01 00 00 	movl   $0x1,0xc(%esp)
 80493a6:	00 
 80493a7:	89 74 24 08          	mov    %esi,0x8(%esp)
 80493ab:	8b 43 08             	mov    0x8(%ebx),%eax
 80493ae:	89 44 24 04          	mov    %eax,0x4(%esp)
 80493b2:	8d 44 24 2f          	lea    0x2f(%esp),%eax
 80493b6:	89 04 24             	mov    %eax,(%esp)
 80493b9:	e8 62 f4 ff ff       	call   8048820 <__memcpy_chk@plt>
 80493be:	01 73 08             	add    %esi,0x8(%ebx)
 80493c1:	29 73 04             	sub    %esi,0x4(%ebx)
 80493c4:	83 fe 01             	cmp    $0x1,%esi
 80493c7:	75 18                	jne    80493e1 <rio_readlineb+0xb1>
 80493c9:	0f b6 44 24 2f       	movzbl 0x2f(%esp),%eax
 80493ce:	8b 54 24 18          	mov    0x18(%esp),%edx
 80493d2:	88 02                	mov    %al,(%edx)
 80493d4:	83 c2 01             	add    $0x1,%edx
 80493d7:	89 54 24 18          	mov    %edx,0x18(%esp)
 80493db:	3c 0a                	cmp    $0xa,%al
 80493dd:	75 13                	jne    80493f2 <rio_readlineb+0xc2>
 80493df:	eb 25                	jmp    8049406 <rio_readlineb+0xd6>
 80493e1:	89 e8                	mov    %ebp,%eax
 80493e3:	85 f6                	test   %esi,%esi
 80493e5:	75 28                	jne    804940f <rio_readlineb+0xdf>
 80493e7:	83 f8 01             	cmp    $0x1,%eax
 80493ea:	75 1a                	jne    8049406 <rio_readlineb+0xd6>
 80493ec:	8d 74 26 00          	lea    0x0(%esi,%eiz,1),%esi
 80493f0:	eb 24                	jmp    8049416 <rio_readlineb+0xe6>
 80493f2:	83 c5 01             	add    $0x1,%ebp
 80493f5:	3b 6c 24 1c          	cmp    0x1c(%esp),%ebp
 80493f9:	75 95                	jne    8049390 <rio_readlineb+0x60>
 80493fb:	eb 09                	jmp    8049406 <rio_readlineb+0xd6>
 80493fd:	89 54 24 18          	mov    %edx,0x18(%esp)
 8049401:	bd 01 00 00 00       	mov    $0x1,%ebp
 8049406:	8b 44 24 18          	mov    0x18(%esp),%eax
 804940a:	c6 00 00             	movb   $0x0,(%eax)
 804940d:	eb 0c                	jmp    804941b <rio_readlineb+0xeb>
 804940f:	bd ff ff ff ff       	mov    $0xffffffff,%ebp
 8049414:	eb 05                	jmp    804941b <rio_readlineb+0xeb>
 8049416:	bd 00 00 00 00       	mov    $0x0,%ebp
 804941b:	89 e8                	mov    %ebp,%eax
 804941d:	83 c4 3c             	add    $0x3c,%esp
 8049420:	5b                   	pop    %ebx
 8049421:	5e                   	pop    %esi
 8049422:	5f                   	pop    %edi
 8049423:	5d                   	pop    %ebp
 8049424:	c3                   	ret    
 8049425:	be ff ff ff ff       	mov    $0xffffffff,%esi
 804942a:	eb 05                	jmp    8049431 <rio_readlineb+0x101>
 804942c:	be 00 00 00 00       	mov    $0x0,%esi
 8049431:	89 e8                	mov    %ebp,%eax
 8049433:	eb ae                	jmp    80493e3 <rio_readlineb+0xb3>
 8049435:	8b 43 08             	mov    0x8(%ebx),%eax
 8049438:	0f b6 00             	movzbl (%eax),%eax
 804943b:	88 44 24 2f          	mov    %al,0x2f(%esp)
 804943f:	83 43 08 01          	addl   $0x1,0x8(%ebx)
 8049443:	83 6b 04 01          	subl   $0x1,0x4(%ebx)
 8049447:	eb 80                	jmp    80493c9 <rio_readlineb+0x99>

08049449 <sigalrm_handler>:
 8049449:	83 ec 1c             	sub    $0x1c,%esp
 804944c:	c7 44 24 0c 00 00 00 	movl   $0x0,0xc(%esp)
 8049453:	00 
 8049454:	c7 44 24 08 08 a4 04 	movl   $0x804a408,0x8(%esp)
 804945b:	08 
 804945c:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049463:	00 
 8049464:	a1 a0 c3 04 08       	mov    0x804c3a0,%eax
 8049469:	89 04 24             	mov    %eax,(%esp)
 804946c:	e8 4f f4 ff ff       	call   80488c0 <__fprintf_chk@plt>
 8049471:	c7 04 24 01 00 00 00 	movl   $0x1,(%esp)
 8049478:	e8 c3 f3 ff ff       	call   8048840 <exit@plt>

0804947d <submitr>:
 804947d:	55                   	push   %ebp
 804947e:	57                   	push   %edi
 804947f:	56                   	push   %esi
 8049480:	53                   	push   %ebx
 8049481:	81 ec 7c a0 00 00    	sub    $0xa07c,%esp
 8049487:	8b 9c 24 90 a0 00 00 	mov    0xa090(%esp),%ebx
 804948e:	8b 84 24 98 a0 00 00 	mov    0xa098(%esp),%eax
 8049495:	89 44 24 30          	mov    %eax,0x30(%esp)
 8049499:	8b 94 24 9c a0 00 00 	mov    0xa09c(%esp),%edx
 80494a0:	89 54 24 34          	mov    %edx,0x34(%esp)
 80494a4:	8b 8c 24 a0 a0 00 00 	mov    0xa0a0(%esp),%ecx
 80494ab:	89 4c 24 38          	mov    %ecx,0x38(%esp)
 80494af:	8b ac 24 a4 a0 00 00 	mov    0xa0a4(%esp),%ebp
 80494b6:	8b 84 24 a8 a0 00 00 	mov    0xa0a8(%esp),%eax
 80494bd:	89 44 24 28          	mov    %eax,0x28(%esp)
 80494c1:	65 8b 15 14 00 00 00 	mov    %gs:0x14,%edx
 80494c8:	89 94 24 6c a0 00 00 	mov    %edx,0xa06c(%esp)
 80494cf:	31 d2                	xor    %edx,%edx
 80494d1:	c7 44 24 44 00 00 00 	movl   $0x0,0x44(%esp)
 80494d8:	00 
 80494d9:	c7 44 24 08 00 00 00 	movl   $0x0,0x8(%esp)
 80494e0:	00 
 80494e1:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 80494e8:	00 
 80494e9:	c7 04 24 02 00 00 00 	movl   $0x2,(%esp)
 80494f0:	e8 bb f3 ff ff       	call   80488b0 <socket@plt>
 80494f5:	89 44 24 2c          	mov    %eax,0x2c(%esp)
 80494f9:	85 c0                	test   %eax,%eax
 80494fb:	79 52                	jns    804954f <submitr+0xd2>
 80494fd:	8b 4c 24 28          	mov    0x28(%esp),%ecx
 8049501:	c7 01 45 72 72 6f    	movl   $0x6f727245,(%ecx)
 8049507:	c7 41 04 72 3a 20 43 	movl   $0x43203a72,0x4(%ecx)
 804950e:	c7 41 08 6c 69 65 6e 	movl   $0x6e65696c,0x8(%ecx)
 8049515:	c7 41 0c 74 20 75 6e 	movl   $0x6e752074,0xc(%ecx)
 804951c:	c7 41 10 61 62 6c 65 	movl   $0x656c6261,0x10(%ecx)
 8049523:	c7 41 14 20 74 6f 20 	movl   $0x206f7420,0x14(%ecx)
 804952a:	c7 41 18 63 72 65 61 	movl   $0x61657263,0x18(%ecx)
 8049531:	c7 41 1c 74 65 20 73 	movl   $0x73206574,0x1c(%ecx)
 8049538:	c7 41 20 6f 63 6b 65 	movl   $0x656b636f,0x20(%ecx)
 804953f:	66 c7 41 24 74 00    	movw   $0x74,0x24(%ecx)
 8049545:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 804954a:	e9 e8 06 00 00       	jmp    8049c37 <submitr+0x7ba>
 804954f:	89 1c 24             	mov    %ebx,(%esp)
 8049552:	e8 79 f3 ff ff       	call   80488d0 <gethostbyname@plt>
 8049557:	85 c0                	test   %eax,%eax
 8049559:	75 70                	jne    80495cb <submitr+0x14e>
 804955b:	8b 44 24 28          	mov    0x28(%esp),%eax
 804955f:	c7 00 45 72 72 6f    	movl   $0x6f727245,(%eax)
 8049565:	c7 40 04 72 3a 20 44 	movl   $0x44203a72,0x4(%eax)
 804956c:	c7 40 08 4e 53 20 69 	movl   $0x6920534e,0x8(%eax)
 8049573:	c7 40 0c 73 20 75 6e 	movl   $0x6e752073,0xc(%eax)
 804957a:	c7 40 10 61 62 6c 65 	movl   $0x656c6261,0x10(%eax)
 8049581:	c7 40 14 20 74 6f 20 	movl   $0x206f7420,0x14(%eax)
 8049588:	c7 40 18 72 65 73 6f 	movl   $0x6f736572,0x18(%eax)
 804958f:	c7 40 1c 6c 76 65 20 	movl   $0x2065766c,0x1c(%eax)
 8049596:	c7 40 20 73 65 72 76 	movl   $0x76726573,0x20(%eax)
 804959d:	c7 40 24 65 72 20 61 	movl   $0x61207265,0x24(%eax)
 80495a4:	c7 40 28 64 64 72 65 	movl   $0x65726464,0x28(%eax)
 80495ab:	66 c7 40 2c 73 73    	movw   $0x7373,0x2c(%eax)
 80495b1:	c6 40 2e 00          	movb   $0x0,0x2e(%eax)
 80495b5:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 80495b9:	89 04 24             	mov    %eax,(%esp)
 80495bc:	e8 3f f3 ff ff       	call   8048900 <close@plt>
 80495c1:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 80495c6:	e9 6c 06 00 00       	jmp    8049c37 <submitr+0x7ba>
 80495cb:	8d 9c 24 54 a0 00 00 	lea    0xa054(%esp),%ebx
 80495d2:	c7 84 24 54 a0 00 00 	movl   $0x0,0xa054(%esp)
 80495d9:	00 00 00 00 
 80495dd:	c7 84 24 58 a0 00 00 	movl   $0x0,0xa058(%esp)
 80495e4:	00 00 00 00 
 80495e8:	c7 84 24 5c a0 00 00 	movl   $0x0,0xa05c(%esp)
 80495ef:	00 00 00 00 
 80495f3:	c7 84 24 60 a0 00 00 	movl   $0x0,0xa060(%esp)
 80495fa:	00 00 00 00 
 80495fe:	66 c7 84 24 54 a0 00 	movw   $0x2,0xa054(%esp)
 8049605:	00 02 00 
 8049608:	c7 44 24 0c 0c 00 00 	movl   $0xc,0xc(%esp)
 804960f:	00 
 8049610:	8b 50 0c             	mov    0xc(%eax),%edx
 8049613:	89 54 24 08          	mov    %edx,0x8(%esp)
 8049617:	8b 40 10             	mov    0x10(%eax),%eax
 804961a:	8b 00                	mov    (%eax),%eax
 804961c:	89 44 24 04          	mov    %eax,0x4(%esp)
 8049620:	8d 84 24 58 a0 00 00 	lea    0xa058(%esp),%eax
 8049627:	89 04 24             	mov    %eax,(%esp)
 804962a:	e8 e1 f1 ff ff       	call   8048810 <__memmove_chk@plt>
 804962f:	0f b7 84 24 94 a0 00 	movzwl 0xa094(%esp),%eax
 8049636:	00 
 8049637:	66 c1 c8 08          	ror    $0x8,%ax
 804963b:	66 89 84 24 56 a0 00 	mov    %ax,0xa056(%esp)
 8049642:	00 
 8049643:	c7 44 24 08 10 00 00 	movl   $0x10,0x8(%esp)
 804964a:	00 
 804964b:	89 5c 24 04          	mov    %ebx,0x4(%esp)
 804964f:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049653:	89 04 24             	mov    %eax,(%esp)
 8049656:	e8 95 f2 ff ff       	call   80488f0 <connect@plt>
 804965b:	85 c0                	test   %eax,%eax
 804965d:	79 62                	jns    80496c1 <submitr+0x244>
 804965f:	8b 54 24 28          	mov    0x28(%esp),%edx
 8049663:	c7 02 45 72 72 6f    	movl   $0x6f727245,(%edx)
 8049669:	c7 42 04 72 3a 20 55 	movl   $0x55203a72,0x4(%edx)
 8049670:	c7 42 08 6e 61 62 6c 	movl   $0x6c62616e,0x8(%edx)
 8049677:	c7 42 0c 65 20 74 6f 	movl   $0x6f742065,0xc(%edx)
 804967e:	c7 42 10 20 63 6f 6e 	movl   $0x6e6f6320,0x10(%edx)
 8049685:	c7 42 14 6e 65 63 74 	movl   $0x7463656e,0x14(%edx)
 804968c:	c7 42 18 20 74 6f 20 	movl   $0x206f7420,0x18(%edx)
 8049693:	c7 42 1c 74 68 65 20 	movl   $0x20656874,0x1c(%edx)
 804969a:	c7 42 20 73 65 72 76 	movl   $0x76726573,0x20(%edx)
 80496a1:	66 c7 42 24 65 72    	movw   $0x7265,0x24(%edx)
 80496a7:	c6 42 26 00          	movb   $0x0,0x26(%edx)
 80496ab:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 80496af:	89 04 24             	mov    %eax,(%esp)
 80496b2:	e8 49 f2 ff ff       	call   8048900 <close@plt>
 80496b7:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 80496bc:	e9 76 05 00 00       	jmp    8049c37 <submitr+0x7ba>
 80496c1:	ba ff ff ff ff       	mov    $0xffffffff,%edx
 80496c6:	89 ef                	mov    %ebp,%edi
 80496c8:	b8 00 00 00 00       	mov    $0x0,%eax
 80496cd:	89 d1                	mov    %edx,%ecx
 80496cf:	f2 ae                	repnz scas %es:(%edi),%al
 80496d1:	89 cb                	mov    %ecx,%ebx
 80496d3:	f7 d3                	not    %ebx
 80496d5:	8b 7c 24 30          	mov    0x30(%esp),%edi
 80496d9:	89 d1                	mov    %edx,%ecx
 80496db:	f2 ae                	repnz scas %es:(%edi),%al
 80496dd:	89 4c 24 3c          	mov    %ecx,0x3c(%esp)
 80496e1:	8b 7c 24 34          	mov    0x34(%esp),%edi
 80496e5:	89 d1                	mov    %edx,%ecx
 80496e7:	f2 ae                	repnz scas %es:(%edi),%al
 80496e9:	89 ce                	mov    %ecx,%esi
 80496eb:	f7 d6                	not    %esi
 80496ed:	8b 7c 24 38          	mov    0x38(%esp),%edi
 80496f1:	89 d1                	mov    %edx,%ecx
 80496f3:	f2 ae                	repnz scas %es:(%edi),%al
 80496f5:	2b 74 24 3c          	sub    0x3c(%esp),%esi
 80496f9:	29 ce                	sub    %ecx,%esi
 80496fb:	8d 44 5b fd          	lea    -0x3(%ebx,%ebx,2),%eax
 80496ff:	8d 44 06 7b          	lea    0x7b(%esi,%eax,1),%eax
 8049703:	3d 00 20 00 00       	cmp    $0x2000,%eax
 8049708:	76 7b                	jbe    8049785 <submitr+0x308>
 804970a:	8b 44 24 28          	mov    0x28(%esp),%eax
 804970e:	c7 00 45 72 72 6f    	movl   $0x6f727245,(%eax)
 8049714:	c7 40 04 72 3a 20 52 	movl   $0x52203a72,0x4(%eax)
 804971b:	c7 40 08 65 73 75 6c 	movl   $0x6c757365,0x8(%eax)
 8049722:	c7 40 0c 74 20 73 74 	movl   $0x74732074,0xc(%eax)
 8049729:	c7 40 10 72 69 6e 67 	movl   $0x676e6972,0x10(%eax)
 8049730:	c7 40 14 20 74 6f 6f 	movl   $0x6f6f7420,0x14(%eax)
 8049737:	c7 40 18 20 6c 61 72 	movl   $0x72616c20,0x18(%eax)
 804973e:	c7 40 1c 67 65 2e 20 	movl   $0x202e6567,0x1c(%eax)
 8049745:	c7 40 20 49 6e 63 72 	movl   $0x72636e49,0x20(%eax)
 804974c:	c7 40 24 65 61 73 65 	movl   $0x65736165,0x24(%eax)
 8049753:	c7 40 28 20 53 55 42 	movl   $0x42555320,0x28(%eax)
 804975a:	c7 40 2c 4d 49 54 52 	movl   $0x5254494d,0x2c(%eax)
 8049761:	c7 40 30 5f 4d 41 58 	movl   $0x58414d5f,0x30(%eax)
 8049768:	c7 40 34 42 55 46 00 	movl   $0x465542,0x34(%eax)
 804976f:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049773:	89 04 24             	mov    %eax,(%esp)
 8049776:	e8 85 f1 ff ff       	call   8048900 <close@plt>
 804977b:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049780:	e9 b2 04 00 00       	jmp    8049c37 <submitr+0x7ba>
 8049785:	8d 94 24 54 40 00 00 	lea    0x4054(%esp),%edx
 804978c:	b9 00 08 00 00       	mov    $0x800,%ecx
 8049791:	b8 00 00 00 00       	mov    $0x0,%eax
 8049796:	89 d7                	mov    %edx,%edi
 8049798:	f3 ab                	rep stos %eax,%es:(%edi)
 804979a:	89 ef                	mov    %ebp,%edi
 804979c:	b9 ff ff ff ff       	mov    $0xffffffff,%ecx
 80497a1:	f2 ae                	repnz scas %es:(%edi),%al
 80497a3:	f7 d1                	not    %ecx
 80497a5:	89 ce                	mov    %ecx,%esi
 80497a7:	83 ee 01             	sub    $0x1,%esi
 80497aa:	0f 84 99 04 00 00    	je     8049c49 <submitr+0x7cc>
 80497b0:	89 d3                	mov    %edx,%ebx
 80497b2:	0f b6 45 00          	movzbl 0x0(%ebp),%eax
 80497b6:	3c 2a                	cmp    $0x2a,%al
 80497b8:	74 24                	je     80497de <submitr+0x361>
 80497ba:	3c 2d                	cmp    $0x2d,%al
 80497bc:	74 20                	je     80497de <submitr+0x361>
 80497be:	3c 2e                	cmp    $0x2e,%al
 80497c0:	74 1c                	je     80497de <submitr+0x361>
 80497c2:	3c 5f                	cmp    $0x5f,%al
 80497c4:	74 18                	je     80497de <submitr+0x361>
 80497c6:	8d 50 d0             	lea    -0x30(%eax),%edx
 80497c9:	80 fa 09             	cmp    $0x9,%dl
 80497cc:	76 10                	jbe    80497de <submitr+0x361>
 80497ce:	8d 50 bf             	lea    -0x41(%eax),%edx
 80497d1:	80 fa 19             	cmp    $0x19,%dl
 80497d4:	76 08                	jbe    80497de <submitr+0x361>
 80497d6:	8d 50 9f             	lea    -0x61(%eax),%edx
 80497d9:	80 fa 19             	cmp    $0x19,%dl
 80497dc:	77 07                	ja     80497e5 <submitr+0x368>
 80497de:	88 03                	mov    %al,(%ebx)
 80497e0:	83 c3 01             	add    $0x1,%ebx
 80497e3:	eb 69                	jmp    804984e <submitr+0x3d1>
 80497e5:	3c 20                	cmp    $0x20,%al
 80497e7:	75 08                	jne    80497f1 <submitr+0x374>
 80497e9:	c6 03 2b             	movb   $0x2b,(%ebx)
 80497ec:	83 c3 01             	add    $0x1,%ebx
 80497ef:	eb 5d                	jmp    804984e <submitr+0x3d1>
 80497f1:	8d 50 e0             	lea    -0x20(%eax),%edx
 80497f4:	80 fa 5f             	cmp    $0x5f,%dl
 80497f7:	76 04                	jbe    80497fd <submitr+0x380>
 80497f9:	3c 09                	cmp    $0x9,%al
 80497fb:	75 62                	jne    804985f <submitr+0x3e2>
 80497fd:	0f b6 c0             	movzbl %al,%eax
 8049800:	89 44 24 10          	mov    %eax,0x10(%esp)
 8049804:	c7 44 24 0c 14 a5 04 	movl   $0x804a514,0xc(%esp)
 804980b:	08 
 804980c:	c7 44 24 08 08 00 00 	movl   $0x8,0x8(%esp)
 8049813:	00 
 8049814:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 804981b:	00 
 804981c:	8d 94 24 64 a0 00 00 	lea    0xa064(%esp),%edx
 8049823:	89 14 24             	mov    %edx,(%esp)
 8049826:	e8 f5 f0 ff ff       	call   8048920 <__sprintf_chk@plt>
 804982b:	0f b6 84 24 64 a0 00 	movzbl 0xa064(%esp),%eax
 8049832:	00 
 8049833:	88 03                	mov    %al,(%ebx)
 8049835:	0f b6 84 24 65 a0 00 	movzbl 0xa065(%esp),%eax
 804983c:	00 
 804983d:	88 43 01             	mov    %al,0x1(%ebx)
 8049840:	0f b6 84 24 66 a0 00 	movzbl 0xa066(%esp),%eax
 8049847:	00 
 8049848:	88 43 02             	mov    %al,0x2(%ebx)
 804984b:	83 c3 03             	add    $0x3,%ebx
 804984e:	83 c5 01             	add    $0x1,%ebp
 8049851:	83 ee 01             	sub    $0x1,%esi
 8049854:	0f 85 58 ff ff ff    	jne    80497b2 <submitr+0x335>
 804985a:	e9 ea 03 00 00       	jmp    8049c49 <submitr+0x7cc>
 804985f:	8b 7c 24 28          	mov    0x28(%esp),%edi
 8049863:	be 2c a4 04 08       	mov    $0x804a42c,%esi
 8049868:	b8 43 00 00 00       	mov    $0x43,%eax
 804986d:	f7 c7 01 00 00 00    	test   $0x1,%edi
 8049873:	74 1a                	je     804988f <submitr+0x412>
 8049875:	0f b6 05 2c a4 04 08 	movzbl 0x804a42c,%eax
 804987c:	88 07                	mov    %al,(%edi)
 804987e:	8b 7c 24 28          	mov    0x28(%esp),%edi
 8049882:	83 c7 01             	add    $0x1,%edi
 8049885:	be 2d a4 04 08       	mov    $0x804a42d,%esi
 804988a:	b8 42 00 00 00       	mov    $0x42,%eax
 804988f:	f7 c7 02 00 00 00    	test   $0x2,%edi
 8049895:	74 0f                	je     80498a6 <submitr+0x429>
 8049897:	0f b7 16             	movzwl (%esi),%edx
 804989a:	66 89 17             	mov    %dx,(%edi)
 804989d:	83 c7 02             	add    $0x2,%edi
 80498a0:	83 c6 02             	add    $0x2,%esi
 80498a3:	83 e8 02             	sub    $0x2,%eax
 80498a6:	89 c1                	mov    %eax,%ecx
 80498a8:	c1 e9 02             	shr    $0x2,%ecx
 80498ab:	f3 a5                	rep movsl %ds:(%esi),%es:(%edi)
 80498ad:	ba 00 00 00 00       	mov    $0x0,%edx
 80498b2:	a8 02                	test   $0x2,%al
 80498b4:	74 0b                	je     80498c1 <submitr+0x444>
 80498b6:	0f b7 16             	movzwl (%esi),%edx
 80498b9:	66 89 17             	mov    %dx,(%edi)
 80498bc:	ba 02 00 00 00       	mov    $0x2,%edx
 80498c1:	a8 01                	test   $0x1,%al
 80498c3:	74 07                	je     80498cc <submitr+0x44f>
 80498c5:	0f b6 04 16          	movzbl (%esi,%edx,1),%eax
 80498c9:	88 04 17             	mov    %al,(%edi,%edx,1)
 80498cc:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 80498d0:	89 04 24             	mov    %eax,(%esp)
 80498d3:	e8 28 f0 ff ff       	call   8048900 <close@plt>
 80498d8:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 80498dd:	e9 55 03 00 00       	jmp    8049c37 <submitr+0x7ba>
 80498e2:	89 fd                	mov    %edi,%ebp
 80498e4:	8b 7c 24 2c          	mov    0x2c(%esp),%edi
 80498e8:	89 5c 24 08          	mov    %ebx,0x8(%esp)
 80498ec:	89 74 24 04          	mov    %esi,0x4(%esp)
 80498f0:	89 3c 24             	mov    %edi,(%esp)
 80498f3:	e8 68 ef ff ff       	call   8048860 <write@plt>
 80498f8:	85 c0                	test   %eax,%eax
 80498fa:	7f 0f                	jg     804990b <submitr+0x48e>
 80498fc:	e8 8f ef ff ff       	call   8048890 <__errno_location@plt>
 8049901:	83 38 04             	cmpl   $0x4,(%eax)
 8049904:	75 0f                	jne    8049915 <submitr+0x498>
 8049906:	b8 00 00 00 00       	mov    $0x0,%eax
 804990b:	01 c6                	add    %eax,%esi
 804990d:	29 c3                	sub    %eax,%ebx
 804990f:	75 d7                	jne    80498e8 <submitr+0x46b>
 8049911:	85 ed                	test   %ebp,%ebp
 8049913:	79 66                	jns    804997b <submitr+0x4fe>
 8049915:	8b 54 24 28          	mov    0x28(%esp),%edx
 8049919:	c7 02 45 72 72 6f    	movl   $0x6f727245,(%edx)
 804991f:	c7 42 04 72 3a 20 43 	movl   $0x43203a72,0x4(%edx)
 8049926:	c7 42 08 6c 69 65 6e 	movl   $0x6e65696c,0x8(%edx)
 804992d:	c7 42 0c 74 20 75 6e 	movl   $0x6e752074,0xc(%edx)
 8049934:	c7 42 10 61 62 6c 65 	movl   $0x656c6261,0x10(%edx)
 804993b:	c7 42 14 20 74 6f 20 	movl   $0x206f7420,0x14(%edx)
 8049942:	c7 42 18 77 72 69 74 	movl   $0x74697277,0x18(%edx)
 8049949:	c7 42 1c 65 20 74 6f 	movl   $0x6f742065,0x1c(%edx)
 8049950:	c7 42 20 20 74 68 65 	movl   $0x65687420,0x20(%edx)
 8049957:	c7 42 24 20 73 65 72 	movl   $0x72657320,0x24(%edx)
 804995e:	c7 42 28 76 65 72 00 	movl   $0x726576,0x28(%edx)
 8049965:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049969:	89 04 24             	mov    %eax,(%esp)
 804996c:	e8 8f ef ff ff       	call   8048900 <close@plt>
 8049971:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049976:	e9 bc 02 00 00       	jmp    8049c37 <submitr+0x7ba>
 804997b:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 804997f:	89 44 24 48          	mov    %eax,0x48(%esp)
 8049983:	c7 44 24 4c 00 00 00 	movl   $0x0,0x4c(%esp)
 804998a:	00 
 804998b:	8d 44 24 54          	lea    0x54(%esp),%eax
 804998f:	89 44 24 50          	mov    %eax,0x50(%esp)
 8049993:	b9 00 20 00 00       	mov    $0x2000,%ecx
 8049998:	8d 94 24 54 20 00 00 	lea    0x2054(%esp),%edx
 804999f:	8d 44 24 48          	lea    0x48(%esp),%eax
 80499a3:	e8 88 f9 ff ff       	call   8049330 <rio_readlineb>
 80499a8:	85 c0                	test   %eax,%eax
 80499aa:	7f 7a                	jg     8049a26 <submitr+0x5a9>
 80499ac:	8b 54 24 28          	mov    0x28(%esp),%edx
 80499b0:	c7 02 45 72 72 6f    	movl   $0x6f727245,(%edx)
 80499b6:	c7 42 04 72 3a 20 43 	movl   $0x43203a72,0x4(%edx)
 80499bd:	c7 42 08 6c 69 65 6e 	movl   $0x6e65696c,0x8(%edx)
 80499c4:	c7 42 0c 74 20 75 6e 	movl   $0x6e752074,0xc(%edx)
 80499cb:	c7 42 10 61 62 6c 65 	movl   $0x656c6261,0x10(%edx)
 80499d2:	c7 42 14 20 74 6f 20 	movl   $0x206f7420,0x14(%edx)
 80499d9:	c7 42 18 72 65 61 64 	movl   $0x64616572,0x18(%edx)
 80499e0:	c7 42 1c 20 66 69 72 	movl   $0x72696620,0x1c(%edx)
 80499e7:	c7 42 20 73 74 20 68 	movl   $0x68207473,0x20(%edx)
 80499ee:	c7 42 24 65 61 64 65 	movl   $0x65646165,0x24(%edx)
 80499f5:	c7 42 28 72 20 66 72 	movl   $0x72662072,0x28(%edx)
 80499fc:	c7 42 2c 6f 6d 20 73 	movl   $0x73206d6f,0x2c(%edx)
 8049a03:	c7 42 30 65 72 76 65 	movl   $0x65767265,0x30(%edx)
 8049a0a:	66 c7 42 34 72 00    	movw   $0x72,0x34(%edx)
 8049a10:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049a14:	89 04 24             	mov    %eax,(%esp)
 8049a17:	e8 e4 ee ff ff       	call   8048900 <close@plt>
 8049a1c:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049a21:	e9 11 02 00 00       	jmp    8049c37 <submitr+0x7ba>
 8049a26:	8d 84 24 54 80 00 00 	lea    0x8054(%esp),%eax
 8049a2d:	89 44 24 10          	mov    %eax,0x10(%esp)
 8049a31:	8d 44 24 44          	lea    0x44(%esp),%eax
 8049a35:	89 44 24 0c          	mov    %eax,0xc(%esp)
 8049a39:	8d 84 24 54 60 00 00 	lea    0x6054(%esp),%eax
 8049a40:	89 44 24 08          	mov    %eax,0x8(%esp)
 8049a44:	c7 44 24 04 1b a5 04 	movl   $0x804a51b,0x4(%esp)
 8049a4b:	08 
 8049a4c:	8d 84 24 54 20 00 00 	lea    0x2054(%esp),%eax
 8049a53:	89 04 24             	mov    %eax,(%esp)
 8049a56:	e8 15 ee ff ff       	call   8048870 <__isoc99_sscanf@plt>
 8049a5b:	8b 44 24 44          	mov    0x44(%esp),%eax
 8049a5f:	3d c8 00 00 00       	cmp    $0xc8,%eax
 8049a64:	0f 84 d3 00 00 00    	je     8049b3d <submitr+0x6c0>
 8049a6a:	8d 94 24 54 80 00 00 	lea    0x8054(%esp),%edx
 8049a71:	89 54 24 14          	mov    %edx,0x14(%esp)
 8049a75:	89 44 24 10          	mov    %eax,0x10(%esp)
 8049a79:	c7 44 24 0c 70 a4 04 	movl   $0x804a470,0xc(%esp)
 8049a80:	08 
 8049a81:	c7 44 24 08 ff ff ff 	movl   $0xffffffff,0x8(%esp)
 8049a88:	ff 
 8049a89:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049a90:	00 
 8049a91:	8b 54 24 28          	mov    0x28(%esp),%edx
 8049a95:	89 14 24             	mov    %edx,(%esp)
 8049a98:	e8 83 ee ff ff       	call   8048920 <__sprintf_chk@plt>
 8049a9d:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049aa1:	89 04 24             	mov    %eax,(%esp)
 8049aa4:	e8 57 ee ff ff       	call   8048900 <close@plt>
 8049aa9:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049aae:	e9 84 01 00 00       	jmp    8049c37 <submitr+0x7ba>
 8049ab3:	b9 00 20 00 00       	mov    $0x2000,%ecx
 8049ab8:	8d 94 24 54 20 00 00 	lea    0x2054(%esp),%edx
 8049abf:	8d 44 24 48          	lea    0x48(%esp),%eax
 8049ac3:	e8 68 f8 ff ff       	call   8049330 <rio_readlineb>
 8049ac8:	85 c0                	test   %eax,%eax
 8049aca:	7f 71                	jg     8049b3d <submitr+0x6c0>
 8049acc:	8b 54 24 28          	mov    0x28(%esp),%edx
 8049ad0:	c7 02 45 72 72 6f    	movl   $0x6f727245,(%edx)
 8049ad6:	c7 42 04 72 3a 20 43 	movl   $0x43203a72,0x4(%edx)
 8049add:	c7 42 08 6c 69 65 6e 	movl   $0x6e65696c,0x8(%edx)
 8049ae4:	c7 42 0c 74 20 75 6e 	movl   $0x6e752074,0xc(%edx)
 8049aeb:	c7 42 10 61 62 6c 65 	movl   $0x656c6261,0x10(%edx)
 8049af2:	c7 42 14 20 74 6f 20 	movl   $0x206f7420,0x14(%edx)
 8049af9:	c7 42 18 72 65 61 64 	movl   $0x64616572,0x18(%edx)
 8049b00:	c7 42 1c 20 68 65 61 	movl   $0x61656820,0x1c(%edx)
 8049b07:	c7 42 20 64 65 72 73 	movl   $0x73726564,0x20(%edx)
 8049b0e:	c7 42 24 20 66 72 6f 	movl   $0x6f726620,0x24(%edx)
 8049b15:	c7 42 28 6d 20 73 65 	movl   $0x6573206d,0x28(%edx)
 8049b1c:	c7 42 2c 72 76 65 72 	movl   $0x72657672,0x2c(%edx)
 8049b23:	c6 42 30 00          	movb   $0x0,0x30(%edx)
 8049b27:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049b2b:	89 04 24             	mov    %eax,(%esp)
 8049b2e:	e8 cd ed ff ff       	call   8048900 <close@plt>
 8049b33:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049b38:	e9 fa 00 00 00       	jmp    8049c37 <submitr+0x7ba>
 8049b3d:	80 bc 24 54 20 00 00 	cmpb   $0xd,0x2054(%esp)
 8049b44:	0d 
 8049b45:	0f 85 68 ff ff ff    	jne    8049ab3 <submitr+0x636>
 8049b4b:	80 bc 24 55 20 00 00 	cmpb   $0xa,0x2055(%esp)
 8049b52:	0a 
 8049b53:	0f 85 5a ff ff ff    	jne    8049ab3 <submitr+0x636>
 8049b59:	80 bc 24 56 20 00 00 	cmpb   $0x0,0x2056(%esp)
 8049b60:	00 
 8049b61:	0f 85 4c ff ff ff    	jne    8049ab3 <submitr+0x636>
 8049b67:	b9 00 20 00 00       	mov    $0x2000,%ecx
 8049b6c:	8d 94 24 54 20 00 00 	lea    0x2054(%esp),%edx
 8049b73:	8d 44 24 48          	lea    0x48(%esp),%eax
 8049b77:	e8 b4 f7 ff ff       	call   8049330 <rio_readlineb>
 8049b7c:	85 c0                	test   %eax,%eax
 8049b7e:	7f 78                	jg     8049bf8 <submitr+0x77b>
 8049b80:	8b 54 24 28          	mov    0x28(%esp),%edx
 8049b84:	c7 02 45 72 72 6f    	movl   $0x6f727245,(%edx)
 8049b8a:	c7 42 04 72 3a 20 43 	movl   $0x43203a72,0x4(%edx)
 8049b91:	c7 42 08 6c 69 65 6e 	movl   $0x6e65696c,0x8(%edx)
 8049b98:	c7 42 0c 74 20 75 6e 	movl   $0x6e752074,0xc(%edx)
 8049b9f:	c7 42 10 61 62 6c 65 	movl   $0x656c6261,0x10(%edx)
 8049ba6:	c7 42 14 20 74 6f 20 	movl   $0x206f7420,0x14(%edx)
 8049bad:	c7 42 18 72 65 61 64 	movl   $0x64616572,0x18(%edx)
 8049bb4:	c7 42 1c 20 73 74 61 	movl   $0x61747320,0x1c(%edx)
 8049bbb:	c7 42 20 74 75 73 20 	movl   $0x20737574,0x20(%edx)
 8049bc2:	c7 42 24 6d 65 73 73 	movl   $0x7373656d,0x24(%edx)
 8049bc9:	c7 42 28 61 67 65 20 	movl   $0x20656761,0x28(%edx)
 8049bd0:	c7 42 2c 66 72 6f 6d 	movl   $0x6d6f7266,0x2c(%edx)
 8049bd7:	c7 42 30 20 73 65 72 	movl   $0x72657320,0x30(%edx)
 8049bde:	c7 42 34 76 65 72 00 	movl   $0x726576,0x34(%edx)
 8049be5:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049be9:	89 04 24             	mov    %eax,(%esp)
 8049bec:	e8 0f ed ff ff       	call   8048900 <close@plt>
 8049bf1:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049bf6:	eb 3f                	jmp    8049c37 <submitr+0x7ba>
 8049bf8:	8d 84 24 54 20 00 00 	lea    0x2054(%esp),%eax
 8049bff:	89 44 24 04          	mov    %eax,0x4(%esp)
 8049c03:	8b 54 24 28          	mov    0x28(%esp),%edx
 8049c07:	89 14 24             	mov    %edx,(%esp)
 8049c0a:	e8 d1 eb ff ff       	call   80487e0 <strcpy@plt>
 8049c0f:	8b 44 24 2c          	mov    0x2c(%esp),%eax
 8049c13:	89 04 24             	mov    %eax,(%esp)
 8049c16:	e8 e5 ec ff ff       	call   8048900 <close@plt>
 8049c1b:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049c20:	8b 54 24 28          	mov    0x28(%esp),%edx
 8049c24:	80 3a 4f             	cmpb   $0x4f,(%edx)
 8049c27:	75 0e                	jne    8049c37 <submitr+0x7ba>
 8049c29:	80 7a 01 4b          	cmpb   $0x4b,0x1(%edx)
 8049c2d:	75 08                	jne    8049c37 <submitr+0x7ba>
 8049c2f:	80 7a 02 01          	cmpb   $0x1,0x2(%edx)
 8049c33:	19 c0                	sbb    %eax,%eax
 8049c35:	f7 d0                	not    %eax
 8049c37:	8b 8c 24 6c a0 00 00 	mov    0xa06c(%esp),%ecx
 8049c3e:	65 33 0d 14 00 00 00 	xor    %gs:0x14,%ecx
 8049c45:	74 78                	je     8049cbf <submitr+0x842>
 8049c47:	eb 71                	jmp    8049cba <submitr+0x83d>
 8049c49:	8d 84 24 54 40 00 00 	lea    0x4054(%esp),%eax
 8049c50:	89 44 24 1c          	mov    %eax,0x1c(%esp)
 8049c54:	8b 44 24 38          	mov    0x38(%esp),%eax
 8049c58:	89 44 24 18          	mov    %eax,0x18(%esp)
 8049c5c:	8b 54 24 34          	mov    0x34(%esp),%edx
 8049c60:	89 54 24 14          	mov    %edx,0x14(%esp)
 8049c64:	8b 4c 24 30          	mov    0x30(%esp),%ecx
 8049c68:	89 4c 24 10          	mov    %ecx,0x10(%esp)
 8049c6c:	c7 44 24 0c a0 a4 04 	movl   $0x804a4a0,0xc(%esp)
 8049c73:	08 
 8049c74:	c7 44 24 08 00 20 00 	movl   $0x2000,0x8(%esp)
 8049c7b:	00 
 8049c7c:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049c83:	00 
 8049c84:	8d bc 24 54 20 00 00 	lea    0x2054(%esp),%edi
 8049c8b:	89 3c 24             	mov    %edi,(%esp)
 8049c8e:	e8 8d ec ff ff       	call   8048920 <__sprintf_chk@plt>
 8049c93:	b8 00 00 00 00       	mov    $0x0,%eax
 8049c98:	b9 ff ff ff ff       	mov    $0xffffffff,%ecx
 8049c9d:	f2 ae                	repnz scas %es:(%edi),%al
 8049c9f:	f7 d1                	not    %ecx
 8049ca1:	8d 79 ff             	lea    -0x1(%ecx),%edi
 8049ca4:	89 fb                	mov    %edi,%ebx
 8049ca6:	8d b4 24 54 20 00 00 	lea    0x2054(%esp),%esi
 8049cad:	85 ff                	test   %edi,%edi
 8049caf:	0f 85 2d fc ff ff    	jne    80498e2 <submitr+0x465>
 8049cb5:	e9 c1 fc ff ff       	jmp    804997b <submitr+0x4fe>
 8049cba:	e8 11 eb ff ff       	call   80487d0 <__stack_chk_fail@plt>
 8049cbf:	81 c4 7c a0 00 00    	add    $0xa07c,%esp
 8049cc5:	5b                   	pop    %ebx
 8049cc6:	5e                   	pop    %esi
 8049cc7:	5f                   	pop    %edi
 8049cc8:	5d                   	pop    %ebp
 8049cc9:	c3                   	ret    

08049cca <init_timeout>:
 8049cca:	53                   	push   %ebx
 8049ccb:	83 ec 18             	sub    $0x18,%esp
 8049cce:	8b 5c 24 20          	mov    0x20(%esp),%ebx
 8049cd2:	85 db                	test   %ebx,%ebx
 8049cd4:	74 26                	je     8049cfc <init_timeout+0x32>
 8049cd6:	c7 44 24 04 49 94 04 	movl   $0x8049449,0x4(%esp)
 8049cdd:	08 
 8049cde:	c7 04 24 0e 00 00 00 	movl   $0xe,(%esp)
 8049ce5:	e8 b6 ea ff ff       	call   80487a0 <signal@plt>
 8049cea:	85 db                	test   %ebx,%ebx
 8049cec:	b8 00 00 00 00       	mov    $0x0,%eax
 8049cf1:	0f 48 d8             	cmovs  %eax,%ebx
 8049cf4:	89 1c 24             	mov    %ebx,(%esp)
 8049cf7:	e8 c4 ea ff ff       	call   80487c0 <alarm@plt>
 8049cfc:	83 c4 18             	add    $0x18,%esp
 8049cff:	5b                   	pop    %ebx
 8049d00:	c3                   	ret    

08049d01 <init_driver>:
 8049d01:	57                   	push   %edi
 8049d02:	56                   	push   %esi
 8049d03:	53                   	push   %ebx
 8049d04:	83 ec 40             	sub    $0x40,%esp
 8049d07:	8b 74 24 50          	mov    0x50(%esp),%esi
 8049d0b:	65 a1 14 00 00 00    	mov    %gs:0x14,%eax
 8049d11:	89 44 24 3c          	mov    %eax,0x3c(%esp)
 8049d15:	31 c0                	xor    %eax,%eax
 8049d17:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049d1e:	00 
 8049d1f:	c7 04 24 0d 00 00 00 	movl   $0xd,(%esp)
 8049d26:	e8 75 ea ff ff       	call   80487a0 <signal@plt>
 8049d2b:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049d32:	00 
 8049d33:	c7 04 24 1d 00 00 00 	movl   $0x1d,(%esp)
 8049d3a:	e8 61 ea ff ff       	call   80487a0 <signal@plt>
 8049d3f:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049d46:	00 
 8049d47:	c7 04 24 1d 00 00 00 	movl   $0x1d,(%esp)
 8049d4e:	e8 4d ea ff ff       	call   80487a0 <signal@plt>
 8049d53:	c7 44 24 08 00 00 00 	movl   $0x0,0x8(%esp)
 8049d5a:	00 
 8049d5b:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049d62:	00 
 8049d63:	c7 04 24 02 00 00 00 	movl   $0x2,(%esp)
 8049d6a:	e8 41 eb ff ff       	call   80488b0 <socket@plt>
 8049d6f:	89 c3                	mov    %eax,%ebx
 8049d71:	85 c0                	test   %eax,%eax
 8049d73:	79 4e                	jns    8049dc3 <init_driver+0xc2>
 8049d75:	c7 06 45 72 72 6f    	movl   $0x6f727245,(%esi)
 8049d7b:	c7 46 04 72 3a 20 43 	movl   $0x43203a72,0x4(%esi)
 8049d82:	c7 46 08 6c 69 65 6e 	movl   $0x6e65696c,0x8(%esi)
 8049d89:	c7 46 0c 74 20 75 6e 	movl   $0x6e752074,0xc(%esi)
 8049d90:	c7 46 10 61 62 6c 65 	movl   $0x656c6261,0x10(%esi)
 8049d97:	c7 46 14 20 74 6f 20 	movl   $0x206f7420,0x14(%esi)
 8049d9e:	c7 46 18 63 72 65 61 	movl   $0x61657263,0x18(%esi)
 8049da5:	c7 46 1c 74 65 20 73 	movl   $0x73206574,0x1c(%esi)
 8049dac:	c7 46 20 6f 63 6b 65 	movl   $0x656b636f,0x20(%esi)
 8049db3:	66 c7 46 24 74 00    	movw   $0x74,0x24(%esi)
 8049db9:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049dbe:	e9 33 01 00 00       	jmp    8049ef6 <init_driver+0x1f5>
 8049dc3:	c7 04 24 2c a5 04 08 	movl   $0x804a52c,(%esp)
 8049dca:	e8 01 eb ff ff       	call   80488d0 <gethostbyname@plt>
 8049dcf:	85 c0                	test   %eax,%eax
 8049dd1:	75 68                	jne    8049e3b <init_driver+0x13a>
 8049dd3:	c7 06 45 72 72 6f    	movl   $0x6f727245,(%esi)
 8049dd9:	c7 46 04 72 3a 20 44 	movl   $0x44203a72,0x4(%esi)
 8049de0:	c7 46 08 4e 53 20 69 	movl   $0x6920534e,0x8(%esi)
 8049de7:	c7 46 0c 73 20 75 6e 	movl   $0x6e752073,0xc(%esi)
 8049dee:	c7 46 10 61 62 6c 65 	movl   $0x656c6261,0x10(%esi)
 8049df5:	c7 46 14 20 74 6f 20 	movl   $0x206f7420,0x14(%esi)
 8049dfc:	c7 46 18 72 65 73 6f 	movl   $0x6f736572,0x18(%esi)
 8049e03:	c7 46 1c 6c 76 65 20 	movl   $0x2065766c,0x1c(%esi)
 8049e0a:	c7 46 20 73 65 72 76 	movl   $0x76726573,0x20(%esi)
 8049e11:	c7 46 24 65 72 20 61 	movl   $0x61207265,0x24(%esi)
 8049e18:	c7 46 28 64 64 72 65 	movl   $0x65726464,0x28(%esi)
 8049e1f:	66 c7 46 2c 73 73    	movw   $0x7373,0x2c(%esi)
 8049e25:	c6 46 2e 00          	movb   $0x0,0x2e(%esi)
 8049e29:	89 1c 24             	mov    %ebx,(%esp)
 8049e2c:	e8 cf ea ff ff       	call   8048900 <close@plt>
 8049e31:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049e36:	e9 bb 00 00 00       	jmp    8049ef6 <init_driver+0x1f5>
 8049e3b:	8d 7c 24 2c          	lea    0x2c(%esp),%edi
 8049e3f:	c7 44 24 2c 00 00 00 	movl   $0x0,0x2c(%esp)
 8049e46:	00 
 8049e47:	c7 44 24 30 00 00 00 	movl   $0x0,0x30(%esp)
 8049e4e:	00 
 8049e4f:	c7 44 24 34 00 00 00 	movl   $0x0,0x34(%esp)
 8049e56:	00 
 8049e57:	c7 44 24 38 00 00 00 	movl   $0x0,0x38(%esp)
 8049e5e:	00 
 8049e5f:	66 c7 44 24 2c 02 00 	movw   $0x2,0x2c(%esp)
 8049e66:	c7 44 24 0c 0c 00 00 	movl   $0xc,0xc(%esp)
 8049e6d:	00 
 8049e6e:	8b 50 0c             	mov    0xc(%eax),%edx
 8049e71:	89 54 24 08          	mov    %edx,0x8(%esp)
 8049e75:	8b 40 10             	mov    0x10(%eax),%eax
 8049e78:	8b 00                	mov    (%eax),%eax
 8049e7a:	89 44 24 04          	mov    %eax,0x4(%esp)
 8049e7e:	8d 44 24 30          	lea    0x30(%esp),%eax
 8049e82:	89 04 24             	mov    %eax,(%esp)
 8049e85:	e8 86 e9 ff ff       	call   8048810 <__memmove_chk@plt>
 8049e8a:	66 c7 44 24 2e 3b 6e 	movw   $0x6e3b,0x2e(%esp)
 8049e91:	c7 44 24 08 10 00 00 	movl   $0x10,0x8(%esp)
 8049e98:	00 
 8049e99:	89 7c 24 04          	mov    %edi,0x4(%esp)
 8049e9d:	89 1c 24             	mov    %ebx,(%esp)
 8049ea0:	e8 4b ea ff ff       	call   80488f0 <connect@plt>
 8049ea5:	85 c0                	test   %eax,%eax
 8049ea7:	79 37                	jns    8049ee0 <init_driver+0x1df>
 8049ea9:	c7 44 24 10 2c a5 04 	movl   $0x804a52c,0x10(%esp)
 8049eb0:	08 
 8049eb1:	c7 44 24 0c ec a4 04 	movl   $0x804a4ec,0xc(%esp)
 8049eb8:	08 
 8049eb9:	c7 44 24 08 ff ff ff 	movl   $0xffffffff,0x8(%esp)
 8049ec0:	ff 
 8049ec1:	c7 44 24 04 01 00 00 	movl   $0x1,0x4(%esp)
 8049ec8:	00 
 8049ec9:	89 34 24             	mov    %esi,(%esp)
 8049ecc:	e8 4f ea ff ff       	call   8048920 <__sprintf_chk@plt>
 8049ed1:	89 1c 24             	mov    %ebx,(%esp)
 8049ed4:	e8 27 ea ff ff       	call   8048900 <close@plt>
 8049ed9:	b8 ff ff ff ff       	mov    $0xffffffff,%eax
 8049ede:	eb 16                	jmp    8049ef6 <init_driver+0x1f5>
 8049ee0:	89 1c 24             	mov    %ebx,(%esp)
 8049ee3:	e8 18 ea ff ff       	call   8048900 <close@plt>
 8049ee8:	66 c7 06 4f 4b       	movw   $0x4b4f,(%esi)
 8049eed:	c6 46 02 00          	movb   $0x0,0x2(%esi)
 8049ef1:	b8 00 00 00 00       	mov    $0x0,%eax
 8049ef6:	8b 54 24 3c          	mov    0x3c(%esp),%edx
 8049efa:	65 33 15 14 00 00 00 	xor    %gs:0x14,%edx
 8049f01:	74 05                	je     8049f08 <init_driver+0x207>
 8049f03:	e8 c8 e8 ff ff       	call   80487d0 <__stack_chk_fail@plt>
 8049f08:	83 c4 40             	add    $0x40,%esp
 8049f0b:	5b                   	pop    %ebx
 8049f0c:	5e                   	pop    %esi
 8049f0d:	5f                   	pop    %edi
 8049f0e:	c3                   	ret    

08049f0f <driver_post>:
 8049f0f:	53                   	push   %ebx
 8049f10:	83 ec 28             	sub    $0x28,%esp
 8049f13:	8b 44 24 30          	mov    0x30(%esp),%eax
 8049f17:	8b 54 24 34          	mov    0x34(%esp),%edx
 8049f1b:	8b 5c 24 3c          	mov    0x3c(%esp),%ebx
 8049f1f:	83 7c 24 38 00       	cmpl   $0x0,0x38(%esp)
 8049f24:	74 28                	je     8049f4e <driver_post+0x3f>
 8049f26:	89 54 24 08          	mov    %edx,0x8(%esp)
 8049f2a:	c7 44 24 04 3f a5 04 	movl   $0x804a53f,0x4(%esp)
 8049f31:	08 
 8049f32:	c7 04 24 01 00 00 00 	movl   $0x1,(%esp)
 8049f39:	e8 62 e9 ff ff       	call   80488a0 <__printf_chk@plt>
 8049f3e:	66 c7 03 4f 4b       	movw   $0x4b4f,(%ebx)
 8049f43:	c6 43 02 00          	movb   $0x0,0x2(%ebx)
 8049f47:	b8 00 00 00 00       	mov    $0x0,%eax
 8049f4c:	eb 49                	jmp    8049f97 <driver_post+0x88>
 8049f4e:	85 c0                	test   %eax,%eax
 8049f50:	74 37                	je     8049f89 <driver_post+0x7a>
 8049f52:	80 38 00             	cmpb   $0x0,(%eax)
 8049f55:	74 32                	je     8049f89 <driver_post+0x7a>
 8049f57:	89 5c 24 18          	mov    %ebx,0x18(%esp)
 8049f5b:	89 54 24 14          	mov    %edx,0x14(%esp)
 8049f5f:	c7 44 24 10 56 a5 04 	movl   $0x804a556,0x10(%esp)
 8049f66:	08 
 8049f67:	89 44 24 0c          	mov    %eax,0xc(%esp)
 8049f6b:	c7 44 24 08 5a a5 04 	movl   $0x804a55a,0x8(%esp)
 8049f72:	08 
 8049f73:	c7 44 24 04 6e 3b 00 	movl   $0x3b6e,0x4(%esp)
 8049f7a:	00 
 8049f7b:	c7 04 24 2c a5 04 08 	movl   $0x804a52c,(%esp)
 8049f82:	e8 f6 f4 ff ff       	call   804947d <submitr>
 8049f87:	eb 0e                	jmp    8049f97 <driver_post+0x88>
 8049f89:	66 c7 03 4f 4b       	movw   $0x4b4f,(%ebx)
 8049f8e:	c6 43 02 00          	movb   $0x0,0x2(%ebx)
 8049f92:	b8 00 00 00 00       	mov    $0x0,%eax
 8049f97:	83 c4 28             	add    $0x28,%esp
 8049f9a:	5b                   	pop    %ebx
 8049f9b:	c3                   	ret    
 8049f9c:	90                   	nop
 8049f9d:	90                   	nop
 8049f9e:	90                   	nop
 8049f9f:	90                   	nop

08049fa0 <__libc_csu_init>:
 8049fa0:	55                   	push   %ebp
 8049fa1:	57                   	push   %edi
 8049fa2:	56                   	push   %esi
 8049fa3:	53                   	push   %ebx
 8049fa4:	e8 69 00 00 00       	call   804a012 <__i686.get_pc_thunk.bx>
 8049fa9:	81 c3 4b 20 00 00    	add    $0x204b,%ebx
 8049faf:	83 ec 1c             	sub    $0x1c,%esp
 8049fb2:	8b 6c 24 30          	mov    0x30(%esp),%ebp
 8049fb6:	8d bb 20 ff ff ff    	lea    -0xe0(%ebx),%edi
 8049fbc:	e8 63 e7 ff ff       	call   8048724 <_init>
 8049fc1:	8d 83 20 ff ff ff    	lea    -0xe0(%ebx),%eax
 8049fc7:	29 c7                	sub    %eax,%edi
 8049fc9:	c1 ff 02             	sar    $0x2,%edi
 8049fcc:	85 ff                	test   %edi,%edi
 8049fce:	74 29                	je     8049ff9 <__libc_csu_init+0x59>
 8049fd0:	31 f6                	xor    %esi,%esi
 8049fd2:	8d b6 00 00 00 00    	lea    0x0(%esi),%esi
 8049fd8:	8b 44 24 38          	mov    0x38(%esp),%eax
 8049fdc:	89 2c 24             	mov    %ebp,(%esp)
 8049fdf:	89 44 24 08          	mov    %eax,0x8(%esp)
 8049fe3:	8b 44 24 34          	mov    0x34(%esp),%eax
 8049fe7:	89 44 24 04          	mov    %eax,0x4(%esp)
 8049feb:	ff 94 b3 20 ff ff ff 	call   *-0xe0(%ebx,%esi,4)
 8049ff2:	83 c6 01             	add    $0x1,%esi
 8049ff5:	39 fe                	cmp    %edi,%esi
 8049ff7:	75 df                	jne    8049fd8 <__libc_csu_init+0x38>
 8049ff9:	83 c4 1c             	add    $0x1c,%esp
 8049ffc:	5b                   	pop    %ebx
 8049ffd:	5e                   	pop    %esi
 8049ffe:	5f                   	pop    %edi
 8049fff:	5d                   	pop    %ebp
 804a000:	c3                   	ret    
 804a001:	eb 0d                	jmp    804a010 <__libc_csu_fini>
 804a003:	90                   	nop
 804a004:	90                   	nop
 804a005:	90                   	nop
 804a006:	90                   	nop
 804a007:	90                   	nop
 804a008:	90                   	nop
 804a009:	90                   	nop
 804a00a:	90                   	nop
 804a00b:	90                   	nop
 804a00c:	90                   	nop
 804a00d:	90                   	nop
 804a00e:	90                   	nop
 804a00f:	90                   	nop

0804a010 <__libc_csu_fini>:
 804a010:	f3 c3                	repz ret 

0804a012 <__i686.get_pc_thunk.bx>:
 804a012:	8b 1c 24             	mov    (%esp),%ebx
 804a015:	c3                   	ret    
 804a016:	90                   	nop
 804a017:	90                   	nop
 804a018:	90                   	nop
 804a019:	90                   	nop
 804a01a:	90                   	nop
 804a01b:	90                   	nop
 804a01c:	90                   	nop
 804a01d:	90                   	nop
 804a01e:	90                   	nop
 804a01f:	90                   	nop

0804a020 <__do_global_ctors_aux>:
 804a020:	55                   	push   %ebp
 804a021:	89 e5                	mov    %esp,%ebp
 804a023:	53                   	push   %ebx
 804a024:	83 ec 04             	sub    $0x4,%esp
 804a027:	a1 14 bf 04 08       	mov    0x804bf14,%eax
 804a02c:	83 f8 ff             	cmp    $0xffffffff,%eax
 804a02f:	74 13                	je     804a044 <__do_global_ctors_aux+0x24>
 804a031:	bb 14 bf 04 08       	mov    $0x804bf14,%ebx
 804a036:	66 90                	xchg   %ax,%ax
 804a038:	83 eb 04             	sub    $0x4,%ebx
 804a03b:	ff d0                	call   *%eax
 804a03d:	8b 03                	mov    (%ebx),%eax
 804a03f:	83 f8 ff             	cmp    $0xffffffff,%eax
 804a042:	75 f4                	jne    804a038 <__do_global_ctors_aux+0x18>
 804a044:	83 c4 04             	add    $0x4,%esp
 804a047:	5b                   	pop    %ebx
 804a048:	5d                   	pop    %ebp
 804a049:	c3                   	ret    
 804a04a:	90                   	nop
 804a04b:	90                   	nop

Disassembly of section .fini:

0804a04c <_fini>:
 804a04c:	53                   	push   %ebx
 804a04d:	83 ec 08             	sub    $0x8,%esp
 804a050:	e8 00 00 00 00       	call   804a055 <_fini+0x9>
 804a055:	5b                   	pop    %ebx
 804a056:	81 c3 9f 1f 00 00    	add    $0x1f9f,%ebx
 804a05c:	e8 ff e8 ff ff       	call   8048960 <__do_global_dtors_aux>
 804a061:	83 c4 08             	add    $0x8,%esp
 804a064:	5b                   	pop    %ebx
 804a065:	c3                   	ret    
