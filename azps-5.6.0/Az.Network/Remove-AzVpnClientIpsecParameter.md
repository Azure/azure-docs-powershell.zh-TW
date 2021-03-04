---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 513fbe1d973a75dbc1c967610d95882202bab147
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903990"
---
# <span data-ttu-id="d8dd9-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8dd9-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="d8dd9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dd9-103">移除虛擬網路閘道資源上的 Vpn 自訂 ipsec 策略集。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="d8dd9-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8dd9-104">SYNTAX</span></span>

### <span data-ttu-id="d8dd9-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d8dd9-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d8dd9-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dd9-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8dd9-108">描述</span><span class="sxs-lookup"><span data-stu-id="d8dd9-108">DESCRIPTION</span></span>
<span data-ttu-id="d8dd9-109">虛擬網路閘道是代表 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d8dd9-110">**Remove-Az VpnClientIpsecParameter** Cmdlet 會移除虛擬網路閘道上所設定 vpn 自訂 ipsec 參數，進而根據傳遞的 VirtualNetworkGateway 名稱和資源組名，在 VPN 閘道上設定預設 vpn ipsec 策略。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="d8dd9-111">例子</span><span class="sxs-lookup"><span data-stu-id="d8dd9-111">EXAMPLES</span></span>

### <span data-ttu-id="d8dd9-112">範例 1：刪除虛擬網路閘道上所設定 vpn ipsec 參數</span><span class="sxs-lookup"><span data-stu-id="d8dd9-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="d8dd9-113">刪除在虛擬網路閘道上設定、名稱為"myGateway"的資源群組"myRG"中的 vpn 自訂 ipsec 參數。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="d8dd9-114">此命令會返回布林值物件，顯示移除是否成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="d8dd9-115">注意：這將會導致在虛擬網路閘道上設定預設的 vpn ipsec 策略。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="d8dd9-116">參數</span><span class="sxs-lookup"><span data-stu-id="d8dd9-116">PARAMETERS</span></span>

### <span data-ttu-id="d8dd9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dd9-117">-DefaultProfile</span></span>
<span data-ttu-id="d8dd9-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dd9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8dd9-119">-InputObject</span></span>
<span data-ttu-id="d8dd9-120">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="d8dd9-120">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dd9-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8dd9-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dd9-123">-ResourceId</span></span>
<span data-ttu-id="d8dd9-124">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd9-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d8dd9-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d8dd9-126">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d8dd9-127">-Confirm</span></span>
<span data-ttu-id="d8dd9-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8dd9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8dd9-129">-WhatIf</span></span>
<span data-ttu-id="d8dd9-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8dd9-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8dd9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dd9-132">CommonParameters</span></span>
<span data-ttu-id="d8dd9-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dd9-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d8dd9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dd9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d8dd9-135">INPUTS</span></span>

### <span data-ttu-id="d8dd9-136">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8dd9-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d8dd9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d8dd9-137">System.String</span></span>

## <span data-ttu-id="d8dd9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d8dd9-138">OUTPUTS</span></span>

### <span data-ttu-id="d8dd9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8dd9-139">System.Boolean</span></span>

## <span data-ttu-id="d8dd9-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d8dd9-140">NOTES</span></span>

## <span data-ttu-id="d8dd9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8dd9-141">RELATED LINKS</span></span>

[<span data-ttu-id="d8dd9-142">Get-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8dd9-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="d8dd9-143">New-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8dd9-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="d8dd9-144">Set-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8dd9-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
