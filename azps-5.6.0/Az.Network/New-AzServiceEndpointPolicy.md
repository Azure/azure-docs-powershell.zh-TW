---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: b5f555a0df848c86dbbc0a04297d45b4132e6972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902370"
---
# <span data-ttu-id="0dfe9-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0dfe9-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="0dfe9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0dfe9-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfe9-103">建立服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="0dfe9-104">語法</span><span class="sxs-lookup"><span data-stu-id="0dfe9-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0dfe9-105">描述</span><span class="sxs-lookup"><span data-stu-id="0dfe9-105">DESCRIPTION</span></span>
<span data-ttu-id="0dfe9-106">**New-AzServiceEndpointPolicy** Cmdlet 會建立服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="0dfe9-107">例子</span><span class="sxs-lookup"><span data-stu-id="0dfe9-107">EXAMPLES</span></span>

### <span data-ttu-id="0dfe9-108">範例 1：建立服務端點策略</span><span class="sxs-lookup"><span data-stu-id="0dfe9-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="0dfe9-109">此命令會建立名為 Policy1 的服務端點策略，其定義由物件定義$serviceEndpointDefinition並儲存在$serviceEndpointPolicy變數中。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="0dfe9-110">參數</span><span class="sxs-lookup"><span data-stu-id="0dfe9-110">PARAMETERS</span></span>

### <span data-ttu-id="0dfe9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfe9-111">-DefaultProfile</span></span>
<span data-ttu-id="0dfe9-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dfe9-113">-強制</span><span class="sxs-lookup"><span data-stu-id="0dfe9-113">-Force</span></span>
<span data-ttu-id="0dfe9-114">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="0dfe9-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfe9-115">-位置</span><span class="sxs-lookup"><span data-stu-id="0dfe9-115">-Location</span></span>
<span data-ttu-id="0dfe9-116">位置。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dfe9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dfe9-117">-Name</span></span>
<span data-ttu-id="0dfe9-118">子網的名稱</span><span class="sxs-lookup"><span data-stu-id="0dfe9-118">The name of the subnet</span></span>

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

### <span data-ttu-id="0dfe9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dfe9-119">-ResourceGroupName</span></span>
<span data-ttu-id="0dfe9-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dfe9-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0dfe9-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="0dfe9-122">服務端點定義清單</span><span class="sxs-lookup"><span data-stu-id="0dfe9-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfe9-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0dfe9-123">-Confirm</span></span>
<span data-ttu-id="0dfe9-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dfe9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dfe9-125">-WhatIf</span></span>
<span data-ttu-id="0dfe9-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dfe9-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dfe9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfe9-128">CommonParameters</span></span>
<span data-ttu-id="0dfe9-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfe9-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0dfe9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfe9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0dfe9-131">INPUTS</span></span>

### <span data-ttu-id="0dfe9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0dfe9-132">System.String</span></span>

## <span data-ttu-id="0dfe9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0dfe9-133">OUTPUTS</span></span>

### <span data-ttu-id="0dfe9-134">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0dfe9-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="0dfe9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0dfe9-135">NOTES</span></span>

## <span data-ttu-id="0dfe9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dfe9-136">RELATED LINKS</span></span>

[<span data-ttu-id="0dfe9-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0dfe9-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="0dfe9-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0dfe9-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="0dfe9-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0dfe9-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
