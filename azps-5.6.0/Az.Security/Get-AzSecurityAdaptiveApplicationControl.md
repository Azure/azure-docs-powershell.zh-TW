---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: ec35083cf4495d0bf262d841563f0dc4100dcdc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907510"
---
# <span data-ttu-id="2f0c2-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="2f0c2-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="2f0c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0c2-103">獲得訂閱的應用程式控制項 VM/伺服器群組清單。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2f0c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f0c2-104">SYNTAX</span></span>

### <span data-ttu-id="2f0c2-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="2f0c2-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f0c2-106">描述</span><span class="sxs-lookup"><span data-stu-id="2f0c2-106">DESCRIPTION</span></span>
<span data-ttu-id="2f0c2-107">自適性應用程式控制項是由 Azure 資訊安全中心自動計算，使用此 Cmdlet 取得訂閱範圍中的自適性應用程式控制項資源清單。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="2f0c2-108">例子</span><span class="sxs-lookup"><span data-stu-id="2f0c2-108">EXAMPLES</span></span>

### <span data-ttu-id="2f0c2-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f0c2-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="2f0c2-110">獲得訂閱的應用程式控制項 VM/伺服器群組清單。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2f0c2-111">參數</span><span class="sxs-lookup"><span data-stu-id="2f0c2-111">PARAMETERS</span></span>

### <span data-ttu-id="2f0c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0c2-112">-DefaultProfile</span></span>
<span data-ttu-id="2f0c2-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f0c2-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f0c2-114">-SubscriptionId</span></span>
<span data-ttu-id="2f0c2-115">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0c2-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="2f0c2-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="2f0c2-117">包含原則規則。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0c2-118">-摘要</span><span class="sxs-lookup"><span data-stu-id="2f0c2-118">-Summary</span></span>
<span data-ttu-id="2f0c2-119">以摘要形式返回輸出。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0c2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0c2-120">CommonParameters</span></span>
<span data-ttu-id="2f0c2-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0c2-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2f0c2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0c2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2f0c2-123">INPUTS</span></span>

### <span data-ttu-id="2f0c2-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2f0c2-124">System.String</span></span>

### <span data-ttu-id="2f0c2-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f0c2-125">System.Boolean</span></span>

## <span data-ttu-id="2f0c2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2f0c2-126">OUTPUTS</span></span>

### <span data-ttu-id="2f0c2-127">Microsoft.Azure.Commands.security.models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="2f0c2-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="2f0c2-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2f0c2-128">NOTES</span></span>

## <span data-ttu-id="2f0c2-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f0c2-129">RELATED LINKS</span></span>
