---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 5bf841e055c81293d6f2f9c5811ad4e1aa1a2f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915894"
---
# <span data-ttu-id="34f62-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="34f62-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="34f62-102">簡介</span><span class="sxs-lookup"><span data-stu-id="34f62-102">SYNOPSIS</span></span>
<span data-ttu-id="34f62-103">建立或更新資源上的安全性評定結果</span><span class="sxs-lookup"><span data-stu-id="34f62-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="34f62-104">語法</span><span class="sxs-lookup"><span data-stu-id="34f62-104">SYNTAX</span></span>

### <span data-ttu-id="34f62-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="34f62-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34f62-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="34f62-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f62-107">描述</span><span class="sxs-lookup"><span data-stu-id="34f62-107">DESCRIPTION</span></span>
<span data-ttu-id="34f62-108">在資源上建立或更新安全性評定結果，可用來變更現有結果的狀態或新增其他資料。</span><span class="sxs-lookup"><span data-stu-id="34f62-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="34f62-109">只能用於「CustomerManaged」評定類型，而且只能在建立相符的評定中繼資料之後使用。</span><span class="sxs-lookup"><span data-stu-id="34f62-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="34f62-110">例子</span><span class="sxs-lookup"><span data-stu-id="34f62-110">EXAMPLES</span></span>

### <span data-ttu-id="34f62-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="34f62-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="34f62-112">將訂閱結果標記為「不健康」，以評定類型 "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - 評估Metadata 類型下會找到評定類型的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="34f62-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="34f62-113">參數</span><span class="sxs-lookup"><span data-stu-id="34f62-113">PARAMETERS</span></span>

### <span data-ttu-id="34f62-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="34f62-114">-AdditionalData</span></span>
<span data-ttu-id="34f62-115">附加至評定結果的資料，可改善調查或狀態明確性。</span><span class="sxs-lookup"><span data-stu-id="34f62-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f62-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="34f62-116">-AssessedResourceId</span></span>
<span data-ttu-id="34f62-117">計算評定之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="34f62-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="34f62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f62-118">-DefaultProfile</span></span>
<span data-ttu-id="34f62-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="34f62-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f62-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="34f62-120">-Name</span></span>
<span data-ttu-id="34f62-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="34f62-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f62-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="34f62-122">-StatusCause</span></span>
<span data-ttu-id="34f62-123">評估結果原因的 Progremmatic 程式碼。</span><span class="sxs-lookup"><span data-stu-id="34f62-123">Progremmatic code for the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f62-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="34f62-124">-StatusCode</span></span>
<span data-ttu-id="34f62-125">評估結果的 Progremmatic 程式碼。</span><span class="sxs-lookup"><span data-stu-id="34f62-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="34f62-126">可以是「健康」、「不健康」或「不適用」</span><span class="sxs-lookup"><span data-stu-id="34f62-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
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

### <span data-ttu-id="34f62-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="34f62-127">-StatusDescription</span></span>
<span data-ttu-id="34f62-128">評估結果原因的可讀描述。</span><span class="sxs-lookup"><span data-stu-id="34f62-128">Human readable description of the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f62-129">-確認</span><span class="sxs-lookup"><span data-stu-id="34f62-129">-Confirm</span></span>
<span data-ttu-id="34f62-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="34f62-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f62-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f62-131">-WhatIf</span></span>
<span data-ttu-id="34f62-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34f62-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f62-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34f62-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f62-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f62-134">CommonParameters</span></span>
<span data-ttu-id="34f62-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="34f62-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f62-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34f62-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f62-137">輸入</span><span class="sxs-lookup"><span data-stu-id="34f62-137">INPUTS</span></span>

### <span data-ttu-id="34f62-138">沒有</span><span class="sxs-lookup"><span data-stu-id="34f62-138">None</span></span>

## <span data-ttu-id="34f62-139">輸出</span><span class="sxs-lookup"><span data-stu-id="34f62-139">OUTPUTS</span></span>

### <span data-ttu-id="34f62-140">Microsoft.Azure.Commands.Security.models.assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="34f62-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="34f62-141">筆記</span><span class="sxs-lookup"><span data-stu-id="34f62-141">NOTES</span></span>

## <span data-ttu-id="34f62-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="34f62-142">RELATED LINKS</span></span>
