---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969601"
---
# <span data-ttu-id="962a9-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="962a9-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="962a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="962a9-102">SYNOPSIS</span></span>
<span data-ttu-id="962a9-103">取得認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="962a9-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="962a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="962a9-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="962a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="962a9-105">DESCRIPTION</span></span>
<span data-ttu-id="962a9-106">**AzCognitiveServicesAccountNetworkRuleSet** Cmdlet 會取得認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="962a9-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="962a9-107">示例</span><span class="sxs-lookup"><span data-stu-id="962a9-107">EXAMPLES</span></span>

### <span data-ttu-id="962a9-108">範例1：取得指定的認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="962a9-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="962a9-109">這個命令會取得指定的認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="962a9-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="962a9-110">參數</span><span class="sxs-lookup"><span data-stu-id="962a9-110">PARAMETERS</span></span>

### <span data-ttu-id="962a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962a9-111">-DefaultProfile</span></span>
<span data-ttu-id="962a9-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="962a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="962a9-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="962a9-113">-Name</span></span>
<span data-ttu-id="962a9-114">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="962a9-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="962a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="962a9-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="962a9-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962a9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962a9-117">CommonParameters</span></span>
<span data-ttu-id="962a9-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="962a9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962a9-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="962a9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962a9-120">輸入</span><span class="sxs-lookup"><span data-stu-id="962a9-120">INPUTS</span></span>

### <span data-ttu-id="962a9-121">System.object</span><span class="sxs-lookup"><span data-stu-id="962a9-121">System.String</span></span>

## <span data-ttu-id="962a9-122">輸出</span><span class="sxs-lookup"><span data-stu-id="962a9-122">OUTPUTS</span></span>

### <span data-ttu-id="962a9-123">PSNetworkRuleSet （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="962a9-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="962a9-124">筆記</span><span class="sxs-lookup"><span data-stu-id="962a9-124">NOTES</span></span>

## <span data-ttu-id="962a9-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="962a9-125">RELATED LINKS</span></span>
