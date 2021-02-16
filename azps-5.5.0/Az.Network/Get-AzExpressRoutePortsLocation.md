---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133907"
---
# <span data-ttu-id="af9e7-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="af9e7-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="af9e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="af9e7-103">取得 ExpressRoutePort 資源可供使用的位置。</span><span class="sxs-lookup"><span data-stu-id="af9e7-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="af9e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="af9e7-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af9e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="af9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="af9e7-106">**AzExpressRoutePortsLocation** Cmdlet 是用來檢索 ExpressRoutePort 資源可用的位置。</span><span class="sxs-lookup"><span data-stu-id="af9e7-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="af9e7-107">已知特定位置作為輸入，此 Cmdlet 會顯示該位置的詳細資料，例如該位置的可用頻寬清單。</span><span class="sxs-lookup"><span data-stu-id="af9e7-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="af9e7-108">示例</span><span class="sxs-lookup"><span data-stu-id="af9e7-108">EXAMPLES</span></span>

### <span data-ttu-id="af9e7-109">範例1</span><span class="sxs-lookup"><span data-stu-id="af9e7-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="af9e7-110">列出可用 ExpressRoutePort 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="af9e7-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="af9e7-111">範例2</span><span class="sxs-lookup"><span data-stu-id="af9e7-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="af9e7-112">列出 $loc 位置的可用 ExpressRoutePort 頻寬。</span><span class="sxs-lookup"><span data-stu-id="af9e7-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="af9e7-113">參數</span><span class="sxs-lookup"><span data-stu-id="af9e7-113">PARAMETERS</span></span>

### <span data-ttu-id="af9e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9e7-114">-DefaultProfile</span></span>
<span data-ttu-id="af9e7-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af9e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9e7-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="af9e7-116">-LocationName</span></span>
<span data-ttu-id="af9e7-117">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="af9e7-117">The name of the location.</span></span>

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

### <span data-ttu-id="af9e7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9e7-118">CommonParameters</span></span>
<span data-ttu-id="af9e7-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af9e7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9e7-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af9e7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9e7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="af9e7-121">INPUTS</span></span>

### <span data-ttu-id="af9e7-122">System.object</span><span class="sxs-lookup"><span data-stu-id="af9e7-122">System.String</span></span>

## <span data-ttu-id="af9e7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="af9e7-123">OUTPUTS</span></span>

### <span data-ttu-id="af9e7-124">PSExpressRoutePortsLocation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af9e7-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="af9e7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="af9e7-125">NOTES</span></span>

## <span data-ttu-id="af9e7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="af9e7-126">RELATED LINKS</span></span>
