---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970204"
---
# <span data-ttu-id="22294-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="22294-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="22294-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22294-102">SYNOPSIS</span></span>
<span data-ttu-id="22294-103">在訂閱上取得安全性評估及其結果</span><span class="sxs-lookup"><span data-stu-id="22294-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="22294-104">句法</span><span class="sxs-lookup"><span data-stu-id="22294-104">SYNTAX</span></span>

### <span data-ttu-id="22294-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="22294-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22294-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="22294-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22294-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="22294-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22294-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="22294-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22294-109">說明</span><span class="sxs-lookup"><span data-stu-id="22294-109">DESCRIPTION</span></span>
<span data-ttu-id="22294-110">取得安全性評估及其在訂閱上的結果。</span><span class="sxs-lookup"><span data-stu-id="22294-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="22294-111">安全性評估會讓您知道 Azure 安全中心 recommanded 哪些最佳做法，以便在您的 Azure 訂閱上緩解。</span><span class="sxs-lookup"><span data-stu-id="22294-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="22294-112">示例</span><span class="sxs-lookup"><span data-stu-id="22294-112">EXAMPLES</span></span>

### <span data-ttu-id="22294-113">範例1</span><span class="sxs-lookup"><span data-stu-id="22294-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="22294-114">取得訂閱中的所有安全性評估</span><span class="sxs-lookup"><span data-stu-id="22294-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="22294-115">參數</span><span class="sxs-lookup"><span data-stu-id="22294-115">PARAMETERS</span></span>

### <span data-ttu-id="22294-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="22294-116">-AssessedResourceId</span></span>
<span data-ttu-id="22294-117">計算評估所依據之資源的完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="22294-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22294-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22294-118">-DefaultProfile</span></span>
<span data-ttu-id="22294-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22294-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22294-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="22294-120">-Name</span></span>
<span data-ttu-id="22294-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="22294-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22294-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22294-122">-ResourceId</span></span>
<span data-ttu-id="22294-123">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="22294-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="22294-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22294-124">CommonParameters</span></span>
<span data-ttu-id="22294-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22294-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22294-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="22294-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22294-127">輸入</span><span class="sxs-lookup"><span data-stu-id="22294-127">INPUTS</span></span>

### <span data-ttu-id="22294-128">System.object</span><span class="sxs-lookup"><span data-stu-id="22294-128">System.String</span></span>

## <span data-ttu-id="22294-129">輸出</span><span class="sxs-lookup"><span data-stu-id="22294-129">OUTPUTS</span></span>

### <span data-ttu-id="22294-130">PSSecurityAssessment （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="22294-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="22294-131">筆記</span><span class="sxs-lookup"><span data-stu-id="22294-131">NOTES</span></span>

## <span data-ttu-id="22294-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="22294-132">RELATED LINKS</span></span>
