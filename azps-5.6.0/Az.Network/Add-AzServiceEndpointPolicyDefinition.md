---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 9a9795547a1d9699a185ae8957852b41d26ca321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908865"
---
# <span data-ttu-id="20610-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20610-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="20610-102">簡介</span><span class="sxs-lookup"><span data-stu-id="20610-102">SYNOPSIS</span></span>
<span data-ttu-id="20610-103">新增服務端點策略定義至指定的策略。</span><span class="sxs-lookup"><span data-stu-id="20610-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="20610-104">語法</span><span class="sxs-lookup"><span data-stu-id="20610-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20610-105">描述</span><span class="sxs-lookup"><span data-stu-id="20610-105">DESCRIPTION</span></span>
<span data-ttu-id="20610-106">**Add-AzServiceEndpointPolicyDefinition** Cmdlet 會新增服務端點策略定義至該策略。</span><span class="sxs-lookup"><span data-stu-id="20610-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="20610-107">例子</span><span class="sxs-lookup"><span data-stu-id="20610-107">EXAMPLES</span></span>

### <span data-ttu-id="20610-108">範例 1：更新服務端點策略中的服務端點策略定義</span><span class="sxs-lookup"><span data-stu-id="20610-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="20610-109">此命令更新服務端點策略定義，名稱為 ServiceEndpointPolicyDefinition1、Service Microsoft.Storage、服務資源訂閱/sub1，以及屬於 ResourceGroup01 資源群組的「新定義」，並儲存在 $policydef 變數中。</span><span class="sxs-lookup"><span data-stu-id="20610-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="20610-110">參數</span><span class="sxs-lookup"><span data-stu-id="20610-110">PARAMETERS</span></span>

### <span data-ttu-id="20610-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20610-111">-DefaultProfile</span></span>
<span data-ttu-id="20610-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="20610-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20610-113">-描述</span><span class="sxs-lookup"><span data-stu-id="20610-113">-Description</span></span>
<span data-ttu-id="20610-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="20610-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20610-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="20610-115">-Name</span></span>
<span data-ttu-id="20610-116">服務端點策略定義的名稱</span><span class="sxs-lookup"><span data-stu-id="20610-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="20610-117">-服務</span><span class="sxs-lookup"><span data-stu-id="20610-117">-Service</span></span>
<span data-ttu-id="20610-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="20610-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20610-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="20610-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="20610-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="20610-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="20610-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="20610-121">-ServiceResource</span></span>
<span data-ttu-id="20610-122">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="20610-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20610-123">-確認</span><span class="sxs-lookup"><span data-stu-id="20610-123">-Confirm</span></span>
<span data-ttu-id="20610-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="20610-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20610-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20610-125">-WhatIf</span></span>
<span data-ttu-id="20610-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20610-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20610-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20610-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20610-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20610-128">CommonParameters</span></span>
<span data-ttu-id="20610-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="20610-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20610-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="20610-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20610-131">輸入</span><span class="sxs-lookup"><span data-stu-id="20610-131">INPUTS</span></span>

### <span data-ttu-id="20610-132">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="20610-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="20610-133">輸出</span><span class="sxs-lookup"><span data-stu-id="20610-133">OUTPUTS</span></span>

### <span data-ttu-id="20610-134">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="20610-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="20610-135">筆記</span><span class="sxs-lookup"><span data-stu-id="20610-135">NOTES</span></span>

## <span data-ttu-id="20610-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="20610-136">RELATED LINKS</span></span>

[<span data-ttu-id="20610-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20610-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="20610-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20610-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="20610-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20610-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="20610-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20610-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
