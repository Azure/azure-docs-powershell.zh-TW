---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140190"
---
# <span data-ttu-id="f1758-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f1758-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="f1758-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1758-102">SYNOPSIS</span></span>
<span data-ttu-id="f1758-103">取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="f1758-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="f1758-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1758-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1758-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1758-105">DESCRIPTION</span></span>
<span data-ttu-id="f1758-106">**AzOperationalInsightsIntelligencePack** Cmdlet 會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="f1758-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="f1758-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1758-107">EXAMPLES</span></span>

### <span data-ttu-id="f1758-108">範例1：取得智慧套件</span><span class="sxs-lookup"><span data-stu-id="f1758-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="f1758-109">這個命令會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="f1758-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="f1758-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1758-110">PARAMETERS</span></span>

### <span data-ttu-id="f1758-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1758-111">-DefaultProfile</span></span>
<span data-ttu-id="f1758-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f1758-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1758-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1758-113">-ResourceGroupName</span></span>
<span data-ttu-id="f1758-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1758-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="f1758-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1758-115">-WorkspaceName</span></span>
<span data-ttu-id="f1758-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="f1758-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f1758-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1758-117">CommonParameters</span></span>
<span data-ttu-id="f1758-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1758-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1758-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1758-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1758-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f1758-120">INPUTS</span></span>

### <span data-ttu-id="f1758-121">System.object</span><span class="sxs-lookup"><span data-stu-id="f1758-121">System.String</span></span>

## <span data-ttu-id="f1758-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f1758-122">OUTPUTS</span></span>

### <span data-ttu-id="f1758-123">PSIntelligencePack 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="f1758-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="f1758-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f1758-124">NOTES</span></span>

## <span data-ttu-id="f1758-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1758-125">RELATED LINKS</span></span>

[<span data-ttu-id="f1758-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1758-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


