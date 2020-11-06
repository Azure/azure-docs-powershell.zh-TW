---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
ms.openlocfilehash: 471178f6b35ea3a382c02a2a0970d0a9466b43ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452112"
---
# <span data-ttu-id="ab66c-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="ab66c-101">Send-Feedback</span></span>

## <span data-ttu-id="ab66c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab66c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab66c-103">透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="ab66c-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab66c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab66c-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab66c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab66c-105">DESCRIPTION</span></span>
<span data-ttu-id="ab66c-106">Send-Feedback Cmdlet 會將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="ab66c-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="ab66c-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab66c-107">EXAMPLES</span></span>

### <span data-ttu-id="ab66c-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="ab66c-108">Example 1:</span></span>
```
PS C:\> Send-Feedback

With zero (0) being the least and ten (10) being the most, how likely are you to recommend Azure PowerShell to a friend or colleague?

10

What does Azure PowerShell do well?

Response.

Upon what could Azure PowerShell improve?

Response.

Please enter your email if you are interested in providing follow up information:

your@email.com
```

## <span data-ttu-id="ab66c-109">參數</span><span class="sxs-lookup"><span data-stu-id="ab66c-109">PARAMETERS</span></span>

### <span data-ttu-id="ab66c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab66c-110">-DefaultProfile</span></span>
<span data-ttu-id="ab66c-111">用於與 azure 進行通訊的認證、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab66c-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab66c-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab66c-112">CommonParameters</span></span>
<span data-ttu-id="ab66c-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab66c-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab66c-114">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab66c-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab66c-115">輸入</span><span class="sxs-lookup"><span data-stu-id="ab66c-115">INPUTS</span></span>

### <span data-ttu-id="ab66c-116">所有</span><span class="sxs-lookup"><span data-stu-id="ab66c-116">None</span></span>
<span data-ttu-id="ab66c-117">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ab66c-117">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab66c-118">輸出</span><span class="sxs-lookup"><span data-stu-id="ab66c-118">OUTPUTS</span></span>

### <span data-ttu-id="ab66c-119">System.void</span><span class="sxs-lookup"><span data-stu-id="ab66c-119">System.Void</span></span>

## <span data-ttu-id="ab66c-120">筆記</span><span class="sxs-lookup"><span data-stu-id="ab66c-120">NOTES</span></span>

## <span data-ttu-id="ab66c-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab66c-121">RELATED LINKS</span></span>

