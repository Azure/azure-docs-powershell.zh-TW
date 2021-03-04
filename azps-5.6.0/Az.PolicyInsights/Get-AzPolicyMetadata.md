---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911381"
---
# <span data-ttu-id="15c1d-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="15c1d-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="15c1d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="15c1d-103">獲得策略中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="15c1d-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="15c1d-104">語法</span><span class="sxs-lookup"><span data-stu-id="15c1d-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15c1d-105">描述</span><span class="sxs-lookup"><span data-stu-id="15c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="15c1d-106">**Get-AzPolicyRemediation** Cmdlet 會取得所有政策中繼資料資源或特定的策略中繼資料資源。</span><span class="sxs-lookup"><span data-stu-id="15c1d-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="15c1d-107">例子</span><span class="sxs-lookup"><span data-stu-id="15c1d-107">EXAMPLES</span></span>

### <span data-ttu-id="15c1d-108">範例 1：取得所有策略中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="15c1d-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="15c1d-109">此命令會獲得所有政策中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="15c1d-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="15c1d-110">範例 2：取得 10 個策略中繼資料資源的集合</span><span class="sxs-lookup"><span data-stu-id="15c1d-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="15c1d-111">此命令會收集 10 個策略中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="15c1d-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="15c1d-112">範例 3：取得名稱為 'ACF1348' 的單一策略中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="15c1d-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="15c1d-113">此命令會獲得名稱為 "ACF1348" 的單一策略中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="15c1d-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="15c1d-114">參數</span><span class="sxs-lookup"><span data-stu-id="15c1d-114">PARAMETERS</span></span>

### <span data-ttu-id="15c1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c1d-115">-DefaultProfile</span></span>
<span data-ttu-id="15c1d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15c1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c1d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="15c1d-117">-Name</span></span>
<span data-ttu-id="15c1d-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="15c1d-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15c1d-119">-頂端</span><span class="sxs-lookup"><span data-stu-id="15c1d-119">-Top</span></span>
<span data-ttu-id="15c1d-120">要返回之策略中繼資料資源的數量上限。</span><span class="sxs-lookup"><span data-stu-id="15c1d-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c1d-121">CommonParameters</span></span>
<span data-ttu-id="15c1d-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15c1d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c1d-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15c1d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c1d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="15c1d-124">INPUTS</span></span>

### <span data-ttu-id="15c1d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="15c1d-125">System.String</span></span>

## <span data-ttu-id="15c1d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="15c1d-126">OUTPUTS</span></span>

### <span data-ttu-id="15c1d-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="15c1d-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="15c1d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="15c1d-128">NOTES</span></span>

## <span data-ttu-id="15c1d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="15c1d-129">RELATED LINKS</span></span>
