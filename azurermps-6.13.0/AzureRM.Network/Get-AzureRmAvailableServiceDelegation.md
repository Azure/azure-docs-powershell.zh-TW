---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624890"
---
# <span data-ttu-id="9f350-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="9f350-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="9f350-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f350-102">SYNOPSIS</span></span>
<span data-ttu-id="9f350-103">在區域中取得可用的服務委派。</span><span class="sxs-lookup"><span data-stu-id="9f350-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f350-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f350-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f350-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f350-105">DESCRIPTION</span></span>
<span data-ttu-id="9f350-106">**AzureRmAvailableServiceDelegation** Cmdlet 可讓您在提供的位置中，取得子網的所有可用服務委派。</span><span class="sxs-lookup"><span data-stu-id="9f350-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="9f350-107">這個 Cmdlet 不 *說明哪個* 委派可以在單一子網上並存。</span><span class="sxs-lookup"><span data-stu-id="9f350-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="9f350-108">示例</span><span class="sxs-lookup"><span data-stu-id="9f350-108">EXAMPLES</span></span>

### <span data-ttu-id="9f350-109">1：取得所有可用的服務委派</span><span class="sxs-lookup"><span data-stu-id="9f350-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="9f350-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f350-110">PARAMETERS</span></span>

### <span data-ttu-id="9f350-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f350-111">-DefaultProfile</span></span>
<span data-ttu-id="9f350-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f350-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f350-113">-位置</span><span class="sxs-lookup"><span data-stu-id="9f350-113">-Location</span></span>
<span data-ttu-id="9f350-114">位置。</span><span class="sxs-lookup"><span data-stu-id="9f350-114">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f350-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f350-115">CommonParameters</span></span>
<span data-ttu-id="9f350-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f350-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9f350-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f350-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f350-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9f350-118">INPUTS</span></span>

### <span data-ttu-id="9f350-119">System.object</span><span class="sxs-lookup"><span data-stu-id="9f350-119">System.String</span></span>

## <span data-ttu-id="9f350-120">輸出</span><span class="sxs-lookup"><span data-stu-id="9f350-120">OUTPUTS</span></span>

### <span data-ttu-id="9f350-121">PSAvailableDelegation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9f350-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="9f350-122">筆記</span><span class="sxs-lookup"><span data-stu-id="9f350-122">NOTES</span></span>

## <span data-ttu-id="9f350-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f350-123">RELATED LINKS</span></span>
<span data-ttu-id="9f350-124">[附加 AzureRmDelegation](./Add-AzureRmDelegation.md) 
[新-AzureRmDelegation](./New-AzureRmDelegation.md) 
[移除-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
[AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="9f350-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
