---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285943"
---
# <span data-ttu-id="af80c-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="af80c-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="af80c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af80c-102">SYNOPSIS</span></span>
<span data-ttu-id="af80c-103">取得由 Azure 安全中心探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="af80c-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="af80c-104">句法</span><span class="sxs-lookup"><span data-stu-id="af80c-104">SYNTAX</span></span>

### <span data-ttu-id="af80c-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="af80c-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af80c-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="af80c-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af80c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af80c-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af80c-108">說明</span><span class="sxs-lookup"><span data-stu-id="af80c-108">DESCRIPTION</span></span>
<span data-ttu-id="af80c-109">安全性解決方案是由 Azure 安全中心自動探索，使用此 Cmdlet 來查看已探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="af80c-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="af80c-110">示例</span><span class="sxs-lookup"><span data-stu-id="af80c-110">EXAMPLES</span></span>

### <span data-ttu-id="af80c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="af80c-111">Example 1</span></span>
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

<span data-ttu-id="af80c-112">取得訂閱中所有已探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="af80c-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="af80c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="af80c-113">Example 2</span></span>
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

<span data-ttu-id="af80c-114">取得特定的安全解決方案</span><span class="sxs-lookup"><span data-stu-id="af80c-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="af80c-115">參數</span><span class="sxs-lookup"><span data-stu-id="af80c-115">PARAMETERS</span></span>

### <span data-ttu-id="af80c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af80c-116">-DefaultProfile</span></span>
<span data-ttu-id="af80c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af80c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af80c-118">-位置</span><span class="sxs-lookup"><span data-stu-id="af80c-118">-Location</span></span>
<span data-ttu-id="af80c-119">位於.</span><span class="sxs-lookup"><span data-stu-id="af80c-119">Location.</span></span>

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

### <span data-ttu-id="af80c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="af80c-120">-Name</span></span>
<span data-ttu-id="af80c-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="af80c-121">Resource name.</span></span>

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

### <span data-ttu-id="af80c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af80c-122">-ResourceGroupName</span></span>
<span data-ttu-id="af80c-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="af80c-123">Resource group name.</span></span>

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

### <span data-ttu-id="af80c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af80c-124">-ResourceId</span></span>
<span data-ttu-id="af80c-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="af80c-125">Resource ID.</span></span>

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

### <span data-ttu-id="af80c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af80c-126">CommonParameters</span></span>
<span data-ttu-id="af80c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af80c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af80c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af80c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af80c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="af80c-129">INPUTS</span></span>

### <span data-ttu-id="af80c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="af80c-130">System.String</span></span>

## <span data-ttu-id="af80c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="af80c-131">OUTPUTS</span></span>

### <span data-ttu-id="af80c-132">PSSecurityDiscoveredSecuritySolution 中的 DiscoveredSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="af80c-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="af80c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="af80c-133">NOTES</span></span>

## <span data-ttu-id="af80c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="af80c-134">RELATED LINKS</span></span>
