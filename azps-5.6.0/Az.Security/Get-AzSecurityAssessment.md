---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 5a8a09955158c21ff6d52e2327370c48448c12d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916494"
---
# <span data-ttu-id="e7ac0-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e7ac0-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="e7ac0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ac0-103">取得訂閱的安全性評定及其結果</span><span class="sxs-lookup"><span data-stu-id="e7ac0-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="e7ac0-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7ac0-104">SYNTAX</span></span>

### <span data-ttu-id="e7ac0-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="e7ac0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7ac0-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e7ac0-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7ac0-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e7ac0-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ac0-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ac0-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7ac0-109">描述</span><span class="sxs-lookup"><span data-stu-id="e7ac0-109">DESCRIPTION</span></span>
<span data-ttu-id="e7ac0-110">取得安全性評定及其訂閱結果。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="e7ac0-111">安全性評定會讓您知道 Azure 安全性中心會重新命令哪些最佳做法，以減輕 Azure 訂閱上的風險。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="e7ac0-112">例子</span><span class="sxs-lookup"><span data-stu-id="e7ac0-112">EXAMPLES</span></span>

### <span data-ttu-id="e7ac0-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="e7ac0-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="e7ac0-114">在訂閱中獲得所有安全性評定</span><span class="sxs-lookup"><span data-stu-id="e7ac0-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="e7ac0-115">參數</span><span class="sxs-lookup"><span data-stu-id="e7ac0-115">PARAMETERS</span></span>

### <span data-ttu-id="e7ac0-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ac0-116">-AssessedResourceId</span></span>
<span data-ttu-id="e7ac0-117">計算評定之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ac0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ac0-118">-DefaultProfile</span></span>
<span data-ttu-id="e7ac0-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ac0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7ac0-120">-Name</span></span>
<span data-ttu-id="e7ac0-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ac0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ac0-122">-ResourceId</span></span>
<span data-ttu-id="e7ac0-123">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e7ac0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ac0-124">CommonParameters</span></span>
<span data-ttu-id="e7ac0-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7ac0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ac0-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7ac0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ac0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e7ac0-127">INPUTS</span></span>

### <span data-ttu-id="e7ac0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e7ac0-128">System.String</span></span>

## <span data-ttu-id="e7ac0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e7ac0-129">OUTPUTS</span></span>

### <span data-ttu-id="e7ac0-130">Microsoft.Azure.Commands.Security.models.assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e7ac0-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="e7ac0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e7ac0-131">NOTES</span></span>

## <span data-ttu-id="e7ac0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7ac0-132">RELATED LINKS</span></span>
