---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448643"
---
# <span data-ttu-id="e5266-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="e5266-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="e5266-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5266-102">SYNOPSIS</span></span>
<span data-ttu-id="e5266-103">從訂閱中刪除安全性評定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e5266-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="e5266-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5266-104">SYNTAX</span></span>

### <span data-ttu-id="e5266-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e5266-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5266-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5266-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5266-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e5266-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5266-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5266-108">DESCRIPTION</span></span>
<span data-ttu-id="e5266-109">從訂閱中刪除安全性評定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e5266-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="e5266-110">這個動作將會從訂閱中刪除評定類型及所有相關評估結果。</span><span class="sxs-lookup"><span data-stu-id="e5266-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="e5266-111">示例</span><span class="sxs-lookup"><span data-stu-id="e5266-111">EXAMPLES</span></span>

### <span data-ttu-id="e5266-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e5266-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="e5266-113">從訂閱中刪除評定類型</span><span class="sxs-lookup"><span data-stu-id="e5266-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="e5266-114">參數</span><span class="sxs-lookup"><span data-stu-id="e5266-114">PARAMETERS</span></span>

### <span data-ttu-id="e5266-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5266-115">-DefaultProfile</span></span>
<span data-ttu-id="e5266-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5266-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5266-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5266-117">-InputObject</span></span>
<span data-ttu-id="e5266-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="e5266-118">Input Object.</span></span>

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

### <span data-ttu-id="e5266-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5266-119">-Name</span></span>
<span data-ttu-id="e5266-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e5266-120">Resource name.</span></span>

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

### <span data-ttu-id="e5266-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5266-121">-PassThru</span></span>
<span data-ttu-id="e5266-122">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="e5266-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="e5266-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5266-123">-ResourceId</span></span>
<span data-ttu-id="e5266-124">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5266-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e5266-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e5266-125">-Confirm</span></span>
<span data-ttu-id="e5266-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5266-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5266-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5266-127">-WhatIf</span></span>
<span data-ttu-id="e5266-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5266-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5266-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5266-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5266-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5266-130">CommonParameters</span></span>
<span data-ttu-id="e5266-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5266-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5266-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5266-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5266-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e5266-133">INPUTS</span></span>

### <span data-ttu-id="e5266-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e5266-134">System.String</span></span>

### <span data-ttu-id="e5266-135">PSSecurityAssessmentMetadata 中的 AssessmentMetadata （Security..。</span><span class="sxs-lookup"><span data-stu-id="e5266-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="e5266-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e5266-136">OUTPUTS</span></span>

### <span data-ttu-id="e5266-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e5266-137">System.Boolean</span></span>

## <span data-ttu-id="e5266-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e5266-138">NOTES</span></span>

## <span data-ttu-id="e5266-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5266-139">RELATED LINKS</span></span>
