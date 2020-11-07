---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 27124aa859fc9c97a74a3ed401c67de328d93884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959189"
---
# <span data-ttu-id="531b7-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="531b7-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="531b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="531b7-102">SYNOPSIS</span></span>
<span data-ttu-id="531b7-103">建立服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="531b7-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="531b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="531b7-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="531b7-105">說明</span><span class="sxs-lookup"><span data-stu-id="531b7-105">DESCRIPTION</span></span>
<span data-ttu-id="531b7-106">**AzServiceEndpointPolicyDefinition** Cmdlet 會建立服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="531b7-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="531b7-107">示例</span><span class="sxs-lookup"><span data-stu-id="531b7-107">EXAMPLES</span></span>

### <span data-ttu-id="531b7-108">範例1：建立服務端點原則</span><span class="sxs-lookup"><span data-stu-id="531b7-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="531b7-109">這個命令會建立服務端點原則定義與 name ServiceEndpointPolicyDefinition1、service name、service 資源訂閱/sub1，以及將其儲存在 $policydef 變數中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="531b7-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="531b7-110">參數</span><span class="sxs-lookup"><span data-stu-id="531b7-110">PARAMETERS</span></span>

### <span data-ttu-id="531b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531b7-111">-DefaultProfile</span></span>
<span data-ttu-id="531b7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="531b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="531b7-113">-描述</span><span class="sxs-lookup"><span data-stu-id="531b7-113">-Description</span></span>
<span data-ttu-id="531b7-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="531b7-114">The description of the definition</span></span>

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

### <span data-ttu-id="531b7-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="531b7-115">-Name</span></span>
<span data-ttu-id="531b7-116">服務端點原則的名稱</span><span class="sxs-lookup"><span data-stu-id="531b7-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="531b7-117">-服務</span><span class="sxs-lookup"><span data-stu-id="531b7-117">-Service</span></span>
<span data-ttu-id="531b7-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="531b7-118">Name of the service</span></span>

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

### <span data-ttu-id="531b7-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="531b7-119">-ServiceResource</span></span>
<span data-ttu-id="531b7-120">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="531b7-120">List of service resources</span></span>

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

### <span data-ttu-id="531b7-121">-確認</span><span class="sxs-lookup"><span data-stu-id="531b7-121">-Confirm</span></span>
<span data-ttu-id="531b7-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="531b7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="531b7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531b7-123">-WhatIf</span></span>
<span data-ttu-id="531b7-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="531b7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="531b7-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="531b7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="531b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531b7-126">CommonParameters</span></span>
<span data-ttu-id="531b7-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="531b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531b7-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="531b7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531b7-129">輸入</span><span class="sxs-lookup"><span data-stu-id="531b7-129">INPUTS</span></span>

### <span data-ttu-id="531b7-130">所有</span><span class="sxs-lookup"><span data-stu-id="531b7-130">None</span></span>

## <span data-ttu-id="531b7-131">輸出</span><span class="sxs-lookup"><span data-stu-id="531b7-131">OUTPUTS</span></span>

### <span data-ttu-id="531b7-132">PSServiceEndpointPolicyDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="531b7-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="531b7-133">筆記</span><span class="sxs-lookup"><span data-stu-id="531b7-133">NOTES</span></span>

## <span data-ttu-id="531b7-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="531b7-134">RELATED LINKS</span></span>

[<span data-ttu-id="531b7-135">附加 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="531b7-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="531b7-136">AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="531b7-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="531b7-137">移除-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="531b7-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="531b7-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="531b7-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
