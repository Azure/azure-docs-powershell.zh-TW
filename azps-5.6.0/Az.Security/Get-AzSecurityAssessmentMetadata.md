---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 92858967d460785af151520c504a4e1cbdb4d3d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916491"
---
# <span data-ttu-id="f140c-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f140c-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="f140c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f140c-102">SYNOPSIS</span></span>
<span data-ttu-id="f140c-103">在訂閱中獲得安全性評定類型和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f140c-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="f140c-104">語法</span><span class="sxs-lookup"><span data-stu-id="f140c-104">SYNTAX</span></span>

### <span data-ttu-id="f140c-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="f140c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f140c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f140c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f140c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f140c-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f140c-108">描述</span><span class="sxs-lookup"><span data-stu-id="f140c-108">DESCRIPTION</span></span>
<span data-ttu-id="f140c-109">在訂閱中獲得安全性評定類型和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f140c-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="f140c-110">安全性評定中繼資料Built-In使用者可以定義的自訂評定類型。</span><span class="sxs-lookup"><span data-stu-id="f140c-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="f140c-111">例子</span><span class="sxs-lookup"><span data-stu-id="f140c-111">EXAMPLES</span></span>

### <span data-ttu-id="f140c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="f140c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="f140c-113">獲得目前訂閱上所配置的所有內建評定和自訂評定。</span><span class="sxs-lookup"><span data-stu-id="f140c-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="f140c-114">參數</span><span class="sxs-lookup"><span data-stu-id="f140c-114">PARAMETERS</span></span>

### <span data-ttu-id="f140c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f140c-115">-DefaultProfile</span></span>
<span data-ttu-id="f140c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f140c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f140c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f140c-117">-Name</span></span>
<span data-ttu-id="f140c-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f140c-118">Resource name.</span></span>

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

### <span data-ttu-id="f140c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f140c-119">-ResourceId</span></span>
<span data-ttu-id="f140c-120">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f140c-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f140c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f140c-121">CommonParameters</span></span>
<span data-ttu-id="f140c-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f140c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f140c-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f140c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f140c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f140c-124">INPUTS</span></span>

### <span data-ttu-id="f140c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f140c-125">System.String</span></span>

## <span data-ttu-id="f140c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f140c-126">OUTPUTS</span></span>

### <span data-ttu-id="f140c-127">Microsoft.Azure.Commands.Security.models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f140c-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="f140c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f140c-128">NOTES</span></span>

## <span data-ttu-id="f140c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f140c-129">RELATED LINKS</span></span>
