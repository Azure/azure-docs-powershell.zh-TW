---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: d98b9d2395c0795c37fd9d7cf31dc354bde3b7cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912722"
---
# <span data-ttu-id="ecfec-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="ecfec-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="ecfec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ecfec-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfec-103">取得地區的可用服務。</span><span class="sxs-lookup"><span data-stu-id="ecfec-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="ecfec-104">語法</span><span class="sxs-lookup"><span data-stu-id="ecfec-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ecfec-105">描述</span><span class="sxs-lookup"><span data-stu-id="ecfec-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfec-106">**Get-AzAvailableServiceDelegation Cmdlet** 可讓您針對提供位置中的子網，取得所有可用的服務轉寄。</span><span class="sxs-lookup"><span data-stu-id="ecfec-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="ecfec-107">此 Cmdlet *不會* 描述單一子網上可能共存的主機。</span><span class="sxs-lookup"><span data-stu-id="ecfec-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="ecfec-108">例子</span><span class="sxs-lookup"><span data-stu-id="ecfec-108">EXAMPLES</span></span>

### <span data-ttu-id="ecfec-109">1：取得所有可用的服務</span><span class="sxs-lookup"><span data-stu-id="ecfec-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="ecfec-110">參數</span><span class="sxs-lookup"><span data-stu-id="ecfec-110">PARAMETERS</span></span>

### <span data-ttu-id="ecfec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfec-111">-DefaultProfile</span></span>
<span data-ttu-id="ecfec-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecfec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfec-113">-位置</span><span class="sxs-lookup"><span data-stu-id="ecfec-113">-Location</span></span>
<span data-ttu-id="ecfec-114">位置。</span><span class="sxs-lookup"><span data-stu-id="ecfec-114">The location.</span></span>

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

### <span data-ttu-id="ecfec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfec-115">CommonParameters</span></span>
<span data-ttu-id="ecfec-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ecfec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfec-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecfec-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfec-118">輸入</span><span class="sxs-lookup"><span data-stu-id="ecfec-118">INPUTS</span></span>

### <span data-ttu-id="ecfec-119">System.String</span><span class="sxs-lookup"><span data-stu-id="ecfec-119">System.String</span></span>

## <span data-ttu-id="ecfec-120">輸出</span><span class="sxs-lookup"><span data-stu-id="ecfec-120">OUTPUTS</span></span>

### <span data-ttu-id="ecfec-121">Microsoft.Azure.Commands.Network.models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="ecfec-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="ecfec-122">筆記</span><span class="sxs-lookup"><span data-stu-id="ecfec-122">NOTES</span></span>

## <span data-ttu-id="ecfec-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecfec-123">RELATED LINKS</span></span>

<span data-ttu-id="ecfec-124">[Add-AzDelegation](./Add-AzDelegation.md) 
[New-AzDelegation](./New-AzDelegation.md) 
[Remove-AzDelegation](./Remove-AzDelegation.md) 
[Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="ecfec-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>