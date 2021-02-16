---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133602"
---
# <span data-ttu-id="53994-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="53994-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="53994-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53994-102">SYNOPSIS</span></span>
<span data-ttu-id="53994-103">在訂閱上取得安全性安全分數及其結果</span><span class="sxs-lookup"><span data-stu-id="53994-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="53994-104">句法</span><span class="sxs-lookup"><span data-stu-id="53994-104">SYNTAX</span></span>

### <span data-ttu-id="53994-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="53994-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53994-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="53994-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53994-107">示例</span><span class="sxs-lookup"><span data-stu-id="53994-107">EXAMPLES</span></span>

### <span data-ttu-id="53994-108">範例1</span><span class="sxs-lookup"><span data-stu-id="53994-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="53994-109">取得訂閱中的所有安全性安全分數</span><span class="sxs-lookup"><span data-stu-id="53994-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="53994-110">參數</span><span class="sxs-lookup"><span data-stu-id="53994-110">PARAMETERS</span></span>

### <span data-ttu-id="53994-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53994-111">-DefaultProfile</span></span>
<span data-ttu-id="53994-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53994-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53994-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="53994-113">-Name</span></span>
<span data-ttu-id="53994-114">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="53994-114">Resource name.</span></span>

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

### <span data-ttu-id="53994-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53994-115">CommonParameters</span></span>
<span data-ttu-id="53994-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53994-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53994-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="53994-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53994-118">輸入</span><span class="sxs-lookup"><span data-stu-id="53994-118">INPUTS</span></span>

### <span data-ttu-id="53994-119">System.object</span><span class="sxs-lookup"><span data-stu-id="53994-119">System.String</span></span>

## <span data-ttu-id="53994-120">輸出</span><span class="sxs-lookup"><span data-stu-id="53994-120">OUTPUTS</span></span>

### <span data-ttu-id="53994-121">PSSecuritySecureScore （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="53994-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="53994-122">筆記</span><span class="sxs-lookup"><span data-stu-id="53994-122">NOTES</span></span>

## <span data-ttu-id="53994-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="53994-123">RELATED LINKS</span></span>
