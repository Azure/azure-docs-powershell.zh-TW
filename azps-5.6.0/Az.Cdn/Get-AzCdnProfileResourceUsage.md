---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 1a4e3f08653f6c7bda799b55618caff4e77fe7bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915601"
---
# <span data-ttu-id="09387-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="09387-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="09387-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09387-102">SYNOPSIS</span></span>
<span data-ttu-id="09387-103">獲得 CDN 設定檔的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="09387-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="09387-104">語法</span><span class="sxs-lookup"><span data-stu-id="09387-104">SYNTAX</span></span>

### <span data-ttu-id="09387-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="09387-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09387-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09387-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09387-107">描述</span><span class="sxs-lookup"><span data-stu-id="09387-107">DESCRIPTION</span></span>
<span data-ttu-id="09387-108">{{填寫 Description}}</span><span class="sxs-lookup"><span data-stu-id="09387-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="09387-109">例子</span><span class="sxs-lookup"><span data-stu-id="09387-109">EXAMPLES</span></span>

### <span data-ttu-id="09387-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="09387-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="09387-111">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="09387-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="09387-112">參數</span><span class="sxs-lookup"><span data-stu-id="09387-112">PARAMETERS</span></span>

### <span data-ttu-id="09387-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="09387-113">-CdnProfile</span></span>
<span data-ttu-id="09387-114">Azure CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="09387-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="09387-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09387-115">-DefaultProfile</span></span>
<span data-ttu-id="09387-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="09387-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09387-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="09387-117">-ProfileName</span></span>
<span data-ttu-id="09387-118">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="09387-118">The name of the profile.</span></span>

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

### <span data-ttu-id="09387-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09387-119">-ResourceGroupName</span></span>
<span data-ttu-id="09387-120">設定檔所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="09387-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="09387-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09387-121">CommonParameters</span></span>
<span data-ttu-id="09387-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09387-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09387-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09387-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09387-124">輸入</span><span class="sxs-lookup"><span data-stu-id="09387-124">INPUTS</span></span>

### <span data-ttu-id="09387-125">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="09387-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="09387-126">輸出</span><span class="sxs-lookup"><span data-stu-id="09387-126">OUTPUTS</span></span>

### <span data-ttu-id="09387-127">Microsoft.Azure.Commands.Cdn.models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="09387-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="09387-128">筆記</span><span class="sxs-lookup"><span data-stu-id="09387-128">NOTES</span></span>

## <span data-ttu-id="09387-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="09387-129">RELATED LINKS</span></span>
