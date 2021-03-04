---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 498777c6413cf4f80d32b50b4fb40da6216e43a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910313"
---
# <span data-ttu-id="9b73f-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="9b73f-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="9b73f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b73f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b73f-103">從 Azure 的租使用者中獲取該策略。</span><span class="sxs-lookup"><span data-stu-id="9b73f-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="9b73f-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b73f-104">SYNTAX</span></span>

### <span data-ttu-id="9b73f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b73f-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b73f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b73f-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b73f-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b73f-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b73f-108">描述</span><span class="sxs-lookup"><span data-stu-id="9b73f-108">DESCRIPTION</span></span>
<span data-ttu-id="9b73f-109">Cmdlet Get-AzAttestationPolicy Azure 的租使用者中，從該租使用者獲得該策略。</span><span class="sxs-lookup"><span data-stu-id="9b73f-109">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="9b73f-110">例子</span><span class="sxs-lookup"><span data-stu-id="9b73f-110">EXAMPLES</span></span>

### <span data-ttu-id="9b73f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9b73f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="9b73f-112">針對 Tee 類型 *SgxEnclave，* 獲得證明提供者 *pshtest* 之政策。</span><span class="sxs-lookup"><span data-stu-id="9b73f-112">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="9b73f-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="9b73f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -DefaultProvider -Location "UK South" -Tee SgxEnclave
Text       : version= 1.0;authorizationrules{c:[type=="$is-debuggable"] => permit();};issuancerules{c:[type=="$is-debuggable"] => issue(type="is-debuggable",
             value=c.value);c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave",
             value=c.value);c:[type=="$product-id"] => issue(type="product-id", value=c.value);c:[type=="$svn"] => issue(type="svn", value=c.value);c:[type=="$tee"]
             => issue(type="tee", value=c.value);};
TextLength : 479
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3TzJGMWRHaHZjbWw2WVhScGIyNXlkV3hsYzN0ak9sdDBlWEJsUFQwaUpHbHpMV1JsWW5WbloyRmliR1Vp
             WFNBOVBpQndaWEp0YVhRb0tUdDlPMmx6YzNWaGJtTmxjblZzWlhON1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pT
             SXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBTSWtjMmQ0TFcxeWMybG5ibVZ5SWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXljMmxuYm1WeUlpd2dkbUZzZFdVOVl5NTJZV3gx
             WlNrN1l6cGJkSGx3WlQwOUlpUnpaM2d0YlhKbGJtTnNZWFpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXlaVzVqYkdGMlpTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBT
             SWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHRqT2x0MGVYQmxQVDBpSkhOMmJpSmRJRDAtSUdsemMzVmxLSFI1
             Y0dVOUluTjJiaUlzSUhaaGJIVmxQV011ZG1Gc2RXVXBPMk02VzNSNWNHVTlQU0lrZEdWbElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWRHVmxJaXdnZG1Gc2RXVTlZeTUyWVd4MVpTazdmVHMifQ.
JwtLength  : 907
Algorithm  : none
```

<span data-ttu-id="9b73f-114">從位置 UK *South* for Tee 類型 *SgxEnclave 獲得證明預設提供者的政策*。</span><span class="sxs-lookup"><span data-stu-id="9b73f-114">Gets the policy for Attestation Default Provider from Location *UK South* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="9b73f-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b73f-115">PARAMETERS</span></span>

### <span data-ttu-id="9b73f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b73f-116">-DefaultProfile</span></span>
<span data-ttu-id="9b73f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b73f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-118">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="9b73f-118">-DefaultProvider</span></span>
<span data-ttu-id="9b73f-119">指定這是要求給預設證明提供者。</span><span class="sxs-lookup"><span data-stu-id="9b73f-119">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-120">-位置</span><span class="sxs-lookup"><span data-stu-id="9b73f-120">-Location</span></span>
<span data-ttu-id="9b73f-121">指定預設證明提供者的位置。</span><span class="sxs-lookup"><span data-stu-id="9b73f-121">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b73f-122">-Name</span></span>
<span data-ttu-id="9b73f-123">指定租使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b73f-123">Specifies a name of the tenant.</span></span>
<span data-ttu-id="9b73f-124">此 Cmdlet 會針對此參數指定的租使用者，獲得證明政策。</span><span class="sxs-lookup"><span data-stu-id="9b73f-124">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b73f-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b73f-126">指定驗證提供者的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9b73f-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b73f-127">-ResourceId</span></span>
<span data-ttu-id="9b73f-128">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="9b73f-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="9b73f-129">-Tee</span></span>
<span data-ttu-id="9b73f-130">指定信任的執行環境類型。</span><span class="sxs-lookup"><span data-stu-id="9b73f-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="9b73f-131">我們支援四種類型的環境：SgxEnclave、OpenEnclave、CyResComponent 和 VBSEnclave。</span><span class="sxs-lookup"><span data-stu-id="9b73f-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9b73f-132">-Confirm</span></span>
<span data-ttu-id="9b73f-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9b73f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b73f-134">-WhatIf</span></span>
<span data-ttu-id="9b73f-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b73f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b73f-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b73f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b73f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b73f-137">CommonParameters</span></span>
<span data-ttu-id="9b73f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b73f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b73f-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b73f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b73f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9b73f-140">INPUTS</span></span>

### <span data-ttu-id="9b73f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9b73f-141">System.String</span></span>

## <span data-ttu-id="9b73f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9b73f-142">OUTPUTS</span></span>

### <span data-ttu-id="9b73f-143">Microsoft.Azure.Commands.點出ation.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9b73f-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="9b73f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9b73f-144">NOTES</span></span>

## <span data-ttu-id="9b73f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b73f-145">RELATED LINKS</span></span>
