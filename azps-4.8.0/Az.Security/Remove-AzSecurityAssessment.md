---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129912"
---
# <span data-ttu-id="6c0b3-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="6c0b3-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="6c0b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c0b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0b3-103">從訂閱中刪除安全性評定結果。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="6c0b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c0b3-104">SYNTAX</span></span>

### <span data-ttu-id="6c0b3-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="6c0b3-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0b3-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="6c0b3-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0b3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c0b3-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0b3-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="6c0b3-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c0b3-109">說明</span><span class="sxs-lookup"><span data-stu-id="6c0b3-109">DESCRIPTION</span></span>
<span data-ttu-id="6c0b3-110">從訂閱中刪除安全性評定結果，通常是在刪除 resoruce 或評估不與特定資源相關時使用</span><span class="sxs-lookup"><span data-stu-id="6c0b3-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="6c0b3-111">示例</span><span class="sxs-lookup"><span data-stu-id="6c0b3-111">EXAMPLES</span></span>

### <span data-ttu-id="6c0b3-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6c0b3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="6c0b3-113">刪除訂閱上的評定結果</span><span class="sxs-lookup"><span data-stu-id="6c0b3-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="6c0b3-114">參數</span><span class="sxs-lookup"><span data-stu-id="6c0b3-114">PARAMETERS</span></span>

### <span data-ttu-id="6c0b3-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="6c0b3-115">-AssessedResourceId</span></span>
<span data-ttu-id="6c0b3-116">計算評估所依據之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="6c0b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0b3-117">-DefaultProfile</span></span>
<span data-ttu-id="6c0b3-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c0b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c0b3-119">-InputObject</span></span>
<span data-ttu-id="6c0b3-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-120">Input Object.</span></span>

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

### <span data-ttu-id="6c0b3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c0b3-121">-Name</span></span>
<span data-ttu-id="6c0b3-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-122">Resource name.</span></span>

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

### <span data-ttu-id="6c0b3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c0b3-123">-PassThru</span></span>
<span data-ttu-id="6c0b3-124">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="6c0b3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c0b3-125">-ResourceId</span></span>
<span data-ttu-id="6c0b3-126">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="6c0b3-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6c0b3-127">-Confirm</span></span>
<span data-ttu-id="6c0b3-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0b3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0b3-129">-WhatIf</span></span>
<span data-ttu-id="6c0b3-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0b3-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0b3-132">CommonParameters</span></span>
<span data-ttu-id="6c0b3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0b3-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0b3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6c0b3-135">INPUTS</span></span>

### <span data-ttu-id="6c0b3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="6c0b3-136">System.String</span></span>

### <span data-ttu-id="6c0b3-137">PSSecurityAssessment （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="6c0b3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6c0b3-138">OUTPUTS</span></span>

### <span data-ttu-id="6c0b3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="6c0b3-139">System.Boolean</span></span>

## <span data-ttu-id="6c0b3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6c0b3-140">NOTES</span></span>

## <span data-ttu-id="6c0b3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c0b3-141">RELATED LINKS</span></span>
