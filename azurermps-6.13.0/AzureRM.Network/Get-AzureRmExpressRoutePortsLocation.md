---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626068"
---
# <span data-ttu-id="3e477-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="3e477-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="3e477-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e477-102">SYNOPSIS</span></span>
<span data-ttu-id="3e477-103">取得 ExpressRoutePort 資源可供使用的位置。</span><span class="sxs-lookup"><span data-stu-id="3e477-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e477-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e477-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e477-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e477-105">DESCRIPTION</span></span>
<span data-ttu-id="3e477-106">**AzureRmExpressRoutePortsLocation** Cmdlet 是用來檢索 ExpressRoutePort 資源可用的位置。</span><span class="sxs-lookup"><span data-stu-id="3e477-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="3e477-107">已知特定位置作為輸入，此 Cmdlet 會顯示該位置的詳細資料，例如該位置的可用頻寬清單。</span><span class="sxs-lookup"><span data-stu-id="3e477-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="3e477-108">示例</span><span class="sxs-lookup"><span data-stu-id="3e477-108">EXAMPLES</span></span>

### <span data-ttu-id="3e477-109">範例1</span><span class="sxs-lookup"><span data-stu-id="3e477-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="3e477-110">列出可用 ExpressRoutePort 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="3e477-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="3e477-111">範例2</span><span class="sxs-lookup"><span data-stu-id="3e477-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="3e477-112">列出 $loc 位置的可用 ExpressRoutePort 頻寬。</span><span class="sxs-lookup"><span data-stu-id="3e477-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="3e477-113">參數</span><span class="sxs-lookup"><span data-stu-id="3e477-113">PARAMETERS</span></span>

### <span data-ttu-id="3e477-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e477-114">-DefaultProfile</span></span>
<span data-ttu-id="3e477-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e477-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e477-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="3e477-116">-LocationName</span></span>
<span data-ttu-id="3e477-117">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e477-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e477-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e477-118">CommonParameters</span></span>
<span data-ttu-id="3e477-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e477-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e477-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e477-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e477-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3e477-121">INPUTS</span></span>

### <span data-ttu-id="3e477-122">System.object</span><span class="sxs-lookup"><span data-stu-id="3e477-122">System.String</span></span>

## <span data-ttu-id="3e477-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3e477-123">OUTPUTS</span></span>

### <span data-ttu-id="3e477-124">PSExpressRoutePortsLocation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3e477-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="3e477-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3e477-125">NOTES</span></span>

## <span data-ttu-id="3e477-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e477-126">RELATED LINKS</span></span>
