---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 5c91ba0dbca881e7e6a6909ef1b7200adf2ba1ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911626"
---
# <span data-ttu-id="9e471-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="9e471-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="9e471-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9e471-102">SYNOPSIS</span></span>
<span data-ttu-id="9e471-103">移除與 VpnGateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="9e471-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="9e471-104">語法</span><span class="sxs-lookup"><span data-stu-id="9e471-104">SYNTAX</span></span>

### <span data-ttu-id="9e471-105">By VpnGatewayNatRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="9e471-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e471-106">By VpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="9e471-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e471-107">By VpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="9e471-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e471-108">描述</span><span class="sxs-lookup"><span data-stu-id="9e471-108">DESCRIPTION</span></span>
<span data-ttu-id="9e471-109">移除與 VpnGateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="9e471-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="9e471-110">例子</span><span class="sxs-lookup"><span data-stu-id="9e471-110">EXAMPLES</span></span>

### <span data-ttu-id="9e471-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9e471-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="9e471-112">上述將建立與 VpnGateway 相關聯的資源群組、虛擬 WAN、虛擬網路、虛擬中樞、VpnGateway 和 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="9e471-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="9e471-113">然後，它會使用 NAT 規則名稱移除 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="9e471-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="9e471-114">參數</span><span class="sxs-lookup"><span data-stu-id="9e471-114">PARAMETERS</span></span>

### <span data-ttu-id="9e471-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e471-115">-DefaultProfile</span></span>
<span data-ttu-id="9e471-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e471-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e471-117">-強制</span><span class="sxs-lookup"><span data-stu-id="9e471-117">-Force</span></span>
<span data-ttu-id="9e471-118">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="9e471-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="9e471-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e471-119">-InputObject</span></span>
<span data-ttu-id="9e471-120">要更新的 VpnGatewayNatRule 物件。</span><span class="sxs-lookup"><span data-stu-id="9e471-120">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e471-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e471-121">-Name</span></span>
<span data-ttu-id="9e471-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9e471-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e471-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9e471-123">-ParentResourceName</span></span>
<span data-ttu-id="9e471-124">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9e471-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e471-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e471-125">-PassThru</span></span>
<span data-ttu-id="9e471-126">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9e471-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="9e471-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e471-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e471-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9e471-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e471-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e471-129">-ResourceId</span></span>
<span data-ttu-id="9e471-130">要刪除的 VpnGatewayNatRule 物件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e471-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e471-131">-確認</span><span class="sxs-lookup"><span data-stu-id="9e471-131">-Confirm</span></span>
<span data-ttu-id="9e471-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9e471-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e471-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e471-133">-WhatIf</span></span>
<span data-ttu-id="9e471-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e471-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e471-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e471-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e471-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e471-136">CommonParameters</span></span>
<span data-ttu-id="9e471-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9e471-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e471-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e471-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e471-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9e471-139">INPUTS</span></span>

### <span data-ttu-id="9e471-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9e471-140">System.String</span></span>

### <span data-ttu-id="9e471-141">Microsoft.Azure.Commands.Network.models.PS VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="9e471-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="9e471-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9e471-142">OUTPUTS</span></span>

### <span data-ttu-id="9e471-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e471-143">System.Boolean</span></span>

## <span data-ttu-id="9e471-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9e471-144">NOTES</span></span>

## <span data-ttu-id="9e471-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e471-145">RELATED LINKS</span></span>
