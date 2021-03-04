---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 430ea183d618779045aaf5d13554edac2ce98626
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913410"
---
# <span data-ttu-id="8491b-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8491b-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="8491b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8491b-102">SYNOPSIS</span></span>
<span data-ttu-id="8491b-103">移除 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="8491b-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="8491b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8491b-104">SYNTAX</span></span>

### <span data-ttu-id="8491b-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8491b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8491b-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8491b-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8491b-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8491b-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8491b-108">描述</span><span class="sxs-lookup"><span data-stu-id="8491b-108">DESCRIPTION</span></span>
<span data-ttu-id="8491b-109">移除 Nat 閘道資源</span><span class="sxs-lookup"><span data-stu-id="8491b-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="8491b-110">例子</span><span class="sxs-lookup"><span data-stu-id="8491b-110">EXAMPLES</span></span>

### <span data-ttu-id="8491b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8491b-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="8491b-112">參數</span><span class="sxs-lookup"><span data-stu-id="8491b-112">PARAMETERS</span></span>

### <span data-ttu-id="8491b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8491b-113">-AsJob</span></span>
<span data-ttu-id="8491b-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8491b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8491b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8491b-115">-DefaultProfile</span></span>
<span data-ttu-id="8491b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8491b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8491b-117">-強制</span><span class="sxs-lookup"><span data-stu-id="8491b-117">-Force</span></span>
<span data-ttu-id="8491b-118">如果您要刪除資源，請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="8491b-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="8491b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8491b-119">-InputObject</span></span>
<span data-ttu-id="8491b-120">指定 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="8491b-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8491b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8491b-121">-Name</span></span>
<span data-ttu-id="8491b-122">Nat 閘道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8491b-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8491b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8491b-123">-PassThru</span></span>
<span data-ttu-id="8491b-124">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8491b-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8491b-125">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8491b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8491b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8491b-126">-ResourceGroupName</span></span>
<span data-ttu-id="8491b-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8491b-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8491b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8491b-128">-ResourceId</span></span>
<span data-ttu-id="8491b-129">與 Nat 閘道相關聯的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8491b-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8491b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8491b-130">-Confirm</span></span>
<span data-ttu-id="8491b-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8491b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8491b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8491b-132">-WhatIf</span></span>
<span data-ttu-id="8491b-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8491b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8491b-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8491b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8491b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8491b-135">CommonParameters</span></span>
<span data-ttu-id="8491b-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8491b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8491b-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8491b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8491b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8491b-138">INPUTS</span></span>

### <span data-ttu-id="8491b-139">Microsoft.Azure.Commands.Network.models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="8491b-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="8491b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8491b-140">System.String</span></span>

## <span data-ttu-id="8491b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8491b-141">OUTPUTS</span></span>

### <span data-ttu-id="8491b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8491b-142">System.Boolean</span></span>

## <span data-ttu-id="8491b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8491b-143">NOTES</span></span>

## <span data-ttu-id="8491b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8491b-144">RELATED LINKS</span></span>
