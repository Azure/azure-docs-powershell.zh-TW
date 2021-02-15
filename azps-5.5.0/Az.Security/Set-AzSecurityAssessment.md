---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142537"
---
# <span data-ttu-id="a8682-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a8682-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="a8682-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8682-102">SYNOPSIS</span></span>
<span data-ttu-id="a8682-103">建立或更新資源的安全性評定結果</span><span class="sxs-lookup"><span data-stu-id="a8682-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="a8682-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8682-104">SYNTAX</span></span>

### <span data-ttu-id="a8682-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a8682-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8682-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="a8682-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8682-107">說明</span><span class="sxs-lookup"><span data-stu-id="a8682-107">DESCRIPTION</span></span>
<span data-ttu-id="a8682-108">建立或更新資源的安全性評定結果，可以用來變更現有結果的狀態或新增其他資料。</span><span class="sxs-lookup"><span data-stu-id="a8682-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="a8682-109">只能用於「CustomerManaged」評定類型，而且只能在建立了相符的評定中繼資料之後才能使用。</span><span class="sxs-lookup"><span data-stu-id="a8682-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="a8682-110">示例</span><span class="sxs-lookup"><span data-stu-id="a8682-110">EXAMPLES</span></span>

### <span data-ttu-id="a8682-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a8682-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="a8682-112">將訂閱結果標示為「不健康」，以便評估類型「4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D」-評定類型的詳細資料會在 assessmentMetadata 類型下找到。</span><span class="sxs-lookup"><span data-stu-id="a8682-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="a8682-113">參數</span><span class="sxs-lookup"><span data-stu-id="a8682-113">PARAMETERS</span></span>

### <span data-ttu-id="a8682-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="a8682-114">-AdditionalData</span></span>
<span data-ttu-id="a8682-115">附加至評定結果的資料，以獲得更佳的調查或狀態明晰性。</span><span class="sxs-lookup"><span data-stu-id="a8682-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

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

### <span data-ttu-id="a8682-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a8682-116">-AssessedResourceId</span></span>
<span data-ttu-id="a8682-117">計算評估所依據之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8682-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="a8682-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8682-118">-DefaultProfile</span></span>
<span data-ttu-id="a8682-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8682-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8682-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8682-120">-Name</span></span>
<span data-ttu-id="a8682-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a8682-121">Resource name.</span></span>

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

### <span data-ttu-id="a8682-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="a8682-122">-StatusCause</span></span>
<span data-ttu-id="a8682-123">Progremmatic 評估結果原因的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a8682-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="a8682-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a8682-124">-StatusCode</span></span>
<span data-ttu-id="a8682-125">評定結果的 Progremmatic 代碼。</span><span class="sxs-lookup"><span data-stu-id="a8682-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="a8682-126">可以是「健康」、「不健康」或「NotApplicable」</span><span class="sxs-lookup"><span data-stu-id="a8682-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

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

### <span data-ttu-id="a8682-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="a8682-127">-StatusDescription</span></span>
<span data-ttu-id="a8682-128">針對評定結果之原因的人可供閱讀的描述。</span><span class="sxs-lookup"><span data-stu-id="a8682-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="a8682-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a8682-129">-Confirm</span></span>
<span data-ttu-id="a8682-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8682-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8682-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8682-131">-WhatIf</span></span>
<span data-ttu-id="a8682-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8682-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8682-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8682-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8682-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8682-134">CommonParameters</span></span>
<span data-ttu-id="a8682-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8682-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8682-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a8682-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8682-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a8682-137">INPUTS</span></span>

### <span data-ttu-id="a8682-138">所有</span><span class="sxs-lookup"><span data-stu-id="a8682-138">None</span></span>

## <span data-ttu-id="a8682-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a8682-139">OUTPUTS</span></span>

### <span data-ttu-id="a8682-140">PSSecurityAssessment （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="a8682-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="a8682-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a8682-141">NOTES</span></span>

## <span data-ttu-id="a8682-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8682-142">RELATED LINKS</span></span>
