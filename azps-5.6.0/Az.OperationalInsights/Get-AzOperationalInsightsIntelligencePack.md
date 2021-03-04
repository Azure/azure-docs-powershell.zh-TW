---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a56fd0303e6f610468c9f2784396023fd20edef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905329"
---
# <span data-ttu-id="2c0b3-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="2c0b3-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="2c0b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c0b3-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0b3-103">獲得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2c0b3-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="2c0b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c0b3-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c0b3-105">描述</span><span class="sxs-lookup"><span data-stu-id="2c0b3-105">DESCRIPTION</span></span>
<span data-ttu-id="2c0b3-106">**Get-AzOperationalInsightsIntelligencePack** Cmdlet 會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2c0b3-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="2c0b3-107">例子</span><span class="sxs-lookup"><span data-stu-id="2c0b3-107">EXAMPLES</span></span>

### <span data-ttu-id="2c0b3-108">範例 1：取得智慧套件</span><span class="sxs-lookup"><span data-stu-id="2c0b3-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="2c0b3-109">此命令會獲得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2c0b3-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="2c0b3-110">參數</span><span class="sxs-lookup"><span data-stu-id="2c0b3-110">PARAMETERS</span></span>

### <span data-ttu-id="2c0b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0b3-111">-DefaultProfile</span></span>
<span data-ttu-id="2c0b3-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2c0b3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c0b3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0b3-113">-ResourceGroupName</span></span>
<span data-ttu-id="2c0b3-114">指定包含工作區的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="2c0b3-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="2c0b3-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c0b3-115">-WorkspaceName</span></span>
<span data-ttu-id="2c0b3-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2c0b3-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2c0b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0b3-117">CommonParameters</span></span>
<span data-ttu-id="2c0b3-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c0b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0b3-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2c0b3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0b3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="2c0b3-120">INPUTS</span></span>

### <span data-ttu-id="2c0b3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2c0b3-121">System.String</span></span>

## <span data-ttu-id="2c0b3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="2c0b3-122">OUTPUTS</span></span>

### <span data-ttu-id="2c0b3-123">Microsoft.Azure.Commands.OperationalInsights.models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="2c0b3-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="2c0b3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="2c0b3-124">NOTES</span></span>

## <span data-ttu-id="2c0b3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c0b3-125">RELATED LINKS</span></span>

[<span data-ttu-id="2c0b3-126">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c0b3-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


