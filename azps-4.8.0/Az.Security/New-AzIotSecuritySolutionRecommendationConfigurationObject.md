---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129924"
---
# <span data-ttu-id="92f74-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="92f74-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="92f74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92f74-102">SYNOPSIS</span></span>
<span data-ttu-id="92f74-103">為 iot 安全解決方案建立新的建議配置</span><span class="sxs-lookup"><span data-stu-id="92f74-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="92f74-104">句法</span><span class="sxs-lookup"><span data-stu-id="92f74-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f74-105">說明</span><span class="sxs-lookup"><span data-stu-id="92f74-105">DESCRIPTION</span></span>
<span data-ttu-id="92f74-106">AzIotSecuritySolutionRecommendationConfigurationObject 會為 iot 安全解決方案建立新的建議設定物件。</span><span class="sxs-lookup"><span data-stu-id="92f74-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="92f74-107">如此一來，就會設定建議的狀態（無論是已啟用還是停用）。</span><span class="sxs-lookup"><span data-stu-id="92f74-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="92f74-108">示例</span><span class="sxs-lookup"><span data-stu-id="92f74-108">EXAMPLES</span></span>

### <span data-ttu-id="92f74-109">範例1</span><span class="sxs-lookup"><span data-stu-id="92f74-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="92f74-110">針對建議輸入 "IoT_ACRAuthentication" （狀態設定為 [停用]）建立新的建議配置</span><span class="sxs-lookup"><span data-stu-id="92f74-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="92f74-111">參數</span><span class="sxs-lookup"><span data-stu-id="92f74-111">PARAMETERS</span></span>

### <span data-ttu-id="92f74-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f74-112">-DefaultProfile</span></span>
<span data-ttu-id="92f74-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92f74-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f74-114">-啟用</span><span class="sxs-lookup"><span data-stu-id="92f74-114">-Enabled</span></span>
<span data-ttu-id="92f74-115">狀態值.</span><span class="sxs-lookup"><span data-stu-id="92f74-115">Status .</span></span>

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

### <span data-ttu-id="92f74-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="92f74-116">-RecommendationType</span></span>
<span data-ttu-id="92f74-117">建議類型。</span><span class="sxs-lookup"><span data-stu-id="92f74-117">Recommendation type.</span></span>

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

### <span data-ttu-id="92f74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f74-118">CommonParameters</span></span>
<span data-ttu-id="92f74-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92f74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f74-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="92f74-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f74-121">輸入</span><span class="sxs-lookup"><span data-stu-id="92f74-121">INPUTS</span></span>

### <span data-ttu-id="92f74-122">所有</span><span class="sxs-lookup"><span data-stu-id="92f74-122">None</span></span>

## <span data-ttu-id="92f74-123">輸出</span><span class="sxs-lookup"><span data-stu-id="92f74-123">OUTPUTS</span></span>

### <span data-ttu-id="92f74-124">PSRecommendationConfiguration 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="92f74-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="92f74-125">筆記</span><span class="sxs-lookup"><span data-stu-id="92f74-125">NOTES</span></span>

## <span data-ttu-id="92f74-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="92f74-126">RELATED LINKS</span></span>
