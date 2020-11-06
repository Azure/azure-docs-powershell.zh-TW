---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 56bc2dd74f17daa9a56eac8ebd5128e6f074fe13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448070"
---
# <span data-ttu-id="509e7-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="509e7-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="509e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="509e7-102">SYNOPSIS</span></span>
<span data-ttu-id="509e7-103">取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="509e7-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="509e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="509e7-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="509e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="509e7-105">DESCRIPTION</span></span>
<span data-ttu-id="509e7-106">**AzureRmOperationalInsightsIntelligencePacks** Cmdlet 會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="509e7-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="509e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="509e7-107">EXAMPLES</span></span>

### <span data-ttu-id="509e7-108">範例1：取得智慧套件</span><span class="sxs-lookup"><span data-stu-id="509e7-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="509e7-109">這個命令會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="509e7-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="509e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="509e7-110">PARAMETERS</span></span>

### <span data-ttu-id="509e7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="509e7-111">-ResourceGroupName</span></span>
<span data-ttu-id="509e7-112">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="509e7-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="509e7-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="509e7-113">-WorkspaceName</span></span>
<span data-ttu-id="509e7-114">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="509e7-114">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="509e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="509e7-115">-DefaultProfile</span></span>
<span data-ttu-id="509e7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="509e7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="509e7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509e7-117">CommonParameters</span></span>
<span data-ttu-id="509e7-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="509e7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509e7-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="509e7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509e7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="509e7-120">INPUTS</span></span>

## <span data-ttu-id="509e7-121">輸出</span><span class="sxs-lookup"><span data-stu-id="509e7-121">OUTPUTS</span></span>

### <span data-ttu-id="509e7-122">[System.object]. 清單 ' 1 [OperationalInsights]。 PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="509e7-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="509e7-123">筆記</span><span class="sxs-lookup"><span data-stu-id="509e7-123">NOTES</span></span>

## <span data-ttu-id="509e7-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="509e7-124">RELATED LINKS</span></span>

[<span data-ttu-id="509e7-125">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="509e7-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


