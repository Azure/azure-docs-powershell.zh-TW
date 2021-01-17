---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448632"
---
# <span data-ttu-id="5e580-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="5e580-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="5e580-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e580-102">SYNOPSIS</span></span>
<span data-ttu-id="5e580-103">建立或更新安全性評定類型。</span><span class="sxs-lookup"><span data-stu-id="5e580-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="5e580-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e580-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e580-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e580-105">DESCRIPTION</span></span>
<span data-ttu-id="5e580-106">建立或更新安全評定中繼資料，可用於建立及管理各種評量屬性。</span><span class="sxs-lookup"><span data-stu-id="5e580-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="5e580-107">在此動作之後，您將能夠在此訂閱中的任何資源上報告評估結果。</span><span class="sxs-lookup"><span data-stu-id="5e580-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="5e580-108">示例</span><span class="sxs-lookup"><span data-stu-id="5e580-108">EXAMPLES</span></span>

### <span data-ttu-id="5e580-109">範例1</span><span class="sxs-lookup"><span data-stu-id="5e580-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="5e580-110">在訂閱中建立新的評定類型。</span><span class="sxs-lookup"><span data-stu-id="5e580-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="5e580-111">參數</span><span class="sxs-lookup"><span data-stu-id="5e580-111">PARAMETERS</span></span>

### <span data-ttu-id="5e580-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e580-112">-DefaultProfile</span></span>
<span data-ttu-id="5e580-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e580-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e580-114">-描述</span><span class="sxs-lookup"><span data-stu-id="5e580-114">-Description</span></span>
<span data-ttu-id="5e580-115">詳細字串，可協助使用者瞭解此評估的意義，以及它的計算方式。</span><span class="sxs-lookup"><span data-stu-id="5e580-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="5e580-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e580-116">-DisplayName</span></span>
<span data-ttu-id="5e580-117">這個物件的人類可讀標題。</span><span class="sxs-lookup"><span data-stu-id="5e580-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="5e580-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e580-118">-Name</span></span>
<span data-ttu-id="5e580-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5e580-119">Resource name.</span></span>

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

### <span data-ttu-id="5e580-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="5e580-120">-RemediationDescription</span></span>
<span data-ttu-id="5e580-121">詳細字串，可協助使用者瞭解減少或修正安全問題的不同方式。</span><span class="sxs-lookup"><span data-stu-id="5e580-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="5e580-122">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="5e580-122">-Severity</span></span>
<span data-ttu-id="5e580-123">指出評估無法正常運行時的安全性風險重要性。</span><span class="sxs-lookup"><span data-stu-id="5e580-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="5e580-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5e580-124">-Confirm</span></span>
<span data-ttu-id="5e580-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e580-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e580-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e580-126">-WhatIf</span></span>
<span data-ttu-id="5e580-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e580-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e580-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e580-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e580-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e580-129">CommonParameters</span></span>
<span data-ttu-id="5e580-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e580-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e580-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5e580-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e580-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5e580-132">INPUTS</span></span>

### <span data-ttu-id="5e580-133">所有</span><span class="sxs-lookup"><span data-stu-id="5e580-133">None</span></span>

## <span data-ttu-id="5e580-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5e580-134">OUTPUTS</span></span>

### <span data-ttu-id="5e580-135">PSSecurityAssessmentMetadata 中的 AssessmentMetadata （Security..。</span><span class="sxs-lookup"><span data-stu-id="5e580-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="5e580-136">筆記</span><span class="sxs-lookup"><span data-stu-id="5e580-136">NOTES</span></span>

## <span data-ttu-id="5e580-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e580-137">RELATED LINKS</span></span>
