---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126845"
---
# <span data-ttu-id="ca7e7-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="ca7e7-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="ca7e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7e7-103">取得 Azure 安全中心將針對特定訂閱自動儲存資料的位置</span><span class="sxs-lookup"><span data-stu-id="ca7e7-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="ca7e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca7e7-104">SYNTAX</span></span>

### <span data-ttu-id="ca7e7-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="ca7e7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca7e7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ca7e7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca7e7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca7e7-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca7e7-108">說明</span><span class="sxs-lookup"><span data-stu-id="ca7e7-108">DESCRIPTION</span></span>
<span data-ttu-id="ca7e7-109">Azure 安全中心會自動決定要儲存部分資料的位置。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="ca7e7-110">使用此 Cmdlet 來探索該位置。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="ca7e7-111">示例</span><span class="sxs-lookup"><span data-stu-id="ca7e7-111">EXAMPLES</span></span>

### <span data-ttu-id="ca7e7-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ca7e7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="ca7e7-113">取得 Azure 安全中心儲存計算安全性資料的位置。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="ca7e7-114">參數</span><span class="sxs-lookup"><span data-stu-id="ca7e7-114">PARAMETERS</span></span>

### <span data-ttu-id="ca7e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7e7-115">-DefaultProfile</span></span>
<span data-ttu-id="ca7e7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca7e7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca7e7-117">-Name</span></span>
<span data-ttu-id="ca7e7-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-118">Resource name.</span></span>

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

### <span data-ttu-id="ca7e7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca7e7-119">-ResourceId</span></span>
<span data-ttu-id="ca7e7-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-120">Resource ID.</span></span>

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

### <span data-ttu-id="ca7e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7e7-121">CommonParameters</span></span>
<span data-ttu-id="ca7e7-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7e7-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7e7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ca7e7-124">INPUTS</span></span>

### <span data-ttu-id="ca7e7-125">System.object</span><span class="sxs-lookup"><span data-stu-id="ca7e7-125">System.String</span></span>

## <span data-ttu-id="ca7e7-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ca7e7-126">OUTPUTS</span></span>

### <span data-ttu-id="ca7e7-127">PSSecurityLocation （Security..。</span><span class="sxs-lookup"><span data-stu-id="ca7e7-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="ca7e7-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ca7e7-128">NOTES</span></span>

## <span data-ttu-id="ca7e7-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca7e7-129">RELATED LINKS</span></span>
