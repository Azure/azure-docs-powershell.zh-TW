---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958482"
---
# <span data-ttu-id="f6791-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6791-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f6791-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6791-102">SYNOPSIS</span></span>
<span data-ttu-id="f6791-103">將服務端點原則定義新增到指定的原則。</span><span class="sxs-lookup"><span data-stu-id="f6791-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="f6791-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6791-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6791-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6791-105">DESCRIPTION</span></span>
<span data-ttu-id="f6791-106">**AzServiceEndpointPolicyDefinition** Cmdlet 會將服務端點原則定義新增至原則。</span><span class="sxs-lookup"><span data-stu-id="f6791-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="f6791-107">示例</span><span class="sxs-lookup"><span data-stu-id="f6791-107">EXAMPLES</span></span>

### <span data-ttu-id="f6791-108">範例1：更新服務端點原則中的服務端點原則定義</span><span class="sxs-lookup"><span data-stu-id="f6791-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="f6791-109">這個命令會更新服務端點原則定義與 name ServiceEndpointPolicyDefinition1、service name、service 資源訂閱/sub1，以及將其儲存在 $policydef 變數中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f6791-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="f6791-110">參數</span><span class="sxs-lookup"><span data-stu-id="f6791-110">PARAMETERS</span></span>

### <span data-ttu-id="f6791-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6791-111">-DefaultProfile</span></span>
<span data-ttu-id="f6791-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6791-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6791-113">-描述</span><span class="sxs-lookup"><span data-stu-id="f6791-113">-Description</span></span>
<span data-ttu-id="f6791-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="f6791-114">The description of the definition</span></span>

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

### <span data-ttu-id="f6791-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6791-115">-Name</span></span>
<span data-ttu-id="f6791-116">服務端點原則定義的名稱</span><span class="sxs-lookup"><span data-stu-id="f6791-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="f6791-117">-服務</span><span class="sxs-lookup"><span data-stu-id="f6791-117">-Service</span></span>
<span data-ttu-id="f6791-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="f6791-118">Name of the service</span></span>

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

### <span data-ttu-id="f6791-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f6791-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f6791-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f6791-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="f6791-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="f6791-121">-ServiceResource</span></span>
<span data-ttu-id="f6791-122">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="f6791-122">List of service resources</span></span>

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

### <span data-ttu-id="f6791-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f6791-123">-Confirm</span></span>
<span data-ttu-id="f6791-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6791-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6791-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6791-125">-WhatIf</span></span>
<span data-ttu-id="f6791-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6791-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6791-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6791-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6791-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6791-128">CommonParameters</span></span>
<span data-ttu-id="f6791-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6791-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6791-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6791-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6791-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f6791-131">INPUTS</span></span>

### <span data-ttu-id="f6791-132">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6791-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f6791-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f6791-133">OUTPUTS</span></span>

### <span data-ttu-id="f6791-134">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6791-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f6791-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f6791-135">NOTES</span></span>

## <span data-ttu-id="f6791-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6791-136">RELATED LINKS</span></span>

[<span data-ttu-id="f6791-137">AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6791-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f6791-138">新-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6791-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f6791-139">移除-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6791-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f6791-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6791-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)