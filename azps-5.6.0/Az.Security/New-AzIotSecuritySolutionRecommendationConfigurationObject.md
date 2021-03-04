---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 677c67ecc2418a4940b4cbe79e2ac7145eada0c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909961"
---
# <span data-ttu-id="9c8b7-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="9c8b7-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="9c8b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9c8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8b7-103">為 iot 安全性解決方案建立新建議組</span><span class="sxs-lookup"><span data-stu-id="9c8b7-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="9c8b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="9c8b7-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c8b7-105">描述</span><span class="sxs-lookup"><span data-stu-id="9c8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="9c8b7-106">AzIotSecuritySolutionRecommendationConfigurationObject 會為 iot 安全性解決方案建立新的建議組組物件。</span><span class="sxs-lookup"><span data-stu-id="9c8b7-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="9c8b7-107">如此一來，建議的狀態即會處於啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="9c8b7-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="9c8b7-108">例子</span><span class="sxs-lookup"><span data-stu-id="9c8b7-108">EXAMPLES</span></span>

### <span data-ttu-id="9c8b7-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="9c8b7-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="9c8b7-110">建立建議類型 「IoT_ACRAuthentication」的新建議設定，並設定為停用狀態</span><span class="sxs-lookup"><span data-stu-id="9c8b7-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="9c8b7-111">參數</span><span class="sxs-lookup"><span data-stu-id="9c8b7-111">PARAMETERS</span></span>

### <span data-ttu-id="9c8b7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8b7-112">-DefaultProfile</span></span>
<span data-ttu-id="9c8b7-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c8b7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c8b7-114">-已啟用</span><span class="sxs-lookup"><span data-stu-id="9c8b7-114">-Enabled</span></span>
<span data-ttu-id="9c8b7-115">地位。</span><span class="sxs-lookup"><span data-stu-id="9c8b7-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8b7-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="9c8b7-116">-RecommendationType</span></span>
<span data-ttu-id="9c8b7-117">建議類型。</span><span class="sxs-lookup"><span data-stu-id="9c8b7-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8b7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8b7-118">CommonParameters</span></span>
<span data-ttu-id="9c8b7-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9c8b7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8b7-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c8b7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8b7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9c8b7-121">INPUTS</span></span>

### <span data-ttu-id="9c8b7-122">沒有</span><span class="sxs-lookup"><span data-stu-id="9c8b7-122">None</span></span>

## <span data-ttu-id="9c8b7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9c8b7-123">OUTPUTS</span></span>

### <span data-ttu-id="9c8b7-124">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c8b7-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="9c8b7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="9c8b7-125">NOTES</span></span>

## <span data-ttu-id="9c8b7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c8b7-126">RELATED LINKS</span></span>
