---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 1ff3e4f4a69309d2dfa5655fefac3d1c5a0e933f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798365"
---
# <span data-ttu-id="a644c-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a644c-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="a644c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a644c-102">SYNOPSIS</span></span>
<span data-ttu-id="a644c-103">取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="a644c-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="a644c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a644c-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a644c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a644c-105">DESCRIPTION</span></span>
<span data-ttu-id="a644c-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="a644c-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="a644c-107">**AzVpnClientIpsecParameter** Cmdlet 會根據閘道名稱和資源組名稱，傳回在 Azure 上的閘道上設定的 vpn ipsec 參數物件。</span><span class="sxs-lookup"><span data-stu-id="a644c-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="a644c-108">示例</span><span class="sxs-lookup"><span data-stu-id="a644c-108">EXAMPLES</span></span>

### <span data-ttu-id="a644c-109">1：取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="a644c-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="a644c-110">傳回在資源群組 "myRG" 中，以 "myGateway" 為名稱設定之 vpn ipsec 參數集的物件</span><span class="sxs-lookup"><span data-stu-id="a644c-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="a644c-111">參數</span><span class="sxs-lookup"><span data-stu-id="a644c-111">PARAMETERS</span></span>

### <span data-ttu-id="a644c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a644c-112">-DefaultProfile</span></span>
<span data-ttu-id="a644c-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a644c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a644c-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a644c-114">-Name</span></span>
<span data-ttu-id="a644c-115">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a644c-115">The resource name.</span></span>

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

### <span data-ttu-id="a644c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a644c-116">-ResourceGroupName</span></span>
<span data-ttu-id="a644c-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a644c-117">The resource group name.</span></span>

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

### <span data-ttu-id="a644c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a644c-118">CommonParameters</span></span>
<span data-ttu-id="a644c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a644c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a644c-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a644c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a644c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a644c-121">INPUTS</span></span>

### <span data-ttu-id="a644c-122">System.object</span><span class="sxs-lookup"><span data-stu-id="a644c-122">System.String</span></span>

## <span data-ttu-id="a644c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a644c-123">OUTPUTS</span></span>

### <span data-ttu-id="a644c-124">PSVpnClientIPsecParameters 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a644c-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="a644c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a644c-125">NOTES</span></span>

## <span data-ttu-id="a644c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a644c-126">RELATED LINKS</span></span>

[<span data-ttu-id="a644c-127">新-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a644c-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="a644c-128">移除-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a644c-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="a644c-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a644c-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
