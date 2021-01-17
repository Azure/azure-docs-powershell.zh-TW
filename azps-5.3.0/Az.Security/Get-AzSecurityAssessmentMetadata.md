---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448704"
---
# <span data-ttu-id="1a860-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1a860-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1a860-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a860-102">SYNOPSIS</span></span>
<span data-ttu-id="1a860-103">取得訂閱中的安全性評定類型和 metadta。</span><span class="sxs-lookup"><span data-stu-id="1a860-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="1a860-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a860-104">SYNTAX</span></span>

### <span data-ttu-id="1a860-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="1a860-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a860-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1a860-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a860-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a860-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a860-108">說明</span><span class="sxs-lookup"><span data-stu-id="1a860-108">DESCRIPTION</span></span>
<span data-ttu-id="1a860-109">取得訂閱中的安全性評定類型和 metadta。</span><span class="sxs-lookup"><span data-stu-id="1a860-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="1a860-110">安全性評定中繼資料包括 Built-In 評量以及使用者可以定義的自訂評定類型。</span><span class="sxs-lookup"><span data-stu-id="1a860-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="1a860-111">示例</span><span class="sxs-lookup"><span data-stu-id="1a860-111">EXAMPLES</span></span>

### <span data-ttu-id="1a860-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1a860-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="1a860-113">取得在目前訂閱上設定的所有內建評估和自訂評量。</span><span class="sxs-lookup"><span data-stu-id="1a860-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="1a860-114">參數</span><span class="sxs-lookup"><span data-stu-id="1a860-114">PARAMETERS</span></span>

### <span data-ttu-id="1a860-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a860-115">-DefaultProfile</span></span>
<span data-ttu-id="1a860-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a860-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a860-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a860-117">-Name</span></span>
<span data-ttu-id="1a860-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1a860-118">Resource name.</span></span>

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

### <span data-ttu-id="1a860-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a860-119">-ResourceId</span></span>
<span data-ttu-id="1a860-120">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a860-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1a860-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a860-121">CommonParameters</span></span>
<span data-ttu-id="1a860-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a860-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a860-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1a860-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a860-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1a860-124">INPUTS</span></span>

### <span data-ttu-id="1a860-125">System.object</span><span class="sxs-lookup"><span data-stu-id="1a860-125">System.String</span></span>

## <span data-ttu-id="1a860-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1a860-126">OUTPUTS</span></span>

### <span data-ttu-id="1a860-127">PSSecurityAssessmentMetadata 中的 AssessmentMetadata （Security..。</span><span class="sxs-lookup"><span data-stu-id="1a860-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1a860-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1a860-128">NOTES</span></span>

## <span data-ttu-id="1a860-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a860-129">RELATED LINKS</span></span>
