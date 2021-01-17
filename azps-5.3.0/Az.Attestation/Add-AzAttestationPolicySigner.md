---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287499"
---
# <span data-ttu-id="afb99-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="afb99-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="afb99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afb99-102">SYNOPSIS</span></span>
<span data-ttu-id="afb99-103">針對 Azure 證明中的租使用者，新增受信任的原則簽章者。</span><span class="sxs-lookup"><span data-stu-id="afb99-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="afb99-104">句法</span><span class="sxs-lookup"><span data-stu-id="afb99-104">SYNTAX</span></span>

### <span data-ttu-id="afb99-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="afb99-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb99-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afb99-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb99-107">說明</span><span class="sxs-lookup"><span data-stu-id="afb99-107">DESCRIPTION</span></span>
<span data-ttu-id="afb99-108">Add-AzAttestationPolicySigner Cmdlet 會針對 Azure 證明中的租使用者新增受信任的原則簽章者。</span><span class="sxs-lookup"><span data-stu-id="afb99-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="afb99-109">示例</span><span class="sxs-lookup"><span data-stu-id="afb99-109">EXAMPLES</span></span>

### <span data-ttu-id="afb99-110">範例1</span><span class="sxs-lookup"><span data-stu-id="afb99-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="afb99-111">為名為 *pshtest* 的 Atteestation 提供者新增受信任的簽章者。</span><span class="sxs-lookup"><span data-stu-id="afb99-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="afb99-112">參數</span><span class="sxs-lookup"><span data-stu-id="afb99-112">PARAMETERS</span></span>

### <span data-ttu-id="afb99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb99-113">-DefaultProfile</span></span>
<span data-ttu-id="afb99-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="afb99-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb99-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="afb99-115">-Name</span></span>
<span data-ttu-id="afb99-116">指定認證提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="afb99-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="afb99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb99-117">-ResourceGroupName</span></span>
<span data-ttu-id="afb99-118">指定證明提供者的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="afb99-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="afb99-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afb99-119">-ResourceId</span></span>
<span data-ttu-id="afb99-120">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="afb99-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="afb99-121">-簽章者</span><span class="sxs-lookup"><span data-stu-id="afb99-121">-Signer</span></span>
<span data-ttu-id="afb99-122">指定包含名為 "maa-policyCertificate" 的 RFC7519 JSON Web 權杖，其值是包含要新增之新信任簽章金鑰的 RFC7517 JSON Web 金鑰。</span><span class="sxs-lookup"><span data-stu-id="afb99-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="afb99-123">RFC7519 JWT 必須以其中一個現有的信任簽入金鑰來簽署。</span><span class="sxs-lookup"><span data-stu-id="afb99-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="afb99-124">-確認</span><span class="sxs-lookup"><span data-stu-id="afb99-124">-Confirm</span></span>
<span data-ttu-id="afb99-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="afb99-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb99-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb99-126">-WhatIf</span></span>
<span data-ttu-id="afb99-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afb99-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb99-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afb99-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb99-129">CommonParameters</span></span>
<span data-ttu-id="afb99-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afb99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb99-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="afb99-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb99-132">輸入</span><span class="sxs-lookup"><span data-stu-id="afb99-132">INPUTS</span></span>

### <span data-ttu-id="afb99-133">System.object</span><span class="sxs-lookup"><span data-stu-id="afb99-133">System.String</span></span>

## <span data-ttu-id="afb99-134">輸出</span><span class="sxs-lookup"><span data-stu-id="afb99-134">OUTPUTS</span></span>

### <span data-ttu-id="afb99-135">PSPolicySigners 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="afb99-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="afb99-136">筆記</span><span class="sxs-lookup"><span data-stu-id="afb99-136">NOTES</span></span>

## <span data-ttu-id="afb99-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="afb99-137">RELATED LINKS</span></span>
