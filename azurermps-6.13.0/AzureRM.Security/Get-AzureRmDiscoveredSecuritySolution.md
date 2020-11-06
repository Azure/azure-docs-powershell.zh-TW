---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448230"
---
# <span data-ttu-id="0a0e0-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0a0e0-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="0a0e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0e0-103">取得由 Azure 安全中心探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="0a0e0-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a0e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a0e0-104">SYNTAX</span></span>

### <span data-ttu-id="0a0e0-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="0a0e0-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a0e0-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0a0e0-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a0e0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a0e0-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a0e0-108">說明</span><span class="sxs-lookup"><span data-stu-id="0a0e0-108">DESCRIPTION</span></span>
<span data-ttu-id="0a0e0-109">安全性解決方案是由 Azure 安全中心自動探索，使用此 Cmdlet 來查看已探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="0a0e0-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="0a0e0-110">示例</span><span class="sxs-lookup"><span data-stu-id="0a0e0-110">EXAMPLES</span></span>

### <span data-ttu-id="0a0e0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0a0e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="0a0e0-112">取得訂閱中所有已探索的安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="0a0e0-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="0a0e0-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0a0e0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="0a0e0-114">取得特定的安全解決方案</span><span class="sxs-lookup"><span data-stu-id="0a0e0-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="0a0e0-115">參數</span><span class="sxs-lookup"><span data-stu-id="0a0e0-115">PARAMETERS</span></span>

### <span data-ttu-id="0a0e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0e0-116">-DefaultProfile</span></span>
<span data-ttu-id="0a0e0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a0e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a0e0-118">-位置</span><span class="sxs-lookup"><span data-stu-id="0a0e0-118">-Location</span></span>
<span data-ttu-id="0a0e0-119">位於.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0e0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a0e0-120">-Name</span></span>
<span data-ttu-id="0a0e0-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0e0-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a0e0-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0e0-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0e0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a0e0-124">-ResourceId</span></span>
<span data-ttu-id="0a0e0-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0a0e0-125">Resource ID.</span></span>

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

### <span data-ttu-id="0a0e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0e0-126">CommonParameters</span></span>
<span data-ttu-id="0a0e0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a0e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0e0-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a0e0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0e0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0a0e0-129">INPUTS</span></span>

### <span data-ttu-id="0a0e0-130">System.object</span><span class="sxs-lookup"><span data-stu-id="0a0e0-130">System.String</span></span>

## <span data-ttu-id="0a0e0-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0a0e0-131">OUTPUTS</span></span>

### <span data-ttu-id="0a0e0-132">PSSecurityDiscoveredSecuritySolution 中的 DiscoveredSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="0a0e0-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="0a0e0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0a0e0-133">NOTES</span></span>

## <span data-ttu-id="0a0e0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a0e0-134">RELATED LINKS</span></span>
