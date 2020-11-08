---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127450"
---
# <span data-ttu-id="f1c26-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1c26-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f1c26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1c26-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c26-103">更新服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="f1c26-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="f1c26-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1c26-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1c26-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1c26-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c26-106">**AzServiceEndpointPolicyDefinition** Cmdlet 會建立服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="f1c26-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="f1c26-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1c26-107">EXAMPLES</span></span>

### <span data-ttu-id="f1c26-108">範例1：更新服務端點原則中的服務端點原則定義</span><span class="sxs-lookup"><span data-stu-id="f1c26-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="f1c26-109">這個命令會更新 $ServiceEndpointPolicy 物件定義之服務端點原則中名為 Policydef1 的服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="f1c26-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="f1c26-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1c26-110">PARAMETERS</span></span>

### <span data-ttu-id="f1c26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c26-111">-DefaultProfile</span></span>
<span data-ttu-id="f1c26-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1c26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c26-113">-描述</span><span class="sxs-lookup"><span data-stu-id="f1c26-113">-Description</span></span>
<span data-ttu-id="f1c26-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="f1c26-114">The description of the definition</span></span>

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

### <span data-ttu-id="f1c26-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1c26-115">-Name</span></span>
<span data-ttu-id="f1c26-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="f1c26-116">The name of the rule</span></span>

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

### <span data-ttu-id="f1c26-117">-服務</span><span class="sxs-lookup"><span data-stu-id="f1c26-117">-Service</span></span>
<span data-ttu-id="f1c26-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="f1c26-118">Name of the service</span></span>

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

### <span data-ttu-id="f1c26-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f1c26-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f1c26-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f1c26-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="f1c26-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="f1c26-121">-ServiceResource</span></span>
<span data-ttu-id="f1c26-122">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="f1c26-122">List of service resources</span></span>

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

### <span data-ttu-id="f1c26-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f1c26-123">-Confirm</span></span>
<span data-ttu-id="f1c26-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1c26-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c26-125">-WhatIf</span></span>
<span data-ttu-id="f1c26-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1c26-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1c26-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1c26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c26-128">CommonParameters</span></span>
<span data-ttu-id="f1c26-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1c26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c26-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1c26-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c26-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f1c26-131">INPUTS</span></span>

### <span data-ttu-id="f1c26-132">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f1c26-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f1c26-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f1c26-133">OUTPUTS</span></span>

### <span data-ttu-id="f1c26-134">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f1c26-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f1c26-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f1c26-135">NOTES</span></span>

## <span data-ttu-id="f1c26-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1c26-136">RELATED LINKS</span></span>

[<span data-ttu-id="f1c26-137">附加 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1c26-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f1c26-138">AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1c26-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f1c26-139">新-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1c26-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f1c26-140">移除-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1c26-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
