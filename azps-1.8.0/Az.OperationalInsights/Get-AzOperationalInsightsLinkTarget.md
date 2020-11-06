---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623387"
---
# <span data-ttu-id="5ea70-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="5ea70-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="5ea70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ea70-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea70-103">取得不與訂閱相關聯的帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ea70-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="5ea70-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ea70-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ea70-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ea70-105">DESCRIPTION</span></span>
<span data-ttu-id="5ea70-106">**AzOperationalInsightsLinkTarget** Cmdlet 會列出與 Azure 訂閱不相關聯的現有帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ea70-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="5ea70-107">若要將新的工作區連結至現有的帳戶，請在新工作區的 [customer ID] 屬性中，使用此作業所傳回的客戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ea70-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="5ea70-108">示例</span><span class="sxs-lookup"><span data-stu-id="5ea70-108">EXAMPLES</span></span>

### <span data-ttu-id="5ea70-109">範例1：取得未連結的帳戶</span><span class="sxs-lookup"><span data-stu-id="5ea70-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="5ea70-110">這個命令會取得呼叫者識別碼所擁有的未連結帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ea70-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="5ea70-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ea70-111">PARAMETERS</span></span>

### <span data-ttu-id="5ea70-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea70-112">-DefaultProfile</span></span>
<span data-ttu-id="5ea70-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5ea70-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea70-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea70-114">CommonParameters</span></span>
<span data-ttu-id="5ea70-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ea70-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea70-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ea70-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea70-117">輸入</span><span class="sxs-lookup"><span data-stu-id="5ea70-117">INPUTS</span></span>

### <span data-ttu-id="5ea70-118">所有</span><span class="sxs-lookup"><span data-stu-id="5ea70-118">None</span></span>

## <span data-ttu-id="5ea70-119">輸出</span><span class="sxs-lookup"><span data-stu-id="5ea70-119">OUTPUTS</span></span>

### <span data-ttu-id="5ea70-120">PSAccount 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="5ea70-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="5ea70-121">筆記</span><span class="sxs-lookup"><span data-stu-id="5ea70-121">NOTES</span></span>

## <span data-ttu-id="5ea70-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ea70-122">RELATED LINKS</span></span>

[<span data-ttu-id="5ea70-123">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ea70-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


