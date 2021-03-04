---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: daa0d87eab24743863e6cbbcdd1c010e974c113c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907506"
---
# <span data-ttu-id="3852e-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3852e-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="3852e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3852e-102">SYNOPSIS</span></span>
<span data-ttu-id="3852e-103">刪除訂閱的安全性評定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3852e-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="3852e-104">語法</span><span class="sxs-lookup"><span data-stu-id="3852e-104">SYNTAX</span></span>

### <span data-ttu-id="3852e-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="3852e-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3852e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3852e-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3852e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3852e-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3852e-108">描述</span><span class="sxs-lookup"><span data-stu-id="3852e-108">DESCRIPTION</span></span>
<span data-ttu-id="3852e-109">刪除訂閱的安全性評定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3852e-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="3852e-110">此動作會從訂閱中刪除評定類型及所有相關評定結果。</span><span class="sxs-lookup"><span data-stu-id="3852e-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="3852e-111">例子</span><span class="sxs-lookup"><span data-stu-id="3852e-111">EXAMPLES</span></span>

### <span data-ttu-id="3852e-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="3852e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="3852e-113">從訂閱中刪除評定類型</span><span class="sxs-lookup"><span data-stu-id="3852e-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="3852e-114">參數</span><span class="sxs-lookup"><span data-stu-id="3852e-114">PARAMETERS</span></span>

### <span data-ttu-id="3852e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3852e-115">-DefaultProfile</span></span>
<span data-ttu-id="3852e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3852e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3852e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3852e-117">-InputObject</span></span>
<span data-ttu-id="3852e-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="3852e-118">Input Object.</span></span>

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

### <span data-ttu-id="3852e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3852e-119">-Name</span></span>
<span data-ttu-id="3852e-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3852e-120">Resource name.</span></span>

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

### <span data-ttu-id="3852e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3852e-121">-PassThru</span></span>
<span data-ttu-id="3852e-122">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="3852e-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="3852e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3852e-123">-ResourceId</span></span>
<span data-ttu-id="3852e-124">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3852e-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3852e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="3852e-125">-Confirm</span></span>
<span data-ttu-id="3852e-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3852e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3852e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3852e-127">-WhatIf</span></span>
<span data-ttu-id="3852e-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3852e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3852e-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3852e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3852e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3852e-130">CommonParameters</span></span>
<span data-ttu-id="3852e-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3852e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3852e-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3852e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3852e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3852e-133">INPUTS</span></span>

### <span data-ttu-id="3852e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3852e-134">System.String</span></span>

### <span data-ttu-id="3852e-135">Microsoft.Azure.Commands.Security.models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3852e-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="3852e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3852e-136">OUTPUTS</span></span>

### <span data-ttu-id="3852e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3852e-137">System.Boolean</span></span>

## <span data-ttu-id="3852e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3852e-138">NOTES</span></span>

## <span data-ttu-id="3852e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3852e-139">RELATED LINKS</span></span>
