---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452843"
---
# <span data-ttu-id="c7fab-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="c7fab-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="c7fab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7fab-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fab-103">取得 CDN 設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="c7fab-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7fab-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7fab-104">SYNTAX</span></span>

### <span data-ttu-id="c7fab-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c7fab-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7fab-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fab-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7fab-107">說明</span><span class="sxs-lookup"><span data-stu-id="c7fab-107">DESCRIPTION</span></span>
<span data-ttu-id="c7fab-108">**AzureRmCdnProfileSupportedOptimizationType** Cmdlet 會取得目前設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="c7fab-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="c7fab-109">使用者可以使用所列的值來建立具有 [優化類型] 的端點。</span><span class="sxs-lookup"><span data-stu-id="c7fab-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="c7fab-110">示例</span><span class="sxs-lookup"><span data-stu-id="c7fab-110">EXAMPLES</span></span>

### <span data-ttu-id="c7fab-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c7fab-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="c7fab-112">取得 CDN 設定檔支援的優化類型。</span><span class="sxs-lookup"><span data-stu-id="c7fab-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="c7fab-113">參數</span><span class="sxs-lookup"><span data-stu-id="c7fab-113">PARAMETERS</span></span>

### <span data-ttu-id="c7fab-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c7fab-114">-CdnProfile</span></span>
<span data-ttu-id="c7fab-115">Azure CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="c7fab-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="c7fab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fab-116">-DefaultProfile</span></span>
<span data-ttu-id="c7fab-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7fab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7fab-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c7fab-118">-ProfileName</span></span>
<span data-ttu-id="c7fab-119">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7fab-119">The name of the profile.</span></span>

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

### <span data-ttu-id="c7fab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7fab-120">-ResourceGroupName</span></span>
<span data-ttu-id="c7fab-121">設定檔所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c7fab-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c7fab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fab-122">CommonParameters</span></span>
<span data-ttu-id="c7fab-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7fab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fab-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7fab-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fab-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c7fab-125">INPUTS</span></span>

### <span data-ttu-id="c7fab-126">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c7fab-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="c7fab-127">參數： CdnProfile (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c7fab-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="c7fab-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c7fab-128">OUTPUTS</span></span>

### <span data-ttu-id="c7fab-129">PSOptimizationType 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c7fab-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="c7fab-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c7fab-130">NOTES</span></span>

## <span data-ttu-id="c7fab-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7fab-131">RELATED LINKS</span></span>
