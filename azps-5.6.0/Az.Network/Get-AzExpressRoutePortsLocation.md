---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: d16b5d916f3a807de818c58de94f7f0841e04d17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903166"
---
# <span data-ttu-id="5b0f5-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="5b0f5-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="5b0f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5b0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0f5-103">獲得可以使用 ExpressRoutePort 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="5b0f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="5b0f5-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b0f5-105">描述</span><span class="sxs-lookup"><span data-stu-id="5b0f5-105">DESCRIPTION</span></span>
<span data-ttu-id="5b0f5-106">**Get-AzExpressRoutePortsLocation** Cmdlet 是用來取回可用 ExpressRoutePort 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="5b0f5-107">如果指定特定位置做為輸入，Cmdlet 會顯示該位置的詳細資訊，即該位置的可用頻寬清單。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="5b0f5-108">例子</span><span class="sxs-lookup"><span data-stu-id="5b0f5-108">EXAMPLES</span></span>

### <span data-ttu-id="5b0f5-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="5b0f5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="5b0f5-110">列出可以使用 ExpressRoutePort 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="5b0f5-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="5b0f5-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="5b0f5-112">列出可在位置或位置使用 ExpressRoutePort $loc。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="5b0f5-113">參數</span><span class="sxs-lookup"><span data-stu-id="5b0f5-113">PARAMETERS</span></span>

### <span data-ttu-id="5b0f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0f5-114">-DefaultProfile</span></span>
<span data-ttu-id="5b0f5-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b0f5-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="5b0f5-116">-LocationName</span></span>
<span data-ttu-id="5b0f5-117">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-117">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0f5-118">CommonParameters</span></span>
<span data-ttu-id="5b0f5-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5b0f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0f5-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b0f5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0f5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5b0f5-121">INPUTS</span></span>

### <span data-ttu-id="5b0f5-122">System.String</span><span class="sxs-lookup"><span data-stu-id="5b0f5-122">System.String</span></span>

## <span data-ttu-id="5b0f5-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5b0f5-123">OUTPUTS</span></span>

### <span data-ttu-id="5b0f5-124">Microsoft.Azure.Commands.Network.models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="5b0f5-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="5b0f5-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5b0f5-125">NOTES</span></span>

## <span data-ttu-id="5b0f5-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b0f5-126">RELATED LINKS</span></span>
