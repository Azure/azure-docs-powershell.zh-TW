---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 60a61af31b5a7986779b19b893d4c02d0039ae49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916233"
---
# <span data-ttu-id="f7d4a-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7d4a-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="f7d4a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d4a-103">取得認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="f7d4a-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f7d4a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7d4a-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7d4a-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d4a-106">**Get-AzCognitiveServicesAccountNetworkRuleSet** Cmdlet 取得認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="f7d4a-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f7d4a-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d4a-108">範例 1：取得指定認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="f7d4a-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="f7d4a-109">此命令會獲得指定認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="f7d4a-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="f7d4a-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7d4a-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d4a-111">-DefaultProfile</span></span>
<span data-ttu-id="f7d4a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7d4a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d4a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7d4a-113">-Name</span></span>
<span data-ttu-id="f7d4a-114">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d4a-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="f7d4a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d4a-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7d4a-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f7d4a-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7d4a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d4a-117">CommonParameters</span></span>
<span data-ttu-id="f7d4a-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7d4a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d4a-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7d4a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d4a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f7d4a-120">INPUTS</span></span>

### <span data-ttu-id="f7d4a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f7d4a-121">System.String</span></span>

## <span data-ttu-id="f7d4a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f7d4a-122">OUTPUTS</span></span>

### <span data-ttu-id="f7d4a-123">Microsoft.Azure.Commands.management.CognitiveServices.models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7d4a-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="f7d4a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f7d4a-124">NOTES</span></span>

## <span data-ttu-id="f7d4a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7d4a-125">RELATED LINKS</span></span>
