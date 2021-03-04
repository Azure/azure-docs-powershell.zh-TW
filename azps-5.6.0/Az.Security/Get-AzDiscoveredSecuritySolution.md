---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d351ab76941d16e3d3e091e223524863d4256d75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910649"
---
# <span data-ttu-id="d651e-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d651e-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="d651e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d651e-102">SYNOPSIS</span></span>
<span data-ttu-id="d651e-103">獲得 Azure 資訊安全中心所發現的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d651e-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="d651e-104">語法</span><span class="sxs-lookup"><span data-stu-id="d651e-104">SYNTAX</span></span>

### <span data-ttu-id="d651e-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="d651e-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d651e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d651e-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d651e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d651e-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d651e-108">描述</span><span class="sxs-lookup"><span data-stu-id="d651e-108">DESCRIPTION</span></span>
<span data-ttu-id="d651e-109">Azure 資訊安全中心會自動探索安全性解決方案，請使用此 Cmdlet 來查看所發現的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d651e-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="d651e-110">例子</span><span class="sxs-lookup"><span data-stu-id="d651e-110">EXAMPLES</span></span>

### <span data-ttu-id="d651e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d651e-111">Example 1</span></span>
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

<span data-ttu-id="d651e-112">取得訂閱中所有已發現的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d651e-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="d651e-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="d651e-113">Example 2</span></span>
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

<span data-ttu-id="d651e-114">取得特定的已發現安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d651e-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="d651e-115">參數</span><span class="sxs-lookup"><span data-stu-id="d651e-115">PARAMETERS</span></span>

### <span data-ttu-id="d651e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d651e-116">-DefaultProfile</span></span>
<span data-ttu-id="d651e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d651e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d651e-118">-位置</span><span class="sxs-lookup"><span data-stu-id="d651e-118">-Location</span></span>
<span data-ttu-id="d651e-119">位置。</span><span class="sxs-lookup"><span data-stu-id="d651e-119">Location.</span></span>

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

### <span data-ttu-id="d651e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d651e-120">-Name</span></span>
<span data-ttu-id="d651e-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d651e-121">Resource name.</span></span>

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

### <span data-ttu-id="d651e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d651e-122">-ResourceGroupName</span></span>
<span data-ttu-id="d651e-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d651e-123">Resource group name.</span></span>

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

### <span data-ttu-id="d651e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d651e-124">-ResourceId</span></span>
<span data-ttu-id="d651e-125">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d651e-125">Resource ID.</span></span>

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

### <span data-ttu-id="d651e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d651e-126">CommonParameters</span></span>
<span data-ttu-id="d651e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d651e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d651e-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d651e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d651e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d651e-129">INPUTS</span></span>

### <span data-ttu-id="d651e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d651e-130">System.String</span></span>

## <span data-ttu-id="d651e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d651e-131">OUTPUTS</span></span>

### <span data-ttu-id="d651e-132">Microsoft.Azure.Commands.security.models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d651e-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="d651e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d651e-133">NOTES</span></span>

## <span data-ttu-id="d651e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d651e-134">RELATED LINKS</span></span>
