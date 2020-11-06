---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a88806ddd934c2c7ee4eb8bb6f463da24ecefde7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447311"
---
# <span data-ttu-id="f0254-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f0254-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f0254-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0254-102">SYNOPSIS</span></span>
<span data-ttu-id="f0254-103">取得工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0254-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0254-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0254-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0254-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0254-105">DESCRIPTION</span></span>
<span data-ttu-id="f0254-106">**AzureRmOperationalInsightsWorkspace** Cmdlet 會取得現有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0254-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="f0254-107">如果您指定工作區名稱，此 Cmdlet 會取得該工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0254-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="f0254-108">如果您沒有指定名稱，此 Cmdlet 會取得資源群組中所有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0254-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="f0254-109">如果您沒有指定名稱和資源群組，此 Cmdlet 會取得訂閱中所有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0254-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="f0254-110">示例</span><span class="sxs-lookup"><span data-stu-id="f0254-110">EXAMPLES</span></span>

### <span data-ttu-id="f0254-111">範例1：依名稱取得工作區</span><span class="sxs-lookup"><span data-stu-id="f0254-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f0254-112">這個命令會在名為 [ContosoResourceGroup] 的資源群組中取得名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="f0254-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="f0254-113">參數</span><span class="sxs-lookup"><span data-stu-id="f0254-113">PARAMETERS</span></span>

### <span data-ttu-id="f0254-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0254-114">-DefaultProfile</span></span>
<span data-ttu-id="f0254-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f0254-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0254-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0254-116">-Name</span></span>
<span data-ttu-id="f0254-117">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="f0254-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0254-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0254-118">-ResourceGroupName</span></span>
<span data-ttu-id="f0254-119">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0254-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0254-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0254-120">CommonParameters</span></span>
<span data-ttu-id="f0254-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0254-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0254-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0254-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0254-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f0254-123">INPUTS</span></span>

### <span data-ttu-id="f0254-124">System.object</span><span class="sxs-lookup"><span data-stu-id="f0254-124">System.String</span></span>

## <span data-ttu-id="f0254-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f0254-125">OUTPUTS</span></span>

### <span data-ttu-id="f0254-126">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="f0254-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f0254-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f0254-127">NOTES</span></span>

## <span data-ttu-id="f0254-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0254-128">RELATED LINKS</span></span>

[<span data-ttu-id="f0254-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f0254-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


