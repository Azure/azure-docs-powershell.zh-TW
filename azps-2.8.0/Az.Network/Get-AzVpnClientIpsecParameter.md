---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: d837355891f3b8095da0380fd91a9ac58a74acff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789466"
---
# <span data-ttu-id="215ea-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="215ea-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="215ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="215ea-102">SYNOPSIS</span></span>
<span data-ttu-id="215ea-103">取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="215ea-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="215ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="215ea-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="215ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="215ea-105">DESCRIPTION</span></span>
<span data-ttu-id="215ea-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="215ea-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="215ea-107">**AzVpnClientIpsecParameter** Cmdlet 會根據閘道名稱和資源組名稱，傳回在 Azure 上的閘道上設定的 vpn ipsec 參數物件。</span><span class="sxs-lookup"><span data-stu-id="215ea-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="215ea-108">示例</span><span class="sxs-lookup"><span data-stu-id="215ea-108">EXAMPLES</span></span>

### <span data-ttu-id="215ea-109">1：取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="215ea-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="215ea-110">傳回在資源群組 "myRG" 中，以 "myGateway" 為名稱設定之 vpn ipsec 參數集的物件</span><span class="sxs-lookup"><span data-stu-id="215ea-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="215ea-111">參數</span><span class="sxs-lookup"><span data-stu-id="215ea-111">PARAMETERS</span></span>

### <span data-ttu-id="215ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215ea-112">-DefaultProfile</span></span>
<span data-ttu-id="215ea-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="215ea-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="215ea-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="215ea-114">-Name</span></span>
<span data-ttu-id="215ea-115">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="215ea-115">The resource name.</span></span>

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

### <span data-ttu-id="215ea-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215ea-116">-ResourceGroupName</span></span>
<span data-ttu-id="215ea-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="215ea-117">The resource group name.</span></span>

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

### <span data-ttu-id="215ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215ea-118">CommonParameters</span></span>
<span data-ttu-id="215ea-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="215ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215ea-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="215ea-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215ea-121">輸入</span><span class="sxs-lookup"><span data-stu-id="215ea-121">INPUTS</span></span>

### <span data-ttu-id="215ea-122">System.object</span><span class="sxs-lookup"><span data-stu-id="215ea-122">System.String</span></span>

## <span data-ttu-id="215ea-123">輸出</span><span class="sxs-lookup"><span data-stu-id="215ea-123">OUTPUTS</span></span>

### <span data-ttu-id="215ea-124">PSVpnClientIPsecParameters 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="215ea-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="215ea-125">筆記</span><span class="sxs-lookup"><span data-stu-id="215ea-125">NOTES</span></span>

## <span data-ttu-id="215ea-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="215ea-126">RELATED LINKS</span></span>

[<span data-ttu-id="215ea-127">新-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="215ea-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="215ea-128">移除-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="215ea-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="215ea-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="215ea-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
