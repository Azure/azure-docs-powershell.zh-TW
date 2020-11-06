---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 3f0418a06b11af933cfc7ad09a2c0fc492db4f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453348"
---
# <span data-ttu-id="e58c0-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="e58c0-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="e58c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e58c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e58c0-103">取得不與訂閱相關聯的帳戶。</span><span class="sxs-lookup"><span data-stu-id="e58c0-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e58c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e58c0-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e58c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="e58c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e58c0-106">**AzureRmOperationalInsightsLinkTargets** Cmdlet 會列出與 Azure 訂閱不相關聯的現有帳戶。</span><span class="sxs-lookup"><span data-stu-id="e58c0-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="e58c0-107">若要將新的工作區連結至現有的帳戶，請在新工作區的 [customer ID] 屬性中，使用此作業所傳回的客戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="e58c0-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="e58c0-108">示例</span><span class="sxs-lookup"><span data-stu-id="e58c0-108">EXAMPLES</span></span>

### <span data-ttu-id="e58c0-109">範例1：取得未連結的帳戶</span><span class="sxs-lookup"><span data-stu-id="e58c0-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="e58c0-110">這個命令會取得呼叫者識別碼所擁有的未連結帳戶。</span><span class="sxs-lookup"><span data-stu-id="e58c0-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="e58c0-111">參數</span><span class="sxs-lookup"><span data-stu-id="e58c0-111">PARAMETERS</span></span>

### <span data-ttu-id="e58c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e58c0-112">-DefaultProfile</span></span>
<span data-ttu-id="e58c0-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e58c0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e58c0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e58c0-114">CommonParameters</span></span>
<span data-ttu-id="e58c0-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e58c0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e58c0-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e58c0-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e58c0-117">輸入</span><span class="sxs-lookup"><span data-stu-id="e58c0-117">INPUTS</span></span>

## <span data-ttu-id="e58c0-118">輸出</span><span class="sxs-lookup"><span data-stu-id="e58c0-118">OUTPUTS</span></span>

### <span data-ttu-id="e58c0-119">[System.object]. 清單 ' 1 [OperationalInsights]。 PSAccount]</span><span class="sxs-lookup"><span data-stu-id="e58c0-119">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="e58c0-120">筆記</span><span class="sxs-lookup"><span data-stu-id="e58c0-120">NOTES</span></span>

## <span data-ttu-id="e58c0-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="e58c0-121">RELATED LINKS</span></span>

[<span data-ttu-id="e58c0-122">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e58c0-122">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


