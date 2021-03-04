---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: c371749643952e8209b3cbec0721331a4d380d94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916889"
---
# <span data-ttu-id="2994d-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="2994d-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="2994d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2994d-102">SYNOPSIS</span></span>
<span data-ttu-id="2994d-103">取得訂閱中的子評定結果。</span><span class="sxs-lookup"><span data-stu-id="2994d-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="2994d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2994d-104">SYNTAX</span></span>

### <span data-ttu-id="2994d-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="2994d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2994d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2994d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2994d-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="2994d-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2994d-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="2994d-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2994d-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2994d-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2994d-110">描述</span><span class="sxs-lookup"><span data-stu-id="2994d-110">DESCRIPTION</span></span>
<span data-ttu-id="2994d-111">取得訂閱中的子評定結果。</span><span class="sxs-lookup"><span data-stu-id="2994d-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="2994d-112">例子</span><span class="sxs-lookup"><span data-stu-id="2994d-112">EXAMPLES</span></span>

### <span data-ttu-id="2994d-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="2994d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="2994d-114">取得訂閱中所有的子評定結果。</span><span class="sxs-lookup"><span data-stu-id="2994d-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="2994d-115">參數</span><span class="sxs-lookup"><span data-stu-id="2994d-115">PARAMETERS</span></span>

### <span data-ttu-id="2994d-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="2994d-116">-AssessedResourceId</span></span>
<span data-ttu-id="2994d-117">計算評定之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2994d-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994d-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="2994d-118">-AssessmentName</span></span>
<span data-ttu-id="2994d-119">評定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2994d-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2994d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2994d-120">-DefaultProfile</span></span>
<span data-ttu-id="2994d-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2994d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2994d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2994d-122">-Name</span></span>
<span data-ttu-id="2994d-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2994d-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2994d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2994d-124">-ResourceId</span></span>
<span data-ttu-id="2994d-125">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2994d-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2994d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2994d-126">CommonParameters</span></span>
<span data-ttu-id="2994d-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2994d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2994d-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2994d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2994d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2994d-129">INPUTS</span></span>

### <span data-ttu-id="2994d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2994d-130">System.String</span></span>

## <span data-ttu-id="2994d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2994d-131">OUTPUTS</span></span>

### <span data-ttu-id="2994d-132">Microsoft.Azure.Commands.Security.models.SubAssessments.PSSecuritySubAssesment</span><span class="sxs-lookup"><span data-stu-id="2994d-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="2994d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2994d-133">NOTES</span></span>

## <span data-ttu-id="2994d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2994d-134">RELATED LINKS</span></span>
