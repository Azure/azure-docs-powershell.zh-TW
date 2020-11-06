---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448371"
---
# <span data-ttu-id="6b9a9-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6b9a9-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="6b9a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9a9-103">取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b9a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b9a9-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b9a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="6b9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9a9-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="6b9a9-107">**AzureRmVpnClientIpsecParameter** Cmdlet 會根據閘道名稱和資源組名稱，傳回在 Azure 上的閘道上設定的 vpn ipsec 參數物件。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="6b9a9-108">示例</span><span class="sxs-lookup"><span data-stu-id="6b9a9-108">EXAMPLES</span></span>

### <span data-ttu-id="6b9a9-109">1：取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6b9a9-110">傳回在資源群組 "myRG" 中，以 "myGateway" 為名稱設定之 vpn ipsec 參數集的物件</span><span class="sxs-lookup"><span data-stu-id="6b9a9-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="6b9a9-111">參數</span><span class="sxs-lookup"><span data-stu-id="6b9a9-111">PARAMETERS</span></span>

### <span data-ttu-id="6b9a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9a9-112">-DefaultProfile</span></span>
<span data-ttu-id="6b9a9-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b9a9-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b9a9-114">-Name</span></span>
<span data-ttu-id="6b9a9-115">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-115">The resource name.</span></span>

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

### <span data-ttu-id="6b9a9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9a9-116">-ResourceGroupName</span></span>
<span data-ttu-id="6b9a9-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-117">The resource group name.</span></span>

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

### <span data-ttu-id="6b9a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9a9-118">CommonParameters</span></span>
<span data-ttu-id="6b9a9-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9a9-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b9a9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9a9-121">輸入</span><span class="sxs-lookup"><span data-stu-id="6b9a9-121">INPUTS</span></span>

### <span data-ttu-id="6b9a9-122">System.object</span><span class="sxs-lookup"><span data-stu-id="6b9a9-122">System.String</span></span>

## <span data-ttu-id="6b9a9-123">輸出</span><span class="sxs-lookup"><span data-stu-id="6b9a9-123">OUTPUTS</span></span>

### <span data-ttu-id="6b9a9-124">PSVpnClientIPsecParameters 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6b9a9-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="6b9a9-125">筆記</span><span class="sxs-lookup"><span data-stu-id="6b9a9-125">NOTES</span></span>

## <span data-ttu-id="6b9a9-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b9a9-126">RELATED LINKS</span></span>
