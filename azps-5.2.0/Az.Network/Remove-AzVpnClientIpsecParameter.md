---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278899"
---
# <span data-ttu-id="fc13b-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc13b-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="fc13b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc13b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc13b-103">移除在虛擬網路閘道資源上設定的 Vpn 自訂 ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="fc13b-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="fc13b-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc13b-104">SYNTAX</span></span>

### <span data-ttu-id="fc13b-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fc13b-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc13b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fc13b-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc13b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc13b-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc13b-108">說明</span><span class="sxs-lookup"><span data-stu-id="fc13b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc13b-109">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="fc13b-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="fc13b-110">**AzVpnClientIpsecParameter** Cmdlet 會移除您在虛擬網路閘道上設定的 vpn 自訂 ipsec 參數，然後根據傳遞的 VirtualNetworkGateway 名稱和資源組名稱，在 vpn 閘道上設定預設的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="fc13b-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="fc13b-111">示例</span><span class="sxs-lookup"><span data-stu-id="fc13b-111">EXAMPLES</span></span>

### <span data-ttu-id="fc13b-112">範例1：刪除在虛擬網路閘道設定的 vpn ipsec 參數集</span><span class="sxs-lookup"><span data-stu-id="fc13b-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="fc13b-113">刪除在您的虛擬網路閘道上設定的 vpn 自訂 ipsec 參數，名稱為 "myRG" 中的 [myGateway "。</span><span class="sxs-lookup"><span data-stu-id="fc13b-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="fc13b-114">這個命令會傳回 bool 物件，顯示刪除成功或失敗的情況。</span><span class="sxs-lookup"><span data-stu-id="fc13b-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="fc13b-115">注意：這將會導致在您的虛擬網路閘道設定預設的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="fc13b-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="fc13b-116">參數</span><span class="sxs-lookup"><span data-stu-id="fc13b-116">PARAMETERS</span></span>

### <span data-ttu-id="fc13b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc13b-117">-DefaultProfile</span></span>
<span data-ttu-id="fc13b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc13b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc13b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc13b-119">-InputObject</span></span>
<span data-ttu-id="fc13b-120">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="fc13b-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="fc13b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc13b-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc13b-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc13b-122">The resource group name.</span></span>

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

### <span data-ttu-id="fc13b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc13b-123">-ResourceId</span></span>
<span data-ttu-id="fc13b-124">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc13b-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fc13b-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fc13b-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fc13b-126">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="fc13b-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="fc13b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="fc13b-127">-Confirm</span></span>
<span data-ttu-id="fc13b-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc13b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc13b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc13b-129">-WhatIf</span></span>
<span data-ttu-id="fc13b-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc13b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc13b-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc13b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc13b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc13b-132">CommonParameters</span></span>
<span data-ttu-id="fc13b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc13b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc13b-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc13b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc13b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="fc13b-135">INPUTS</span></span>

### <span data-ttu-id="fc13b-136">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fc13b-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fc13b-137">System.object</span><span class="sxs-lookup"><span data-stu-id="fc13b-137">System.String</span></span>

## <span data-ttu-id="fc13b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fc13b-138">OUTPUTS</span></span>

### <span data-ttu-id="fc13b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fc13b-139">System.Boolean</span></span>

## <span data-ttu-id="fc13b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fc13b-140">NOTES</span></span>

## <span data-ttu-id="fc13b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc13b-141">RELATED LINKS</span></span>

[<span data-ttu-id="fc13b-142">AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc13b-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fc13b-143">新-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc13b-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fc13b-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc13b-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
