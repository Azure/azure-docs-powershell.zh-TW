---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126992"
---
# <span data-ttu-id="e1705-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1705-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e1705-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1705-102">SYNOPSIS</span></span>
<span data-ttu-id="e1705-103">取得服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="e1705-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="e1705-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1705-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1705-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1705-105">DESCRIPTION</span></span>
<span data-ttu-id="e1705-106">**AzServiceEndpointPolicyDefinition** Cmdlet 會取得服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="e1705-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="e1705-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1705-107">EXAMPLES</span></span>

### <span data-ttu-id="e1705-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e1705-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="e1705-109">這個命令會在 ServiceEndpointPolicy 中取得名為 ServiceEndpointPolicyDefinition1 的服務端點原則定義，$Policy 將其儲存在 $policydef 變數中。</span><span class="sxs-lookup"><span data-stu-id="e1705-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="e1705-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1705-110">PARAMETERS</span></span>

### <span data-ttu-id="e1705-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1705-111">-DefaultProfile</span></span>
<span data-ttu-id="e1705-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1705-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1705-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1705-113">-Name</span></span>
<span data-ttu-id="e1705-114">服務端點原則定義的名稱</span><span class="sxs-lookup"><span data-stu-id="e1705-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="e1705-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e1705-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e1705-116">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="e1705-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="e1705-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e1705-117">-Confirm</span></span>
<span data-ttu-id="e1705-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1705-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1705-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1705-119">-WhatIf</span></span>
<span data-ttu-id="e1705-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1705-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1705-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1705-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1705-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1705-122">CommonParameters</span></span>
<span data-ttu-id="e1705-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1705-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1705-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1705-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1705-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e1705-125">INPUTS</span></span>

### <span data-ttu-id="e1705-126">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e1705-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e1705-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e1705-127">OUTPUTS</span></span>

### <span data-ttu-id="e1705-128">PSServiceEndpointPolicyDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e1705-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e1705-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e1705-129">NOTES</span></span>

## <span data-ttu-id="e1705-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1705-130">RELATED LINKS</span></span>

[<span data-ttu-id="e1705-131">附加 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1705-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e1705-132">新-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1705-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e1705-133">移除-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1705-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e1705-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1705-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)