---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 0cce3e4e1aa0f5de93e9c54c00cfa1902a4c24b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913322"
---
# <span data-ttu-id="be610-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="be610-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="be610-102">簡介</span><span class="sxs-lookup"><span data-stu-id="be610-102">SYNOPSIS</span></span>
<span data-ttu-id="be610-103">取得安全性安全分數及其訂閱結果</span><span class="sxs-lookup"><span data-stu-id="be610-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="be610-104">語法</span><span class="sxs-lookup"><span data-stu-id="be610-104">SYNTAX</span></span>

### <span data-ttu-id="be610-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="be610-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be610-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="be610-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be610-107">例子</span><span class="sxs-lookup"><span data-stu-id="be610-107">EXAMPLES</span></span>

### <span data-ttu-id="be610-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="be610-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="be610-109">在訂閱中獲得所有安全性安全分數</span><span class="sxs-lookup"><span data-stu-id="be610-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="be610-110">參數</span><span class="sxs-lookup"><span data-stu-id="be610-110">PARAMETERS</span></span>

### <span data-ttu-id="be610-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be610-111">-DefaultProfile</span></span>
<span data-ttu-id="be610-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="be610-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be610-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="be610-113">-Name</span></span>
<span data-ttu-id="be610-114">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="be610-114">Resource name.</span></span>

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

### <span data-ttu-id="be610-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be610-115">CommonParameters</span></span>
<span data-ttu-id="be610-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="be610-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be610-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be610-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be610-118">輸入</span><span class="sxs-lookup"><span data-stu-id="be610-118">INPUTS</span></span>

### <span data-ttu-id="be610-119">System.String</span><span class="sxs-lookup"><span data-stu-id="be610-119">System.String</span></span>

## <span data-ttu-id="be610-120">輸出</span><span class="sxs-lookup"><span data-stu-id="be610-120">OUTPUTS</span></span>

### <span data-ttu-id="be610-121">Microsoft.Azure.Commands.Security.models.assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="be610-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="be610-122">筆記</span><span class="sxs-lookup"><span data-stu-id="be610-122">NOTES</span></span>

## <span data-ttu-id="be610-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="be610-123">RELATED LINKS</span></span>
