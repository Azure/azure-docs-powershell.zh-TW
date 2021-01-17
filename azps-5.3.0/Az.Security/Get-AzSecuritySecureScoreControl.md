---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286539"
---
# <span data-ttu-id="88e02-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="88e02-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="88e02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88e02-102">SYNOPSIS</span></span>
<span data-ttu-id="88e02-103">在訂閱上取得安全性安全分數控制項及其結果</span><span class="sxs-lookup"><span data-stu-id="88e02-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="88e02-104">句法</span><span class="sxs-lookup"><span data-stu-id="88e02-104">SYNTAX</span></span>

### <span data-ttu-id="88e02-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="88e02-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88e02-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="88e02-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e02-107">示例</span><span class="sxs-lookup"><span data-stu-id="88e02-107">EXAMPLES</span></span>

### <span data-ttu-id="88e02-108">範例1</span><span class="sxs-lookup"><span data-stu-id="88e02-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="88e02-109">取得訂閱中的所有安全性安全分數</span><span class="sxs-lookup"><span data-stu-id="88e02-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="88e02-110">參數</span><span class="sxs-lookup"><span data-stu-id="88e02-110">PARAMETERS</span></span>

### <span data-ttu-id="88e02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e02-111">-DefaultProfile</span></span>
<span data-ttu-id="88e02-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88e02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e02-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="88e02-113">-Name</span></span>
<span data-ttu-id="88e02-114">安全計分名稱。</span><span class="sxs-lookup"><span data-stu-id="88e02-114">Secure score name.</span></span>

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

### <span data-ttu-id="88e02-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e02-115">CommonParameters</span></span>
<span data-ttu-id="88e02-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88e02-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e02-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="88e02-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e02-118">輸入</span><span class="sxs-lookup"><span data-stu-id="88e02-118">INPUTS</span></span>

### <span data-ttu-id="88e02-119">System.object</span><span class="sxs-lookup"><span data-stu-id="88e02-119">System.String</span></span>

## <span data-ttu-id="88e02-120">輸出</span><span class="sxs-lookup"><span data-stu-id="88e02-120">OUTPUTS</span></span>

### <span data-ttu-id="88e02-121">PSSecuritySecureScoreControl （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="88e02-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="88e02-122">筆記</span><span class="sxs-lookup"><span data-stu-id="88e02-122">NOTES</span></span>

## <span data-ttu-id="88e02-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="88e02-123">RELATED LINKS</span></span>
