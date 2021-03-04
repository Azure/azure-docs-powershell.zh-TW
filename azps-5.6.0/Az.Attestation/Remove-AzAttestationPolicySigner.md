---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: e0b86a1cd7c3e1355cfc760fecc257b3cde87561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905625"
---
# <span data-ttu-id="eeaa5-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="eeaa5-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="eeaa5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eeaa5-102">SYNOPSIS</span></span>
<span data-ttu-id="eeaa5-103">移除 Azure 的租使用者信任之政策簽署者。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="eeaa5-104">語法</span><span class="sxs-lookup"><span data-stu-id="eeaa5-104">SYNTAX</span></span>

### <span data-ttu-id="eeaa5-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeaa5-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeaa5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeaa5-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeaa5-107">描述</span><span class="sxs-lookup"><span data-stu-id="eeaa5-107">DESCRIPTION</span></span>
<span data-ttu-id="eeaa5-108">此Remove-AzAttestationPolicySigner Cmdlet 會移除 Azure 的租使用者信任之政策簽署者。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="eeaa5-109">例子</span><span class="sxs-lookup"><span data-stu-id="eeaa5-109">EXAMPLES</span></span>

### <span data-ttu-id="eeaa5-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="eeaa5-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="eeaa5-111">移除名為 pshtest 之證明提供者的受信任 *簽名者*。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="eeaa5-112">參數</span><span class="sxs-lookup"><span data-stu-id="eeaa5-112">PARAMETERS</span></span>

### <span data-ttu-id="eeaa5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeaa5-113">-DefaultProfile</span></span>
<span data-ttu-id="eeaa5-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeaa5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eeaa5-115">-Name</span></span>
<span data-ttu-id="eeaa5-116">指定證明提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="eeaa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeaa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="eeaa5-118">指定驗證提供者的資源組名。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="eeaa5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeaa5-119">-ResourceId</span></span>
<span data-ttu-id="eeaa5-120">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="eeaa5-121">-簽署者</span><span class="sxs-lookup"><span data-stu-id="eeaa5-121">-Signer</span></span>
<span data-ttu-id="eeaa5-122">指定 RFC7519 JSON Web Token，其中包含名為 "maa-policyCertificate" 的索賠，其值為 RFC7517 JSON Web Key，其中包含要移除的受信任簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="eeaa5-123">RFC7519 JWT 必須使用其中一個現有的信任簽署金鑰簽署。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="eeaa5-124">-確認</span><span class="sxs-lookup"><span data-stu-id="eeaa5-124">-Confirm</span></span>
<span data-ttu-id="eeaa5-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeaa5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeaa5-126">-WhatIf</span></span>
<span data-ttu-id="eeaa5-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeaa5-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeaa5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeaa5-129">CommonParameters</span></span>
<span data-ttu-id="eeaa5-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eeaa5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeaa5-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eeaa5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeaa5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="eeaa5-132">INPUTS</span></span>

### <span data-ttu-id="eeaa5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="eeaa5-133">System.String</span></span>

## <span data-ttu-id="eeaa5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="eeaa5-134">OUTPUTS</span></span>

### <span data-ttu-id="eeaa5-135">Microsoft.Azure.Commands.點出ation.models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="eeaa5-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="eeaa5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="eeaa5-136">NOTES</span></span>

## <span data-ttu-id="eeaa5-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="eeaa5-137">RELATED LINKS</span></span>
