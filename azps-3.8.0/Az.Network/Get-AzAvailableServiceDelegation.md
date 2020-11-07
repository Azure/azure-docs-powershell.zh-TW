---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797073"
---
# <span data-ttu-id="f63ac-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="f63ac-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="f63ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f63ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f63ac-103">在區域中取得可用的服務委派。</span><span class="sxs-lookup"><span data-stu-id="f63ac-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="f63ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="f63ac-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f63ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="f63ac-105">DESCRIPTION</span></span>
<span data-ttu-id="f63ac-106">**AzAvailableServiceDelegation** Cmdlet 可讓您在提供的位置中，取得子網的所有可用服務委派。</span><span class="sxs-lookup"><span data-stu-id="f63ac-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="f63ac-107">這個 Cmdlet 不 *說明哪個* 委派可以在單一子網上並存。</span><span class="sxs-lookup"><span data-stu-id="f63ac-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="f63ac-108">示例</span><span class="sxs-lookup"><span data-stu-id="f63ac-108">EXAMPLES</span></span>

### <span data-ttu-id="f63ac-109">1：取得所有可用的服務委派</span><span class="sxs-lookup"><span data-stu-id="f63ac-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="f63ac-110">參數</span><span class="sxs-lookup"><span data-stu-id="f63ac-110">PARAMETERS</span></span>

### <span data-ttu-id="f63ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63ac-111">-DefaultProfile</span></span>
<span data-ttu-id="f63ac-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f63ac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f63ac-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f63ac-113">-Location</span></span>
<span data-ttu-id="f63ac-114">位置。</span><span class="sxs-lookup"><span data-stu-id="f63ac-114">The location.</span></span>

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

### <span data-ttu-id="f63ac-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63ac-115">CommonParameters</span></span>
<span data-ttu-id="f63ac-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f63ac-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63ac-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f63ac-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63ac-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f63ac-118">INPUTS</span></span>

### <span data-ttu-id="f63ac-119">System.object</span><span class="sxs-lookup"><span data-stu-id="f63ac-119">System.String</span></span>

## <span data-ttu-id="f63ac-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f63ac-120">OUTPUTS</span></span>

### <span data-ttu-id="f63ac-121">PSAvailableDelegation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f63ac-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="f63ac-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f63ac-122">NOTES</span></span>

## <span data-ttu-id="f63ac-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="f63ac-123">RELATED LINKS</span></span>

<span data-ttu-id="f63ac-124">[附加 AzDelegation](./Add-AzDelegation.md) 
[新-AzDelegation](./New-AzDelegation.md) 
[移除-AzDelegation](./Remove-AzDelegation.md) 
[AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="f63ac-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>