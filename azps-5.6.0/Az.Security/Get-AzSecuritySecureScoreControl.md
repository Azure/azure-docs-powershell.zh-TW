---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 497865446e943fc34f45f6c98713d559086cca84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908749"
---
# <span data-ttu-id="462f1-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="462f1-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="462f1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="462f1-102">SYNOPSIS</span></span>
<span data-ttu-id="462f1-103">取得安全性安全分數控制項及其訂閱結果</span><span class="sxs-lookup"><span data-stu-id="462f1-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="462f1-104">語法</span><span class="sxs-lookup"><span data-stu-id="462f1-104">SYNTAX</span></span>

### <span data-ttu-id="462f1-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="462f1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="462f1-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="462f1-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="462f1-107">例子</span><span class="sxs-lookup"><span data-stu-id="462f1-107">EXAMPLES</span></span>

### <span data-ttu-id="462f1-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="462f1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="462f1-109">在訂閱中獲得所有安全性安全分數</span><span class="sxs-lookup"><span data-stu-id="462f1-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="462f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="462f1-110">PARAMETERS</span></span>

### <span data-ttu-id="462f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462f1-111">-DefaultProfile</span></span>
<span data-ttu-id="462f1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="462f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="462f1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="462f1-113">-Name</span></span>
<span data-ttu-id="462f1-114">安全分數名稱。</span><span class="sxs-lookup"><span data-stu-id="462f1-114">Secure score name.</span></span>

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

### <span data-ttu-id="462f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462f1-115">CommonParameters</span></span>
<span data-ttu-id="462f1-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="462f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462f1-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="462f1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462f1-118">輸入</span><span class="sxs-lookup"><span data-stu-id="462f1-118">INPUTS</span></span>

### <span data-ttu-id="462f1-119">System.String</span><span class="sxs-lookup"><span data-stu-id="462f1-119">System.String</span></span>

## <span data-ttu-id="462f1-120">輸出</span><span class="sxs-lookup"><span data-stu-id="462f1-120">OUTPUTS</span></span>

### <span data-ttu-id="462f1-121">Microsoft.Azure.Commands.Security.models.assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="462f1-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="462f1-122">筆記</span><span class="sxs-lookup"><span data-stu-id="462f1-122">NOTES</span></span>

## <span data-ttu-id="462f1-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="462f1-123">RELATED LINKS</span></span>
