---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138174"
---
# <span data-ttu-id="eb8ee-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="eb8ee-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="eb8ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8ee-103">從訂閱中刪除安全性評定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="eb8ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb8ee-104">SYNTAX</span></span>

### <span data-ttu-id="eb8ee-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="eb8ee-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8ee-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb8ee-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8ee-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="eb8ee-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb8ee-108">說明</span><span class="sxs-lookup"><span data-stu-id="eb8ee-108">DESCRIPTION</span></span>
<span data-ttu-id="eb8ee-109">從訂閱中刪除安全性評定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="eb8ee-110">這個動作將會從訂閱中刪除評定類型及所有相關評估結果。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="eb8ee-111">示例</span><span class="sxs-lookup"><span data-stu-id="eb8ee-111">EXAMPLES</span></span>

### <span data-ttu-id="eb8ee-112">範例1</span><span class="sxs-lookup"><span data-stu-id="eb8ee-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="eb8ee-113">從訂閱中刪除評定類型</span><span class="sxs-lookup"><span data-stu-id="eb8ee-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="eb8ee-114">參數</span><span class="sxs-lookup"><span data-stu-id="eb8ee-114">PARAMETERS</span></span>

### <span data-ttu-id="eb8ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8ee-115">-DefaultProfile</span></span>
<span data-ttu-id="eb8ee-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb8ee-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb8ee-117">-InputObject</span></span>
<span data-ttu-id="eb8ee-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8ee-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb8ee-119">-Name</span></span>
<span data-ttu-id="eb8ee-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-120">Resource name.</span></span>

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

### <span data-ttu-id="eb8ee-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb8ee-121">-PassThru</span></span>
<span data-ttu-id="eb8ee-122">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-122">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8ee-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb8ee-123">-ResourceId</span></span>
<span data-ttu-id="eb8ee-124">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="eb8ee-125">-確認</span><span class="sxs-lookup"><span data-stu-id="eb8ee-125">-Confirm</span></span>
<span data-ttu-id="eb8ee-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8ee-127">-WhatIf</span></span>
<span data-ttu-id="eb8ee-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb8ee-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8ee-130">CommonParameters</span></span>
<span data-ttu-id="eb8ee-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8ee-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8ee-133">輸入</span><span class="sxs-lookup"><span data-stu-id="eb8ee-133">INPUTS</span></span>

### <span data-ttu-id="eb8ee-134">System.object</span><span class="sxs-lookup"><span data-stu-id="eb8ee-134">System.String</span></span>

### <span data-ttu-id="eb8ee-135">PSSecurityAssessmentMetadata 中的 AssessmentMetadata （Security..。</span><span class="sxs-lookup"><span data-stu-id="eb8ee-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="eb8ee-136">輸出</span><span class="sxs-lookup"><span data-stu-id="eb8ee-136">OUTPUTS</span></span>

### <span data-ttu-id="eb8ee-137">System.object</span><span class="sxs-lookup"><span data-stu-id="eb8ee-137">System.Boolean</span></span>

## <span data-ttu-id="eb8ee-138">筆記</span><span class="sxs-lookup"><span data-stu-id="eb8ee-138">NOTES</span></span>

## <span data-ttu-id="eb8ee-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb8ee-139">RELATED LINKS</span></span>
