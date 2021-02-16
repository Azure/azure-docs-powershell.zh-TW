---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133586"
---
# <span data-ttu-id="13c03-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="13c03-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="13c03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13c03-102">SYNOPSIS</span></span>
<span data-ttu-id="13c03-103">取得訂閱上安全性安全分數控制定義</span><span class="sxs-lookup"><span data-stu-id="13c03-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="13c03-104">句法</span><span class="sxs-lookup"><span data-stu-id="13c03-104">SYNTAX</span></span>

### <span data-ttu-id="13c03-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="13c03-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c03-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="13c03-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c03-107">示例</span><span class="sxs-lookup"><span data-stu-id="13c03-107">EXAMPLES</span></span>

### <span data-ttu-id="13c03-108">範例1</span><span class="sxs-lookup"><span data-stu-id="13c03-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="13c03-109">取得訂閱中的所有安全性安全分數控制定義</span><span class="sxs-lookup"><span data-stu-id="13c03-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="13c03-110">參數</span><span class="sxs-lookup"><span data-stu-id="13c03-110">PARAMETERS</span></span>

### <span data-ttu-id="13c03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c03-111">-DefaultProfile</span></span>
<span data-ttu-id="13c03-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13c03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c03-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c03-113">CommonParameters</span></span>
<span data-ttu-id="13c03-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13c03-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c03-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="13c03-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c03-116">輸入</span><span class="sxs-lookup"><span data-stu-id="13c03-116">INPUTS</span></span>

### <span data-ttu-id="13c03-117">System.object</span><span class="sxs-lookup"><span data-stu-id="13c03-117">System.String</span></span>

## <span data-ttu-id="13c03-118">輸出</span><span class="sxs-lookup"><span data-stu-id="13c03-118">OUTPUTS</span></span>

### <span data-ttu-id="13c03-119">PSSecuritySecureScoreControlDefinition （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="13c03-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="13c03-120">筆記</span><span class="sxs-lookup"><span data-stu-id="13c03-120">NOTES</span></span>

## <span data-ttu-id="13c03-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="13c03-121">RELATED LINKS</span></span>
