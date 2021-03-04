---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: e0c8b550b6d9571c3dd55552bab101441085f3ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915298"
---
# <span data-ttu-id="f94f5-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f94f5-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="f94f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f94f5-102">SYNOPSIS</span></span>
<span data-ttu-id="f94f5-103">使用公用 Ip 位址、公用 Ip 首碼和 IdleTimeoutInMinutes 更新 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="f94f5-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="f94f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="f94f5-104">SYNTAX</span></span>

### <span data-ttu-id="f94f5-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f94f5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f94f5-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f94f5-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f94f5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f94f5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f94f5-108">描述</span><span class="sxs-lookup"><span data-stu-id="f94f5-108">DESCRIPTION</span></span>
<span data-ttu-id="f94f5-109">使用公用 Ip 位址、公用 Ip 首碼和 IdleTimeoutInMinutes 更新 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="f94f5-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="f94f5-110">例子</span><span class="sxs-lookup"><span data-stu-id="f94f5-110">EXAMPLES</span></span>

### <span data-ttu-id="f94f5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f94f5-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="f94f5-112">參數</span><span class="sxs-lookup"><span data-stu-id="f94f5-112">PARAMETERS</span></span>

### <span data-ttu-id="f94f5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f94f5-113">-AsJob</span></span>
<span data-ttu-id="f94f5-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f94f5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f94f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94f5-115">-DefaultProfile</span></span>
<span data-ttu-id="f94f5-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f94f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f94f5-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f94f5-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f94f5-118">nat 閘道的閒置超時。</span><span class="sxs-lookup"><span data-stu-id="f94f5-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="f94f5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f94f5-119">-InputObject</span></span>
<span data-ttu-id="f94f5-120">指定 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="f94f5-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="f94f5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f94f5-121">-Name</span></span>
<span data-ttu-id="f94f5-122">Nat 閘道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f94f5-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="f94f5-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f94f5-123">-PublicIpAddress</span></span>
<span data-ttu-id="f94f5-124">與 nat 閘道資源相關聯的公用 ip 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="f94f5-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="f94f5-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f94f5-125">-PublicIpPrefix</span></span>
<span data-ttu-id="f94f5-126">與 nat 閘道資源相關聯的公用 ip 首碼陣列。</span><span class="sxs-lookup"><span data-stu-id="f94f5-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="f94f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="f94f5-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f94f5-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="f94f5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f94f5-129">-ResourceId</span></span>
<span data-ttu-id="f94f5-130">指定 Nat 閘道資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f94f5-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="f94f5-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f94f5-131">-Confirm</span></span>
<span data-ttu-id="f94f5-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f94f5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f94f5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f94f5-133">-WhatIf</span></span>
<span data-ttu-id="f94f5-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f94f5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f94f5-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f94f5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f94f5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94f5-136">CommonParameters</span></span>
<span data-ttu-id="f94f5-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f94f5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94f5-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f94f5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94f5-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f94f5-139">INPUTS</span></span>

### <span data-ttu-id="f94f5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f94f5-140">System.String</span></span>

### <span data-ttu-id="f94f5-141">Microsoft.Azure.Commands.Network.models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="f94f5-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="f94f5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f94f5-142">OUTPUTS</span></span>

### <span data-ttu-id="f94f5-143">Microsoft.Azure.Commands.Network.models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="f94f5-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="f94f5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f94f5-144">NOTES</span></span>

## <span data-ttu-id="f94f5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f94f5-145">RELATED LINKS</span></span>
