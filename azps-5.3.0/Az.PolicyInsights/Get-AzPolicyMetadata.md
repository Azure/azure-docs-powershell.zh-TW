---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435687"
---
# <span data-ttu-id="ebe51-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="ebe51-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="ebe51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebe51-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe51-103">取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="ebe51-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="ebe51-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebe51-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebe51-105">說明</span><span class="sxs-lookup"><span data-stu-id="ebe51-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe51-106">**AzPolicyRemediation** Cmdlet 會取得所有原則中繼資料資源或特定的原則中繼資料資源。</span><span class="sxs-lookup"><span data-stu-id="ebe51-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="ebe51-107">示例</span><span class="sxs-lookup"><span data-stu-id="ebe51-107">EXAMPLES</span></span>

### <span data-ttu-id="ebe51-108">範例1：取得所有原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="ebe51-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="ebe51-109">這個命令會取得所有原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="ebe51-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="ebe51-110">範例2：取得10個原則中繼資料資源的集合</span><span class="sxs-lookup"><span data-stu-id="ebe51-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="ebe51-111">這個命令會取得10個原則中繼資料資源的集合</span><span class="sxs-lookup"><span data-stu-id="ebe51-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="ebe51-112">範例3：取得名為「ACF1348」的單一原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="ebe51-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="ebe51-113">這個命令會取得名為「ACF1348」的單一原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="ebe51-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="ebe51-114">參數</span><span class="sxs-lookup"><span data-stu-id="ebe51-114">PARAMETERS</span></span>

### <span data-ttu-id="ebe51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe51-115">-DefaultProfile</span></span>
<span data-ttu-id="ebe51-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebe51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebe51-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ebe51-117">-Name</span></span>
<span data-ttu-id="ebe51-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ebe51-118">Resource name.</span></span>

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

### <span data-ttu-id="ebe51-119">-上方</span><span class="sxs-lookup"><span data-stu-id="ebe51-119">-Top</span></span>
<span data-ttu-id="ebe51-120">要傳回的原則中繼資料資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="ebe51-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="ebe51-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe51-121">CommonParameters</span></span>
<span data-ttu-id="ebe51-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebe51-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe51-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ebe51-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe51-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ebe51-124">INPUTS</span></span>

### <span data-ttu-id="ebe51-125">System.object</span><span class="sxs-lookup"><span data-stu-id="ebe51-125">System.String</span></span>

## <span data-ttu-id="ebe51-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ebe51-126">OUTPUTS</span></span>

### <span data-ttu-id="ebe51-127">PSPolicyMetadata 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="ebe51-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="ebe51-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ebe51-128">NOTES</span></span>

## <span data-ttu-id="ebe51-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebe51-129">RELATED LINKS</span></span>
