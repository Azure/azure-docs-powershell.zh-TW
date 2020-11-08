---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965433"
---
# <span data-ttu-id="7bdde-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7bdde-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="7bdde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bdde-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdde-103">移除服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="7bdde-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="7bdde-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bdde-104">SYNTAX</span></span>

### <span data-ttu-id="7bdde-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7bdde-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bdde-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bdde-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bdde-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bdde-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bdde-108">說明</span><span class="sxs-lookup"><span data-stu-id="7bdde-108">DESCRIPTION</span></span>
<span data-ttu-id="7bdde-109">**AzServiceEndpointPolicy** Cmdlet 會移除服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="7bdde-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="7bdde-110">示例</span><span class="sxs-lookup"><span data-stu-id="7bdde-110">EXAMPLES</span></span>

### <span data-ttu-id="7bdde-111">範例1：使用名稱移除服務端點原則</span><span class="sxs-lookup"><span data-stu-id="7bdde-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="7bdde-112">這個命令會移除名稱為 PolicyDef1 的服務端點原則</span><span class="sxs-lookup"><span data-stu-id="7bdde-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="7bdde-113">參數</span><span class="sxs-lookup"><span data-stu-id="7bdde-113">PARAMETERS</span></span>

### <span data-ttu-id="7bdde-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdde-114">-DefaultProfile</span></span>
<span data-ttu-id="7bdde-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bdde-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bdde-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bdde-116">-InputObject</span></span>
<span data-ttu-id="7bdde-117">服務端點原則定義物件。</span><span class="sxs-lookup"><span data-stu-id="7bdde-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bdde-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bdde-118">-Name</span></span>
<span data-ttu-id="7bdde-119">服務端點定義的名稱</span><span class="sxs-lookup"><span data-stu-id="7bdde-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdde-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bdde-120">-ResourceId</span></span>
<span data-ttu-id="7bdde-121">服務端點定義的 ID。</span><span class="sxs-lookup"><span data-stu-id="7bdde-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bdde-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7bdde-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="7bdde-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7bdde-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bdde-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7bdde-124">-Confirm</span></span>
<span data-ttu-id="7bdde-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7bdde-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bdde-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bdde-126">-WhatIf</span></span>
<span data-ttu-id="7bdde-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bdde-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bdde-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bdde-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bdde-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdde-129">CommonParameters</span></span>
<span data-ttu-id="7bdde-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bdde-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdde-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7bdde-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdde-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7bdde-132">INPUTS</span></span>

### <span data-ttu-id="7bdde-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7bdde-133">System.String</span></span>

### <span data-ttu-id="7bdde-134">PSServiceEndpointPolicyDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7bdde-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="7bdde-135">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7bdde-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="7bdde-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7bdde-136">OUTPUTS</span></span>

### <span data-ttu-id="7bdde-137">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7bdde-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="7bdde-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7bdde-138">NOTES</span></span>

## <span data-ttu-id="7bdde-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bdde-139">RELATED LINKS</span></span>

[<span data-ttu-id="7bdde-140">附加 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7bdde-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7bdde-141">AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7bdde-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7bdde-142">新-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7bdde-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7bdde-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7bdde-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)