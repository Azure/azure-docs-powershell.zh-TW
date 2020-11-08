---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138175"
---
# <span data-ttu-id="c0f0c-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="c0f0c-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="c0f0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f0c-103">從訂閱中刪除安全性評定結果。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="c0f0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0f0c-104">SYNTAX</span></span>

### <span data-ttu-id="c0f0c-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c0f0c-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0f0c-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="c0f0c-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0f0c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0f0c-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0f0c-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="c0f0c-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0f0c-109">說明</span><span class="sxs-lookup"><span data-stu-id="c0f0c-109">DESCRIPTION</span></span>
<span data-ttu-id="c0f0c-110">從訂閱中刪除安全性評定結果，通常是在刪除 resoruce 或評估不與特定資源相關時使用</span><span class="sxs-lookup"><span data-stu-id="c0f0c-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="c0f0c-111">示例</span><span class="sxs-lookup"><span data-stu-id="c0f0c-111">EXAMPLES</span></span>

### <span data-ttu-id="c0f0c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c0f0c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="c0f0c-113">刪除訂閱上的評定結果</span><span class="sxs-lookup"><span data-stu-id="c0f0c-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="c0f0c-114">參數</span><span class="sxs-lookup"><span data-stu-id="c0f0c-114">PARAMETERS</span></span>

### <span data-ttu-id="c0f0c-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="c0f0c-115">-AssessedResourceId</span></span>
<span data-ttu-id="c0f0c-116">計算評估所依據之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="c0f0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f0c-117">-DefaultProfile</span></span>
<span data-ttu-id="c0f0c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0f0c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0f0c-119">-InputObject</span></span>
<span data-ttu-id="c0f0c-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-120">Input Object.</span></span>

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

### <span data-ttu-id="c0f0c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0f0c-121">-Name</span></span>
<span data-ttu-id="c0f0c-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-122">Resource name.</span></span>

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

### <span data-ttu-id="c0f0c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0f0c-123">-PassThru</span></span>
<span data-ttu-id="c0f0c-124">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="c0f0c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0f0c-125">-ResourceId</span></span>
<span data-ttu-id="c0f0c-126">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c0f0c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c0f0c-127">-Confirm</span></span>
<span data-ttu-id="c0f0c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0f0c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0f0c-129">-WhatIf</span></span>
<span data-ttu-id="c0f0c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0f0c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0f0c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f0c-132">CommonParameters</span></span>
<span data-ttu-id="c0f0c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f0c-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f0c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c0f0c-135">INPUTS</span></span>

### <span data-ttu-id="c0f0c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c0f0c-136">System.String</span></span>

### <span data-ttu-id="c0f0c-137">PSSecurityAssessment （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="c0f0c-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="c0f0c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c0f0c-138">OUTPUTS</span></span>

### <span data-ttu-id="c0f0c-139">System.object</span><span class="sxs-lookup"><span data-stu-id="c0f0c-139">System.Boolean</span></span>

## <span data-ttu-id="c0f0c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c0f0c-140">NOTES</span></span>

## <span data-ttu-id="c0f0c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0f0c-141">RELATED LINKS</span></span>