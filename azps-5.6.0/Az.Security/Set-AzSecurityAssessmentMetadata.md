---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: e72766e754394bb43775f73072941dc0d3989c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910637"
---
# <span data-ttu-id="ee2db-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ee2db-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ee2db-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee2db-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2db-103">建立或更新安全性評定類型。</span><span class="sxs-lookup"><span data-stu-id="ee2db-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="ee2db-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee2db-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee2db-105">描述</span><span class="sxs-lookup"><span data-stu-id="ee2db-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2db-106">建立或更新安全性評定中繼資料，可用來建立及管理各種評定屬性。</span><span class="sxs-lookup"><span data-stu-id="ee2db-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="ee2db-107">在採取這個動作之後，您將能報告此訂閱中任何資源的評定結果。</span><span class="sxs-lookup"><span data-stu-id="ee2db-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="ee2db-108">例子</span><span class="sxs-lookup"><span data-stu-id="ee2db-108">EXAMPLES</span></span>

### <span data-ttu-id="ee2db-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="ee2db-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="ee2db-110">在訂閱中建立新評定類型。</span><span class="sxs-lookup"><span data-stu-id="ee2db-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="ee2db-111">參數</span><span class="sxs-lookup"><span data-stu-id="ee2db-111">PARAMETERS</span></span>

### <span data-ttu-id="ee2db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2db-112">-DefaultProfile</span></span>
<span data-ttu-id="ee2db-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee2db-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee2db-114">-描述</span><span class="sxs-lookup"><span data-stu-id="ee2db-114">-Description</span></span>
<span data-ttu-id="ee2db-115">詳細的字串，可協助使用者瞭解此評定的意義及其計算方式。</span><span class="sxs-lookup"><span data-stu-id="ee2db-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="ee2db-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ee2db-116">-DisplayName</span></span>
<span data-ttu-id="ee2db-117">此物件的可讀人稱謂。</span><span class="sxs-lookup"><span data-stu-id="ee2db-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="ee2db-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee2db-118">-Name</span></span>
<span data-ttu-id="ee2db-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ee2db-119">Resource name.</span></span>

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

### <span data-ttu-id="ee2db-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="ee2db-120">-RemediationDescription</span></span>
<span data-ttu-id="ee2db-121">詳細的字串，可協助使用者瞭解減輕或修正安全性問題的不同方式。</span><span class="sxs-lookup"><span data-stu-id="ee2db-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="ee2db-122">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="ee2db-122">-Severity</span></span>
<span data-ttu-id="ee2db-123">指出如果評定不健康，安全性風險的重要性。</span><span class="sxs-lookup"><span data-stu-id="ee2db-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="ee2db-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ee2db-124">-Confirm</span></span>
<span data-ttu-id="ee2db-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ee2db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2db-126">-WhatIf</span></span>
<span data-ttu-id="ee2db-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee2db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee2db-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee2db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2db-129">CommonParameters</span></span>
<span data-ttu-id="ee2db-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee2db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2db-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee2db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2db-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ee2db-132">INPUTS</span></span>

### <span data-ttu-id="ee2db-133">沒有</span><span class="sxs-lookup"><span data-stu-id="ee2db-133">None</span></span>

## <span data-ttu-id="ee2db-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ee2db-134">OUTPUTS</span></span>

### <span data-ttu-id="ee2db-135">Microsoft.Azure.Commands.Security.models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ee2db-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ee2db-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ee2db-136">NOTES</span></span>

## <span data-ttu-id="ee2db-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee2db-137">RELATED LINKS</span></span>
