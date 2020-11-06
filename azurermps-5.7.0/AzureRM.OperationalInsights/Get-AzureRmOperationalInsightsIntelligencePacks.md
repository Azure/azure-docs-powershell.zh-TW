---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 0e63b6926f635a4260e6e3c9d658afa410f29966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447734"
---
# <span data-ttu-id="2f5ec-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="2f5ec-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="2f5ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5ec-103">取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f5ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f5ec-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f5ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f5ec-105">DESCRIPTION</span></span>
<span data-ttu-id="2f5ec-106">**AzureRmOperationalInsightsIntelligencePacks** Cmdlet 會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="2f5ec-107">示例</span><span class="sxs-lookup"><span data-stu-id="2f5ec-107">EXAMPLES</span></span>

### <span data-ttu-id="2f5ec-108">範例1：取得智慧套件</span><span class="sxs-lookup"><span data-stu-id="2f5ec-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="2f5ec-109">這個命令會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="2f5ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="2f5ec-110">PARAMETERS</span></span>

### <span data-ttu-id="2f5ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5ec-111">-DefaultProfile</span></span>
<span data-ttu-id="2f5ec-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2f5ec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f5ec-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f5ec-113">-ResourceGroupName</span></span>
<span data-ttu-id="2f5ec-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5ec-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2f5ec-115">-WorkspaceName</span></span>
<span data-ttu-id="2f5ec-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5ec-117">CommonParameters</span></span>
<span data-ttu-id="2f5ec-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5ec-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5ec-120">輸入</span><span class="sxs-lookup"><span data-stu-id="2f5ec-120">INPUTS</span></span>

### <span data-ttu-id="2f5ec-121">所有</span><span class="sxs-lookup"><span data-stu-id="2f5ec-121">None</span></span>
<span data-ttu-id="2f5ec-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2f5ec-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f5ec-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2f5ec-123">OUTPUTS</span></span>

### <span data-ttu-id="2f5ec-124">[System.object]. 清單 ' 1 [OperationalInsights]。 PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="2f5ec-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="2f5ec-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2f5ec-125">NOTES</span></span>

## <span data-ttu-id="2f5ec-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f5ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="2f5ec-127">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f5ec-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


