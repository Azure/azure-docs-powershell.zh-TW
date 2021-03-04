---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: e8ec0073eef8b8db95197e19f2bfd61d0bbcdafd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913313"
---
# <span data-ttu-id="9f731-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="9f731-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="9f731-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f731-102">SYNOPSIS</span></span>
<span data-ttu-id="9f731-103">取得訂閱上的安全性安全分數控制定義</span><span class="sxs-lookup"><span data-stu-id="9f731-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="9f731-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f731-104">SYNTAX</span></span>

### <span data-ttu-id="9f731-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="9f731-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f731-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="9f731-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f731-107">例子</span><span class="sxs-lookup"><span data-stu-id="9f731-107">EXAMPLES</span></span>

### <span data-ttu-id="9f731-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9f731-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="9f731-109">取得訂閱中所有安全性安全分數控制定義</span><span class="sxs-lookup"><span data-stu-id="9f731-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="9f731-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f731-110">PARAMETERS</span></span>

### <span data-ttu-id="9f731-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f731-111">-DefaultProfile</span></span>
<span data-ttu-id="9f731-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f731-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f731-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f731-113">CommonParameters</span></span>
<span data-ttu-id="9f731-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f731-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f731-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f731-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f731-116">輸入</span><span class="sxs-lookup"><span data-stu-id="9f731-116">INPUTS</span></span>

### <span data-ttu-id="9f731-117">System.String</span><span class="sxs-lookup"><span data-stu-id="9f731-117">System.String</span></span>

## <span data-ttu-id="9f731-118">輸出</span><span class="sxs-lookup"><span data-stu-id="9f731-118">OUTPUTS</span></span>

### <span data-ttu-id="9f731-119">Microsoft.Azure.Commands.Security.models.assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="9f731-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="9f731-120">筆記</span><span class="sxs-lookup"><span data-stu-id="9f731-120">NOTES</span></span>

## <span data-ttu-id="9f731-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f731-121">RELATED LINKS</span></span>
