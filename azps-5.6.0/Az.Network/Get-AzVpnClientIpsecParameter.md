---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3be81626dc48f66fd7aac71c23c2cd9168dab336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916021"
---
# <span data-ttu-id="f5a91-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f5a91-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="f5a91-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5a91-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a91-103">在虛擬網路閘道上設定 vpn Ipsec 參數，以建立指向網站連接。</span><span class="sxs-lookup"><span data-stu-id="f5a91-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="f5a91-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5a91-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5a91-105">描述</span><span class="sxs-lookup"><span data-stu-id="f5a91-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a91-106">虛擬網路閘道是代表 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="f5a91-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f5a91-107">**Get-Az VpnClientIpsecParameter Cmdlet** 會根據閘道名稱和資源組名，在 Azure 閘道上，會返回 vpn ipsec 參數設定的物件。</span><span class="sxs-lookup"><span data-stu-id="f5a91-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="f5a91-108">例子</span><span class="sxs-lookup"><span data-stu-id="f5a91-108">EXAMPLES</span></span>

### <span data-ttu-id="f5a91-109">範例 1：在虛擬網路閘道上設定 vpn Ipsec 參數，以建立指向網站連接。</span><span class="sxs-lookup"><span data-stu-id="f5a91-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="f5a91-110">會返回在虛擬網路閘道上設定 vpn ipsec 參數的物件，名稱為 "myGateway" 位於資源群組 "myRG"</span><span class="sxs-lookup"><span data-stu-id="f5a91-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="f5a91-111">參數</span><span class="sxs-lookup"><span data-stu-id="f5a91-111">PARAMETERS</span></span>

### <span data-ttu-id="f5a91-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a91-112">-DefaultProfile</span></span>
<span data-ttu-id="f5a91-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5a91-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a91-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5a91-114">-Name</span></span>
<span data-ttu-id="f5a91-115">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f5a91-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a91-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a91-116">-ResourceGroupName</span></span>
<span data-ttu-id="f5a91-117">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f5a91-117">The resource group name.</span></span>

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

### <span data-ttu-id="f5a91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a91-118">CommonParameters</span></span>
<span data-ttu-id="f5a91-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5a91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a91-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5a91-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a91-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f5a91-121">INPUTS</span></span>

### <span data-ttu-id="f5a91-122">System.String</span><span class="sxs-lookup"><span data-stu-id="f5a91-122">System.String</span></span>

## <span data-ttu-id="f5a91-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f5a91-123">OUTPUTS</span></span>

### <span data-ttu-id="f5a91-124">Microsoft.Azure.Commands.Network.models.PS VpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="f5a91-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="f5a91-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f5a91-125">NOTES</span></span>

## <span data-ttu-id="f5a91-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5a91-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5a91-127">New-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f5a91-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="f5a91-128">Remove-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f5a91-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="f5a91-129">Set-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f5a91-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
