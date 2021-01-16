---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276395"
---
# <span data-ttu-id="75a8c-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="75a8c-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="75a8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="75a8c-103">移除 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="75a8c-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="75a8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="75a8c-104">SYNTAX</span></span>

### <span data-ttu-id="75a8c-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="75a8c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a8c-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a8c-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a8c-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a8c-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a8c-108">說明</span><span class="sxs-lookup"><span data-stu-id="75a8c-108">DESCRIPTION</span></span>
<span data-ttu-id="75a8c-109">移除 Nat 閘道資源</span><span class="sxs-lookup"><span data-stu-id="75a8c-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="75a8c-110">示例</span><span class="sxs-lookup"><span data-stu-id="75a8c-110">EXAMPLES</span></span>

### <span data-ttu-id="75a8c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="75a8c-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="75a8c-112">參數</span><span class="sxs-lookup"><span data-stu-id="75a8c-112">PARAMETERS</span></span>

### <span data-ttu-id="75a8c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75a8c-113">-AsJob</span></span>
<span data-ttu-id="75a8c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75a8c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75a8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a8c-115">-DefaultProfile</span></span>
<span data-ttu-id="75a8c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75a8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a8c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="75a8c-117">-Force</span></span>
<span data-ttu-id="75a8c-118">如果您想要刪除資源，請不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="75a8c-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="75a8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75a8c-119">-InputObject</span></span>
<span data-ttu-id="75a8c-120">指定 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="75a8c-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="75a8c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="75a8c-121">-Name</span></span>
<span data-ttu-id="75a8c-122">Nat 閘道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a8c-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="75a8c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75a8c-123">-PassThru</span></span>
<span data-ttu-id="75a8c-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="75a8c-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="75a8c-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="75a8c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75a8c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a8c-126">-ResourceGroupName</span></span>
<span data-ttu-id="75a8c-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a8c-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="75a8c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75a8c-128">-ResourceId</span></span>
<span data-ttu-id="75a8c-129">與 Nat 閘道相關聯的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="75a8c-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="75a8c-130">-確認</span><span class="sxs-lookup"><span data-stu-id="75a8c-130">-Confirm</span></span>
<span data-ttu-id="75a8c-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75a8c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75a8c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a8c-132">-WhatIf</span></span>
<span data-ttu-id="75a8c-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75a8c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a8c-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75a8c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75a8c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a8c-135">CommonParameters</span></span>
<span data-ttu-id="75a8c-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75a8c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a8c-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75a8c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a8c-138">輸入</span><span class="sxs-lookup"><span data-stu-id="75a8c-138">INPUTS</span></span>

### <span data-ttu-id="75a8c-139">PSNatGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="75a8c-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="75a8c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="75a8c-140">System.String</span></span>

## <span data-ttu-id="75a8c-141">輸出</span><span class="sxs-lookup"><span data-stu-id="75a8c-141">OUTPUTS</span></span>

### <span data-ttu-id="75a8c-142">System.object</span><span class="sxs-lookup"><span data-stu-id="75a8c-142">System.Boolean</span></span>

## <span data-ttu-id="75a8c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="75a8c-143">NOTES</span></span>

## <span data-ttu-id="75a8c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="75a8c-144">RELATED LINKS</span></span>
