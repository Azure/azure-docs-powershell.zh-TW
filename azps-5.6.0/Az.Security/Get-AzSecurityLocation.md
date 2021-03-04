---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: b835113b07fb2295193b89fd817ba82ceca71655
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913325"
---
# <span data-ttu-id="80a59-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="80a59-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="80a59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80a59-102">SYNOPSIS</span></span>
<span data-ttu-id="80a59-103">獲得 Azure 資訊安全中心會自動儲存特定訂閱資料的位置</span><span class="sxs-lookup"><span data-stu-id="80a59-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="80a59-104">語法</span><span class="sxs-lookup"><span data-stu-id="80a59-104">SYNTAX</span></span>

### <span data-ttu-id="80a59-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="80a59-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a59-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="80a59-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a59-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a59-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80a59-108">描述</span><span class="sxs-lookup"><span data-stu-id="80a59-108">DESCRIPTION</span></span>
<span data-ttu-id="80a59-109">Azure 資訊安全中心會自動決定儲存部分資料的位置。</span><span class="sxs-lookup"><span data-stu-id="80a59-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="80a59-110">使用此 Cmdlet 探索該位置。</span><span class="sxs-lookup"><span data-stu-id="80a59-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="80a59-111">例子</span><span class="sxs-lookup"><span data-stu-id="80a59-111">EXAMPLES</span></span>

### <span data-ttu-id="80a59-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="80a59-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="80a59-113">獲得 Azure 資訊安全中心會保存計算安全性資料的位置。</span><span class="sxs-lookup"><span data-stu-id="80a59-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="80a59-114">參數</span><span class="sxs-lookup"><span data-stu-id="80a59-114">PARAMETERS</span></span>

### <span data-ttu-id="80a59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a59-115">-DefaultProfile</span></span>
<span data-ttu-id="80a59-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="80a59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a59-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="80a59-117">-Name</span></span>
<span data-ttu-id="80a59-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="80a59-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a59-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a59-119">-ResourceId</span></span>
<span data-ttu-id="80a59-120">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="80a59-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a59-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a59-121">CommonParameters</span></span>
<span data-ttu-id="80a59-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80a59-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a59-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80a59-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a59-124">輸入</span><span class="sxs-lookup"><span data-stu-id="80a59-124">INPUTS</span></span>

### <span data-ttu-id="80a59-125">System.String</span><span class="sxs-lookup"><span data-stu-id="80a59-125">System.String</span></span>

## <span data-ttu-id="80a59-126">輸出</span><span class="sxs-lookup"><span data-stu-id="80a59-126">OUTPUTS</span></span>

### <span data-ttu-id="80a59-127">Microsoft.Azure.Commands.security.models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="80a59-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="80a59-128">筆記</span><span class="sxs-lookup"><span data-stu-id="80a59-128">NOTES</span></span>

## <span data-ttu-id="80a59-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="80a59-129">RELATED LINKS</span></span>
