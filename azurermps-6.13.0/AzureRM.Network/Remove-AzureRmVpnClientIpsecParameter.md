---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448305"
---
# <span data-ttu-id="3b071-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3b071-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="3b071-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b071-102">SYNOPSIS</span></span>
<span data-ttu-id="3b071-103">移除在虛擬網路閘道資源上設定的 Vpn 自訂 ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="3b071-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b071-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b071-104">SYNTAX</span></span>

### <span data-ttu-id="3b071-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="3b071-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b071-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3b071-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b071-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b071-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b071-108">說明</span><span class="sxs-lookup"><span data-stu-id="3b071-108">DESCRIPTION</span></span>
<span data-ttu-id="3b071-109">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="3b071-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="3b071-110">**AzureRmVpnClientIpsecParameter** Cmdlet 會移除您在虛擬網路閘道上設定的 vpn 自訂 ipsec 參數，然後根據傳遞的 VirtualNetworkGateway 名稱和資源組名稱，在 vpn 閘道上設定預設的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="3b071-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="3b071-111">示例</span><span class="sxs-lookup"><span data-stu-id="3b071-111">EXAMPLES</span></span>

### <span data-ttu-id="3b071-112">1：刪除虛擬網路閘道上設定的 vpn ipsec 參數</span><span class="sxs-lookup"><span data-stu-id="3b071-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="3b071-113">刪除在您的虛擬網路閘道上設定的 vpn 自訂 ipsec 參數，名稱為 "myRG" 中的 [myGateway "。</span><span class="sxs-lookup"><span data-stu-id="3b071-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="3b071-114">這個命令會傳回 bool 物件，顯示刪除成功或失敗的情況。</span><span class="sxs-lookup"><span data-stu-id="3b071-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="3b071-115">注意：這將會導致在您的虛擬網路閘道設定預設的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="3b071-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="3b071-116">參數</span><span class="sxs-lookup"><span data-stu-id="3b071-116">PARAMETERS</span></span>

### <span data-ttu-id="3b071-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b071-117">-DefaultProfile</span></span>
<span data-ttu-id="3b071-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b071-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b071-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b071-119">-InputObject</span></span>
<span data-ttu-id="3b071-120">虛擬網路 gateaway 物件</span><span class="sxs-lookup"><span data-stu-id="3b071-120">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="3b071-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b071-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b071-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b071-122">The resource group name.</span></span>

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

### <span data-ttu-id="3b071-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b071-123">-ResourceId</span></span>
<span data-ttu-id="3b071-124">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b071-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3b071-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3b071-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3b071-126">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="3b071-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="3b071-127">-確認</span><span class="sxs-lookup"><span data-stu-id="3b071-127">-Confirm</span></span>
<span data-ttu-id="3b071-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3b071-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b071-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b071-129">-WhatIf</span></span>
<span data-ttu-id="3b071-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b071-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b071-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b071-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b071-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b071-132">CommonParameters</span></span>
<span data-ttu-id="3b071-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b071-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b071-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b071-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b071-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3b071-135">INPUTS</span></span>

### <span data-ttu-id="3b071-136">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3b071-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3b071-137">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3b071-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3b071-138">System.object</span><span class="sxs-lookup"><span data-stu-id="3b071-138">System.String</span></span>

## <span data-ttu-id="3b071-139">輸出</span><span class="sxs-lookup"><span data-stu-id="3b071-139">OUTPUTS</span></span>

### <span data-ttu-id="3b071-140">System.object</span><span class="sxs-lookup"><span data-stu-id="3b071-140">System.Boolean</span></span>

## <span data-ttu-id="3b071-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3b071-141">NOTES</span></span>

## <span data-ttu-id="3b071-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b071-142">RELATED LINKS</span></span>
