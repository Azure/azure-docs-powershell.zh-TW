---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d5fca22bf289c42681d9af18a9eaff28587f1922
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792152"
---
# <span data-ttu-id="d68d9-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d68d9-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="d68d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d68d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d68d9-103">取得由 Azure 安全中心探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d68d9-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="d68d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="d68d9-104">SYNTAX</span></span>

### <span data-ttu-id="d68d9-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="d68d9-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d68d9-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d68d9-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d68d9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d68d9-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d68d9-108">說明</span><span class="sxs-lookup"><span data-stu-id="d68d9-108">DESCRIPTION</span></span>
<span data-ttu-id="d68d9-109">安全性解決方案是由 Azure 安全中心自動探索，使用此 Cmdlet 來查看已探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d68d9-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="d68d9-110">示例</span><span class="sxs-lookup"><span data-stu-id="d68d9-110">EXAMPLES</span></span>

### <span data-ttu-id="d68d9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d68d9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="d68d9-112">取得訂閱中所有已探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d68d9-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="d68d9-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d68d9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="d68d9-114">取得特定的安全解決方案</span><span class="sxs-lookup"><span data-stu-id="d68d9-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="d68d9-115">參數</span><span class="sxs-lookup"><span data-stu-id="d68d9-115">PARAMETERS</span></span>

### <span data-ttu-id="d68d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68d9-116">-DefaultProfile</span></span>
<span data-ttu-id="d68d9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d68d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68d9-118">-位置</span><span class="sxs-lookup"><span data-stu-id="d68d9-118">-Location</span></span>
<span data-ttu-id="d68d9-119">位於.</span><span class="sxs-lookup"><span data-stu-id="d68d9-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68d9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d68d9-120">-Name</span></span>
<span data-ttu-id="d68d9-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d68d9-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="d68d9-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d68d9-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68d9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d68d9-124">-ResourceId</span></span>
<span data-ttu-id="d68d9-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d68d9-125">Resource ID.</span></span>

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

### <span data-ttu-id="d68d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68d9-126">CommonParameters</span></span>
<span data-ttu-id="d68d9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d68d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68d9-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d68d9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68d9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d68d9-129">INPUTS</span></span>

### <span data-ttu-id="d68d9-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d68d9-130">System.String</span></span>

## <span data-ttu-id="d68d9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d68d9-131">OUTPUTS</span></span>

### <span data-ttu-id="d68d9-132">PSSecurityDiscoveredSecuritySolution 中的 DiscoveredSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="d68d9-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="d68d9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d68d9-133">NOTES</span></span>

## <span data-ttu-id="d68d9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d68d9-134">RELATED LINKS</span></span>
