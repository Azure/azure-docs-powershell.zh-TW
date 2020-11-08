---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128526"
---
# <span data-ttu-id="c0181-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="c0181-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="c0181-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0181-102">SYNOPSIS</span></span>
<span data-ttu-id="c0181-103">取得 CDN 設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="c0181-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="c0181-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0181-104">SYNTAX</span></span>

### <span data-ttu-id="c0181-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0181-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0181-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0181-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0181-107">說明</span><span class="sxs-lookup"><span data-stu-id="c0181-107">DESCRIPTION</span></span>
<span data-ttu-id="c0181-108">**AzCdnProfileSupportedOptimizationType** Cmdlet 會取得目前設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="c0181-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="c0181-109">使用者可以使用所列的值來建立具有 [優化類型] 的端點。</span><span class="sxs-lookup"><span data-stu-id="c0181-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="c0181-110">示例</span><span class="sxs-lookup"><span data-stu-id="c0181-110">EXAMPLES</span></span>

### <span data-ttu-id="c0181-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c0181-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="c0181-112">取得 CDN 設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="c0181-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="c0181-113">參數</span><span class="sxs-lookup"><span data-stu-id="c0181-113">PARAMETERS</span></span>

### <span data-ttu-id="c0181-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c0181-114">-CdnProfile</span></span>
<span data-ttu-id="c0181-115">Azure CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="c0181-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="c0181-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0181-116">-DefaultProfile</span></span>
<span data-ttu-id="c0181-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0181-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0181-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c0181-118">-ProfileName</span></span>
<span data-ttu-id="c0181-119">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0181-119">The name of the profile.</span></span>

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

### <span data-ttu-id="c0181-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0181-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0181-121">設定檔所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c0181-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c0181-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0181-122">CommonParameters</span></span>
<span data-ttu-id="c0181-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0181-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0181-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0181-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0181-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c0181-125">INPUTS</span></span>

### <span data-ttu-id="c0181-126">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0181-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c0181-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c0181-127">OUTPUTS</span></span>

### <span data-ttu-id="c0181-128">PSOptimizationType 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0181-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="c0181-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c0181-129">NOTES</span></span>

## <span data-ttu-id="c0181-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0181-130">RELATED LINKS</span></span>
