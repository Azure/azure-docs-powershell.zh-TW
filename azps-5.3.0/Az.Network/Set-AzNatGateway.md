---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448906"
---
# <span data-ttu-id="dcec8-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dcec8-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="dcec8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcec8-102">SYNOPSIS</span></span>
<span data-ttu-id="dcec8-103">使用 [公用 Ip 位址]、[公用 Ip 首碼] 和 [IdleTimeoutInMinutes] 來更新 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="dcec8-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="dcec8-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcec8-104">SYNTAX</span></span>

### <span data-ttu-id="dcec8-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dcec8-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcec8-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcec8-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcec8-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcec8-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcec8-108">說明</span><span class="sxs-lookup"><span data-stu-id="dcec8-108">DESCRIPTION</span></span>
<span data-ttu-id="dcec8-109">使用 [公用 Ip 位址]、[公用 Ip 首碼] 和 [IdleTimeoutInMinutes] 來更新 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="dcec8-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="dcec8-110">示例</span><span class="sxs-lookup"><span data-stu-id="dcec8-110">EXAMPLES</span></span>

### <span data-ttu-id="dcec8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dcec8-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="dcec8-112">參數</span><span class="sxs-lookup"><span data-stu-id="dcec8-112">PARAMETERS</span></span>

### <span data-ttu-id="dcec8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcec8-113">-AsJob</span></span>
<span data-ttu-id="dcec8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dcec8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcec8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcec8-115">-DefaultProfile</span></span>
<span data-ttu-id="dcec8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcec8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcec8-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dcec8-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="dcec8-118">Nat 閘道的空閒超時。</span><span class="sxs-lookup"><span data-stu-id="dcec8-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcec8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcec8-119">-InputObject</span></span>
<span data-ttu-id="dcec8-120">指定 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="dcec8-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dcec8-121">-Name</span></span>
<span data-ttu-id="dcec8-122">Nat 閘道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcec8-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcec8-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dcec8-123">-PublicIpAddress</span></span>
<span data-ttu-id="dcec8-124">與 nat 閘道資源相關聯之公用 ip 位址的陣列。</span><span class="sxs-lookup"><span data-stu-id="dcec8-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcec8-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="dcec8-125">-PublicIpPrefix</span></span>
<span data-ttu-id="dcec8-126">與 nat 閘道資源相關聯之公用 ip 首碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="dcec8-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcec8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcec8-127">-ResourceGroupName</span></span>
<span data-ttu-id="dcec8-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcec8-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcec8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcec8-129">-ResourceId</span></span>
<span data-ttu-id="dcec8-130">指定 Nat 閘道資源的 Id。</span><span class="sxs-lookup"><span data-stu-id="dcec8-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="dcec8-131">-Confirm</span></span>
<span data-ttu-id="dcec8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcec8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcec8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcec8-133">-WhatIf</span></span>
<span data-ttu-id="dcec8-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcec8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcec8-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcec8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcec8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcec8-136">CommonParameters</span></span>
<span data-ttu-id="dcec8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcec8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcec8-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dcec8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcec8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="dcec8-139">INPUTS</span></span>

### <span data-ttu-id="dcec8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="dcec8-140">System.String</span></span>

### <span data-ttu-id="dcec8-141">PSNatGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dcec8-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="dcec8-142">輸出</span><span class="sxs-lookup"><span data-stu-id="dcec8-142">OUTPUTS</span></span>

### <span data-ttu-id="dcec8-143">PSNatGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dcec8-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="dcec8-144">筆記</span><span class="sxs-lookup"><span data-stu-id="dcec8-144">NOTES</span></span>

## <span data-ttu-id="dcec8-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcec8-145">RELATED LINKS</span></span>
