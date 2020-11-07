---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 0c36f5fb87e3d247a48031bdc735c077a577ac27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958677"
---
# <span data-ttu-id="bf625-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="bf625-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="bf625-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf625-102">SYNOPSIS</span></span>
<span data-ttu-id="bf625-103">從 Azure 證明中的租使用者取得原則。</span><span class="sxs-lookup"><span data-stu-id="bf625-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bf625-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf625-104">SYNTAX</span></span>

### <span data-ttu-id="bf625-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf625-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf625-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf625-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf625-107">說明</span><span class="sxs-lookup"><span data-stu-id="bf625-107">DESCRIPTION</span></span>
<span data-ttu-id="bf625-108">Get-AzAttestationPolicy Cmdlet 會從 Azure 證明中的租使用者取得原則。</span><span class="sxs-lookup"><span data-stu-id="bf625-108">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bf625-109">示例</span><span class="sxs-lookup"><span data-stu-id="bf625-109">EXAMPLES</span></span>

### <span data-ttu-id="bf625-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bf625-110">Example 1</span></span>
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

<span data-ttu-id="bf625-111">取得 t 類型 *SgxEnclave* 之認證提供者 *pshtest* 的原則。</span><span class="sxs-lookup"><span data-stu-id="bf625-111">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="bf625-112">參數</span><span class="sxs-lookup"><span data-stu-id="bf625-112">PARAMETERS</span></span>

### <span data-ttu-id="bf625-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf625-113">-DefaultProfile</span></span>
<span data-ttu-id="bf625-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf625-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf625-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf625-115">-Name</span></span>
<span data-ttu-id="bf625-116">指定租使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf625-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="bf625-117">這個 Cmdlet 會取得此參數指定之租使用者的證明原則。</span><span class="sxs-lookup"><span data-stu-id="bf625-117">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf625-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf625-118">-ResourceGroupName</span></span>
<span data-ttu-id="bf625-119">指定證明提供者的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bf625-119">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="bf625-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf625-120">-ResourceId</span></span>
<span data-ttu-id="bf625-121">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="bf625-121">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="bf625-122">-T</span><span class="sxs-lookup"><span data-stu-id="bf625-122">-Tee</span></span>
<span data-ttu-id="bf625-123">指定信任的執行環境類型。</span><span class="sxs-lookup"><span data-stu-id="bf625-123">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="bf625-124">我們支援四種類型的環境： SgxEnclave、OpenEnclave、CyResComponent 和 VBSEnclave。</span><span class="sxs-lookup"><span data-stu-id="bf625-124">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="bf625-125">-確認</span><span class="sxs-lookup"><span data-stu-id="bf625-125">-Confirm</span></span>
<span data-ttu-id="bf625-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf625-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf625-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf625-127">-WhatIf</span></span>
<span data-ttu-id="bf625-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf625-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf625-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf625-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf625-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf625-130">CommonParameters</span></span>
<span data-ttu-id="bf625-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf625-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf625-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bf625-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf625-133">輸入</span><span class="sxs-lookup"><span data-stu-id="bf625-133">INPUTS</span></span>

### <span data-ttu-id="bf625-134">System.object</span><span class="sxs-lookup"><span data-stu-id="bf625-134">System.String</span></span>

## <span data-ttu-id="bf625-135">輸出</span><span class="sxs-lookup"><span data-stu-id="bf625-135">OUTPUTS</span></span>

### <span data-ttu-id="bf625-136">PSPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bf625-136">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="bf625-137">筆記</span><span class="sxs-lookup"><span data-stu-id="bf625-137">NOTES</span></span>

## <span data-ttu-id="bf625-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf625-138">RELATED LINKS</span></span>
