---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: bc68a57437bae2af10b5ee39221459aebf82a2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916713"
---
# <span data-ttu-id="666e0-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="666e0-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="666e0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="666e0-102">SYNOPSIS</span></span>
<span data-ttu-id="666e0-103">更新服務端點策略定義。</span><span class="sxs-lookup"><span data-stu-id="666e0-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="666e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="666e0-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="666e0-105">描述</span><span class="sxs-lookup"><span data-stu-id="666e0-105">DESCRIPTION</span></span>
<span data-ttu-id="666e0-106">**Set-AzServiceEndpointPolicyDefinition** Cmdlet 會建立服務端點策略定義。</span><span class="sxs-lookup"><span data-stu-id="666e0-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="666e0-107">例子</span><span class="sxs-lookup"><span data-stu-id="666e0-107">EXAMPLES</span></span>

### <span data-ttu-id="666e0-108">範例 1：更新服務端點策略中的服務端點策略定義</span><span class="sxs-lookup"><span data-stu-id="666e0-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="666e0-109">此命令會更新由物件定義之服務端點策略中名為 Policydef1 的服務端點$ServiceEndpointPolicy。</span><span class="sxs-lookup"><span data-stu-id="666e0-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="666e0-110">參數</span><span class="sxs-lookup"><span data-stu-id="666e0-110">PARAMETERS</span></span>

### <span data-ttu-id="666e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666e0-111">-DefaultProfile</span></span>
<span data-ttu-id="666e0-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="666e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="666e0-113">-描述</span><span class="sxs-lookup"><span data-stu-id="666e0-113">-Description</span></span>
<span data-ttu-id="666e0-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="666e0-114">The description of the definition</span></span>

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

### <span data-ttu-id="666e0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="666e0-115">-Name</span></span>
<span data-ttu-id="666e0-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="666e0-116">The name of the rule</span></span>

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

### <span data-ttu-id="666e0-117">-服務</span><span class="sxs-lookup"><span data-stu-id="666e0-117">-Service</span></span>
<span data-ttu-id="666e0-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="666e0-118">Name of the service</span></span>

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

### <span data-ttu-id="666e0-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="666e0-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="666e0-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="666e0-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="666e0-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="666e0-121">-ServiceResource</span></span>
<span data-ttu-id="666e0-122">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="666e0-122">List of service resources</span></span>

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

### <span data-ttu-id="666e0-123">-確認</span><span class="sxs-lookup"><span data-stu-id="666e0-123">-Confirm</span></span>
<span data-ttu-id="666e0-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="666e0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="666e0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666e0-125">-WhatIf</span></span>
<span data-ttu-id="666e0-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="666e0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="666e0-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="666e0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="666e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666e0-128">CommonParameters</span></span>
<span data-ttu-id="666e0-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="666e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666e0-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="666e0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666e0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="666e0-131">INPUTS</span></span>

### <span data-ttu-id="666e0-132">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="666e0-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="666e0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="666e0-133">OUTPUTS</span></span>

### <span data-ttu-id="666e0-134">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="666e0-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="666e0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="666e0-135">NOTES</span></span>

## <span data-ttu-id="666e0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="666e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="666e0-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="666e0-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="666e0-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="666e0-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="666e0-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="666e0-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="666e0-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="666e0-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
