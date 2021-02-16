---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130810"
---
# <span data-ttu-id="81187-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="81187-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="81187-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81187-102">SYNOPSIS</span></span>
<span data-ttu-id="81187-103">取得訂閱中的子評估結果。</span><span class="sxs-lookup"><span data-stu-id="81187-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="81187-104">句法</span><span class="sxs-lookup"><span data-stu-id="81187-104">SYNTAX</span></span>

### <span data-ttu-id="81187-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="81187-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81187-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="81187-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81187-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="81187-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81187-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="81187-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81187-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="81187-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81187-110">說明</span><span class="sxs-lookup"><span data-stu-id="81187-110">DESCRIPTION</span></span>
<span data-ttu-id="81187-111">取得訂閱中的子評估結果。</span><span class="sxs-lookup"><span data-stu-id="81187-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="81187-112">示例</span><span class="sxs-lookup"><span data-stu-id="81187-112">EXAMPLES</span></span>

### <span data-ttu-id="81187-113">範例1</span><span class="sxs-lookup"><span data-stu-id="81187-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="81187-114">取得訂閱中的所有子評估結果。</span><span class="sxs-lookup"><span data-stu-id="81187-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="81187-115">參數</span><span class="sxs-lookup"><span data-stu-id="81187-115">PARAMETERS</span></span>

### <span data-ttu-id="81187-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="81187-116">-AssessedResourceId</span></span>
<span data-ttu-id="81187-117">計算評估所依據之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="81187-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="81187-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="81187-118">-AssessmentName</span></span>
<span data-ttu-id="81187-119">評定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="81187-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="81187-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81187-120">-DefaultProfile</span></span>
<span data-ttu-id="81187-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81187-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81187-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="81187-122">-Name</span></span>
<span data-ttu-id="81187-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="81187-123">Resource name.</span></span>

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

### <span data-ttu-id="81187-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81187-124">-ResourceId</span></span>
<span data-ttu-id="81187-125">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="81187-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="81187-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81187-126">CommonParameters</span></span>
<span data-ttu-id="81187-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81187-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81187-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81187-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81187-129">輸入</span><span class="sxs-lookup"><span data-stu-id="81187-129">INPUTS</span></span>

### <span data-ttu-id="81187-130">System.object</span><span class="sxs-lookup"><span data-stu-id="81187-130">System.String</span></span>

## <span data-ttu-id="81187-131">輸出</span><span class="sxs-lookup"><span data-stu-id="81187-131">OUTPUTS</span></span>

### <span data-ttu-id="81187-132">PSSecuritySubAssessment 中的 SubAssessments （Security..。</span><span class="sxs-lookup"><span data-stu-id="81187-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="81187-133">筆記</span><span class="sxs-lookup"><span data-stu-id="81187-133">NOTES</span></span>

## <span data-ttu-id="81187-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="81187-134">RELATED LINKS</span></span>
