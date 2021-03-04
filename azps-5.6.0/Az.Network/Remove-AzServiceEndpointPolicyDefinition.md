---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 65303db1c76f6e7c6e1323ed0cfc88132e4c1c23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915986"
---
# <span data-ttu-id="197e6-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="197e6-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="197e6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="197e6-102">SYNOPSIS</span></span>
<span data-ttu-id="197e6-103">移除服務端點策略定義。</span><span class="sxs-lookup"><span data-stu-id="197e6-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="197e6-104">語法</span><span class="sxs-lookup"><span data-stu-id="197e6-104">SYNTAX</span></span>

### <span data-ttu-id="197e6-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="197e6-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="197e6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="197e6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="197e6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="197e6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="197e6-108">描述</span><span class="sxs-lookup"><span data-stu-id="197e6-108">DESCRIPTION</span></span>
<span data-ttu-id="197e6-109">**Remove-AzServiceEndpointPolicy** Cmdlet 會移除服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="197e6-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="197e6-110">例子</span><span class="sxs-lookup"><span data-stu-id="197e6-110">EXAMPLES</span></span>

### <span data-ttu-id="197e6-111">範例 1：使用名稱移除服務端點策略</span><span class="sxs-lookup"><span data-stu-id="197e6-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="197e6-112">此命令會移除名稱為 PolicyDef1 的服務端點策略</span><span class="sxs-lookup"><span data-stu-id="197e6-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="197e6-113">參數</span><span class="sxs-lookup"><span data-stu-id="197e6-113">PARAMETERS</span></span>

### <span data-ttu-id="197e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="197e6-114">-DefaultProfile</span></span>
<span data-ttu-id="197e6-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="197e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="197e6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="197e6-116">-InputObject</span></span>
<span data-ttu-id="197e6-117">服務端點策略定義物件。</span><span class="sxs-lookup"><span data-stu-id="197e6-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="197e6-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="197e6-118">-Name</span></span>
<span data-ttu-id="197e6-119">服務端點定義的名稱</span><span class="sxs-lookup"><span data-stu-id="197e6-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="197e6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="197e6-120">-ResourceId</span></span>
<span data-ttu-id="197e6-121">服務端點定義的識別碼。</span><span class="sxs-lookup"><span data-stu-id="197e6-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="197e6-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="197e6-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="197e6-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="197e6-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="197e6-124">-確認</span><span class="sxs-lookup"><span data-stu-id="197e6-124">-Confirm</span></span>
<span data-ttu-id="197e6-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="197e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="197e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="197e6-126">-WhatIf</span></span>
<span data-ttu-id="197e6-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="197e6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="197e6-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="197e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="197e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="197e6-129">CommonParameters</span></span>
<span data-ttu-id="197e6-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="197e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="197e6-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="197e6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="197e6-132">輸入</span><span class="sxs-lookup"><span data-stu-id="197e6-132">INPUTS</span></span>

### <span data-ttu-id="197e6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="197e6-133">System.String</span></span>

### <span data-ttu-id="197e6-134">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="197e6-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="197e6-135">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="197e6-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="197e6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="197e6-136">OUTPUTS</span></span>

### <span data-ttu-id="197e6-137">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="197e6-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="197e6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="197e6-138">NOTES</span></span>

## <span data-ttu-id="197e6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="197e6-139">RELATED LINKS</span></span>

[<span data-ttu-id="197e6-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="197e6-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="197e6-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="197e6-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="197e6-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="197e6-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="197e6-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="197e6-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
