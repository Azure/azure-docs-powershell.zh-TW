---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128315"
---
# <span data-ttu-id="e97fb-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="e97fb-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="e97fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e97fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e97fb-103">取得訂閱的應用程式控制項 VM/伺服器群組清單。</span><span class="sxs-lookup"><span data-stu-id="e97fb-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="e97fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="e97fb-104">SYNTAX</span></span>

### <span data-ttu-id="e97fb-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="e97fb-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e97fb-106">說明</span><span class="sxs-lookup"><span data-stu-id="e97fb-106">DESCRIPTION</span></span>
<span data-ttu-id="e97fb-107">彈性應用程式控制項是由 Azure 安全中心自動計算的，請使用此 Cmdlet 來取得訂閱範圍中的彈性應用程式控制項資源清單。</span><span class="sxs-lookup"><span data-stu-id="e97fb-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="e97fb-108">示例</span><span class="sxs-lookup"><span data-stu-id="e97fb-108">EXAMPLES</span></span>

### <span data-ttu-id="e97fb-109">範例1</span><span class="sxs-lookup"><span data-stu-id="e97fb-109">Example 1</span></span>
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
<span data-ttu-id="e97fb-110">取得訂閱的應用程式控制項 VM/伺服器群組清單。</span><span class="sxs-lookup"><span data-stu-id="e97fb-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="e97fb-111">參數</span><span class="sxs-lookup"><span data-stu-id="e97fb-111">PARAMETERS</span></span>

### <span data-ttu-id="e97fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97fb-112">-DefaultProfile</span></span>
<span data-ttu-id="e97fb-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e97fb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e97fb-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e97fb-114">-SubscriptionId</span></span>
<span data-ttu-id="e97fb-115">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="e97fb-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="e97fb-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="e97fb-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="e97fb-117">包括原則規則。</span><span class="sxs-lookup"><span data-stu-id="e97fb-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="e97fb-118">-摘要</span><span class="sxs-lookup"><span data-stu-id="e97fb-118">-Summary</span></span>
<span data-ttu-id="e97fb-119">傳回匯總表單中的輸出。</span><span class="sxs-lookup"><span data-stu-id="e97fb-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="e97fb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97fb-120">CommonParameters</span></span>
<span data-ttu-id="e97fb-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e97fb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97fb-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e97fb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97fb-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e97fb-123">INPUTS</span></span>

### <span data-ttu-id="e97fb-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e97fb-124">System.String</span></span>

### <span data-ttu-id="e97fb-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e97fb-125">System.Boolean</span></span>

## <span data-ttu-id="e97fb-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e97fb-126">OUTPUTS</span></span>

### <span data-ttu-id="e97fb-127">PSSecurityAdaptiveApplicationControls 中的 AdaptiveApplicationControls （Security..。</span><span class="sxs-lookup"><span data-stu-id="e97fb-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="e97fb-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e97fb-128">NOTES</span></span>

## <span data-ttu-id="e97fb-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e97fb-129">RELATED LINKS</span></span>
