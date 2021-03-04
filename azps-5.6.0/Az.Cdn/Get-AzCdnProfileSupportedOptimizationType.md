---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: f26e1bd19b9856df7bf68de6c8afddefb3ee64a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911190"
---
# <span data-ttu-id="2614f-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="2614f-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="2614f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2614f-102">SYNOPSIS</span></span>
<span data-ttu-id="2614f-103">獲得 CDN 設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="2614f-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="2614f-104">語法</span><span class="sxs-lookup"><span data-stu-id="2614f-104">SYNTAX</span></span>

### <span data-ttu-id="2614f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2614f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2614f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2614f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2614f-107">描述</span><span class="sxs-lookup"><span data-stu-id="2614f-107">DESCRIPTION</span></span>
<span data-ttu-id="2614f-108">**Get-AzCdnProfileSupportedOptimizationType** Cmdlet 會取得目前設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="2614f-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="2614f-109">使用者可以從列出的值建立具有優化類型的端點。</span><span class="sxs-lookup"><span data-stu-id="2614f-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="2614f-110">例子</span><span class="sxs-lookup"><span data-stu-id="2614f-110">EXAMPLES</span></span>

### <span data-ttu-id="2614f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2614f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="2614f-112">取得 CDN 設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="2614f-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="2614f-113">參數</span><span class="sxs-lookup"><span data-stu-id="2614f-113">PARAMETERS</span></span>

### <span data-ttu-id="2614f-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2614f-114">-CdnProfile</span></span>
<span data-ttu-id="2614f-115">Azure CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="2614f-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2614f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2614f-116">-DefaultProfile</span></span>
<span data-ttu-id="2614f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2614f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2614f-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2614f-118">-ProfileName</span></span>
<span data-ttu-id="2614f-119">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="2614f-119">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2614f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2614f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2614f-121">設定檔所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2614f-121">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2614f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2614f-122">CommonParameters</span></span>
<span data-ttu-id="2614f-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2614f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2614f-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2614f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2614f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2614f-125">INPUTS</span></span>

### <span data-ttu-id="2614f-126">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="2614f-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="2614f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2614f-127">OUTPUTS</span></span>

### <span data-ttu-id="2614f-128">Microsoft.Azure.Commands.Cdn.models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="2614f-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="2614f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2614f-129">NOTES</span></span>

## <span data-ttu-id="2614f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2614f-130">RELATED LINKS</span></span>
