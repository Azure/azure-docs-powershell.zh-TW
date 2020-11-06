---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445463"
---
# <span data-ttu-id="220a1-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="220a1-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="220a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="220a1-102">SYNOPSIS</span></span>
<span data-ttu-id="220a1-103">取得 Azure 安全中心將針對特定訂閱自動儲存資料的位置</span><span class="sxs-lookup"><span data-stu-id="220a1-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="220a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="220a1-104">SYNTAX</span></span>

### <span data-ttu-id="220a1-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="220a1-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="220a1-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="220a1-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="220a1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="220a1-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="220a1-108">說明</span><span class="sxs-lookup"><span data-stu-id="220a1-108">DESCRIPTION</span></span>
<span data-ttu-id="220a1-109">Azure 安全中心會自動決定要儲存部分資料的位置。</span><span class="sxs-lookup"><span data-stu-id="220a1-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="220a1-110">使用此 Cmdlet 來探索該位置。</span><span class="sxs-lookup"><span data-stu-id="220a1-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="220a1-111">示例</span><span class="sxs-lookup"><span data-stu-id="220a1-111">EXAMPLES</span></span>

### <span data-ttu-id="220a1-112">範例1</span><span class="sxs-lookup"><span data-stu-id="220a1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="220a1-113">取得 Azure 安全中心儲存計算安全性資料的位置。</span><span class="sxs-lookup"><span data-stu-id="220a1-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="220a1-114">參數</span><span class="sxs-lookup"><span data-stu-id="220a1-114">PARAMETERS</span></span>

### <span data-ttu-id="220a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220a1-115">-DefaultProfile</span></span>
<span data-ttu-id="220a1-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="220a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220a1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="220a1-117">-Name</span></span>
<span data-ttu-id="220a1-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="220a1-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220a1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="220a1-119">-ResourceId</span></span>
<span data-ttu-id="220a1-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="220a1-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220a1-121">CommonParameters</span></span>
<span data-ttu-id="220a1-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="220a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220a1-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="220a1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220a1-124">輸入</span><span class="sxs-lookup"><span data-stu-id="220a1-124">INPUTS</span></span>

### <span data-ttu-id="220a1-125">System.object</span><span class="sxs-lookup"><span data-stu-id="220a1-125">System.String</span></span>

## <span data-ttu-id="220a1-126">輸出</span><span class="sxs-lookup"><span data-stu-id="220a1-126">OUTPUTS</span></span>

### <span data-ttu-id="220a1-127">PSSecurityLocation （Security..。</span><span class="sxs-lookup"><span data-stu-id="220a1-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="220a1-128">筆記</span><span class="sxs-lookup"><span data-stu-id="220a1-128">NOTES</span></span>

## <span data-ttu-id="220a1-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="220a1-129">RELATED LINKS</span></span>
