---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: ff69cd6296dbd95f959beb48fef6e496866e54f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916887"
---
# <span data-ttu-id="0d247-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="0d247-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="0d247-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0d247-102">SYNOPSIS</span></span>
<span data-ttu-id="0d247-103">刪除訂閱的安全性評定結果。</span><span class="sxs-lookup"><span data-stu-id="0d247-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="0d247-104">語法</span><span class="sxs-lookup"><span data-stu-id="0d247-104">SYNTAX</span></span>

### <span data-ttu-id="0d247-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="0d247-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d247-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="0d247-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d247-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d247-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d247-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="0d247-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d247-109">描述</span><span class="sxs-lookup"><span data-stu-id="0d247-109">DESCRIPTION</span></span>
<span data-ttu-id="0d247-110">從訂閱中刪除安全性評定結果，通常是在刪除資源或評定不再與特定資源相關時使用</span><span class="sxs-lookup"><span data-stu-id="0d247-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="0d247-111">例子</span><span class="sxs-lookup"><span data-stu-id="0d247-111">EXAMPLES</span></span>

### <span data-ttu-id="0d247-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0d247-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="0d247-113">刪除訂閱上的評定結果</span><span class="sxs-lookup"><span data-stu-id="0d247-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="0d247-114">參數</span><span class="sxs-lookup"><span data-stu-id="0d247-114">PARAMETERS</span></span>

### <span data-ttu-id="0d247-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="0d247-115">-AssessedResourceId</span></span>
<span data-ttu-id="0d247-116">計算評定之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d247-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d247-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d247-117">-DefaultProfile</span></span>
<span data-ttu-id="0d247-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d247-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d247-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d247-119">-InputObject</span></span>
<span data-ttu-id="0d247-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0d247-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d247-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d247-121">-Name</span></span>
<span data-ttu-id="0d247-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0d247-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d247-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d247-123">-PassThru</span></span>
<span data-ttu-id="0d247-124">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="0d247-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="0d247-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d247-125">-ResourceId</span></span>
<span data-ttu-id="0d247-126">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d247-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0d247-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0d247-127">-Confirm</span></span>
<span data-ttu-id="0d247-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0d247-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d247-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d247-129">-WhatIf</span></span>
<span data-ttu-id="0d247-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d247-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d247-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d247-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d247-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d247-132">CommonParameters</span></span>
<span data-ttu-id="0d247-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0d247-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d247-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d247-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d247-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0d247-135">INPUTS</span></span>

### <span data-ttu-id="0d247-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0d247-136">System.String</span></span>

### <span data-ttu-id="0d247-137">Microsoft.Azure.Commands.Security.models.assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="0d247-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="0d247-138">輸出</span><span class="sxs-lookup"><span data-stu-id="0d247-138">OUTPUTS</span></span>

### <span data-ttu-id="0d247-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d247-139">System.Boolean</span></span>

## <span data-ttu-id="0d247-140">筆記</span><span class="sxs-lookup"><span data-stu-id="0d247-140">NOTES</span></span>

## <span data-ttu-id="0d247-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d247-141">RELATED LINKS</span></span>
