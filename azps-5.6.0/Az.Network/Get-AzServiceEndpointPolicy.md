---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: eac0d67e2c9ffc77d9387eeb599ad624ac01fbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916025"
---
# <span data-ttu-id="138e0-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="138e0-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="138e0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="138e0-102">SYNOPSIS</span></span>
<span data-ttu-id="138e0-103">獲得服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="138e0-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="138e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="138e0-104">SYNTAX</span></span>

### <span data-ttu-id="138e0-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="138e0-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="138e0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="138e0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="138e0-107">描述</span><span class="sxs-lookup"><span data-stu-id="138e0-107">DESCRIPTION</span></span>
<span data-ttu-id="138e0-108">**Get-AzServiceEndPointPolicy** Cmdlet 會取得服務端點策略。</span><span class="sxs-lookup"><span data-stu-id="138e0-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="138e0-109">例子</span><span class="sxs-lookup"><span data-stu-id="138e0-109">EXAMPLES</span></span>

### <span data-ttu-id="138e0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="138e0-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="138e0-111">此命令會獲得名為 ServiceEndpointPolicy1 的服務端點策略，該策略屬於名為 ResourceGroup01 的資源群組，並儲存在 $policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="138e0-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="138e0-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="138e0-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="138e0-113">此命令會獲得名為 ResourceGroup01 的資源群組中所有服務端點$policyList清單。</span><span class="sxs-lookup"><span data-stu-id="138e0-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="138e0-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="138e0-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="138e0-115">此命令會獲得以「ServiceEndpointPolicy」為起始之所有服務端點策略的清單。</span><span class="sxs-lookup"><span data-stu-id="138e0-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="138e0-116">參數</span><span class="sxs-lookup"><span data-stu-id="138e0-116">PARAMETERS</span></span>

### <span data-ttu-id="138e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138e0-117">-DefaultProfile</span></span>
<span data-ttu-id="138e0-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="138e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="138e0-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="138e0-119">-Name</span></span>
<span data-ttu-id="138e0-120">服務端點策略的名稱</span><span class="sxs-lookup"><span data-stu-id="138e0-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="138e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="138e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="138e0-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="138e0-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="138e0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="138e0-123">-ResourceId</span></span>
<span data-ttu-id="138e0-124">服務端點策略的識別碼。</span><span class="sxs-lookup"><span data-stu-id="138e0-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138e0-125">-確認</span><span class="sxs-lookup"><span data-stu-id="138e0-125">-Confirm</span></span>
<span data-ttu-id="138e0-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="138e0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="138e0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="138e0-127">-WhatIf</span></span>
<span data-ttu-id="138e0-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="138e0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="138e0-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="138e0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="138e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138e0-130">CommonParameters</span></span>
<span data-ttu-id="138e0-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="138e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138e0-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="138e0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138e0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="138e0-133">INPUTS</span></span>

### <span data-ttu-id="138e0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="138e0-134">System.String</span></span>

## <span data-ttu-id="138e0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="138e0-135">OUTPUTS</span></span>

### <span data-ttu-id="138e0-136">Microsoft.Azure.Commands.Network.models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="138e0-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="138e0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="138e0-137">NOTES</span></span>

## <span data-ttu-id="138e0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="138e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="138e0-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="138e0-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="138e0-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="138e0-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="138e0-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="138e0-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
