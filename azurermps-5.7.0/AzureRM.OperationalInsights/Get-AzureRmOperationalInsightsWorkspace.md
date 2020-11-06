---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93457700"
---
# <span data-ttu-id="a1a22-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1a22-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a1a22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1a22-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a22-103">取得工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1a22-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a22-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1a22-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a22-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1a22-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a22-106">**AzureRmOperationalInsightsWorkspace** Cmdlet 會取得現有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1a22-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="a1a22-107">如果您指定工作區名稱，此 Cmdlet 會取得該工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1a22-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="a1a22-108">如果您沒有指定名稱，此 Cmdlet 會取得資源群組中所有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1a22-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="a1a22-109">如果您沒有指定名稱和資源群組，此 Cmdlet 會取得訂閱中所有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1a22-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="a1a22-110">示例</span><span class="sxs-lookup"><span data-stu-id="a1a22-110">EXAMPLES</span></span>

### <span data-ttu-id="a1a22-111">範例1：依名稱取得工作區</span><span class="sxs-lookup"><span data-stu-id="a1a22-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a1a22-112">這個命令會在名為 [ContosoResourceGroup] 的資源群組中取得名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="a1a22-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="a1a22-113">參數</span><span class="sxs-lookup"><span data-stu-id="a1a22-113">PARAMETERS</span></span>

### <span data-ttu-id="a1a22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a22-114">-DefaultProfile</span></span>
<span data-ttu-id="a1a22-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a1a22-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1a22-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1a22-116">-Name</span></span>
<span data-ttu-id="a1a22-117">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="a1a22-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a22-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a22-118">-ResourceGroupName</span></span>
<span data-ttu-id="a1a22-119">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1a22-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a22-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a22-120">CommonParameters</span></span>
<span data-ttu-id="a1a22-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1a22-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a22-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1a22-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a22-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a1a22-123">INPUTS</span></span>

### <span data-ttu-id="a1a22-124">所有</span><span class="sxs-lookup"><span data-stu-id="a1a22-124">None</span></span>
<span data-ttu-id="a1a22-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a1a22-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1a22-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a1a22-126">OUTPUTS</span></span>

### <span data-ttu-id="a1a22-127">[System.object]. 清單 ' 1 [OperationalInsights]。 PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="a1a22-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="a1a22-128">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="a1a22-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a1a22-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a1a22-129">NOTES</span></span>

## <span data-ttu-id="a1a22-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1a22-130">RELATED LINKS</span></span>

[<span data-ttu-id="a1a22-131">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a1a22-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


