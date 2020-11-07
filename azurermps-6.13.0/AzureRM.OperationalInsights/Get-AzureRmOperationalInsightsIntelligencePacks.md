---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: d5877e29db7c678122af93d3e5d2d6281183e410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623752"
---
# <span data-ttu-id="2d399-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="2d399-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="2d399-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d399-102">SYNOPSIS</span></span>
<span data-ttu-id="2d399-103">取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2d399-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d399-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d399-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d399-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d399-105">DESCRIPTION</span></span>
<span data-ttu-id="2d399-106">**AzureRmOperationalInsightsIntelligencePacks** Cmdlet 會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2d399-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="2d399-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d399-107">EXAMPLES</span></span>

### <span data-ttu-id="2d399-108">範例1：取得智慧套件</span><span class="sxs-lookup"><span data-stu-id="2d399-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="2d399-109">這個命令會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="2d399-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="2d399-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d399-110">PARAMETERS</span></span>

### <span data-ttu-id="2d399-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d399-111">-DefaultProfile</span></span>
<span data-ttu-id="2d399-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2d399-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d399-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d399-113">-ResourceGroupName</span></span>
<span data-ttu-id="2d399-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d399-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="2d399-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d399-115">-WorkspaceName</span></span>
<span data-ttu-id="2d399-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2d399-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2d399-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d399-117">CommonParameters</span></span>
<span data-ttu-id="2d399-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d399-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d399-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d399-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d399-120">輸入</span><span class="sxs-lookup"><span data-stu-id="2d399-120">INPUTS</span></span>

### <span data-ttu-id="2d399-121">System.object</span><span class="sxs-lookup"><span data-stu-id="2d399-121">System.String</span></span>

## <span data-ttu-id="2d399-122">輸出</span><span class="sxs-lookup"><span data-stu-id="2d399-122">OUTPUTS</span></span>

### <span data-ttu-id="2d399-123">PSIntelligencePack 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="2d399-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="2d399-124">筆記</span><span class="sxs-lookup"><span data-stu-id="2d399-124">NOTES</span></span>

## <span data-ttu-id="2d399-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d399-125">RELATED LINKS</span></span>

[<span data-ttu-id="2d399-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d399-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


