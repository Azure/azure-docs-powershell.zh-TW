---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 4082e7fc36228953ea33f8f3252bab642ca50e2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914706"
---
# <span data-ttu-id="29559-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="29559-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="29559-102">簡介</span><span class="sxs-lookup"><span data-stu-id="29559-102">SYNOPSIS</span></span>
<span data-ttu-id="29559-103">獲得工作區相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29559-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="29559-104">語法</span><span class="sxs-lookup"><span data-stu-id="29559-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29559-105">描述</span><span class="sxs-lookup"><span data-stu-id="29559-105">DESCRIPTION</span></span>
<span data-ttu-id="29559-106">**Get-AzOperationalInsightsWorkspace** Cmdlet 會取得現有工作區的資訊。</span><span class="sxs-lookup"><span data-stu-id="29559-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="29559-107">如果您指定工作區名稱，此 Cmdlet 會獲得該工作區的資訊。</span><span class="sxs-lookup"><span data-stu-id="29559-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="29559-108">如果您未指定名稱，此 Cmdlet 會獲得資源群組中所有工作區的資訊。</span><span class="sxs-lookup"><span data-stu-id="29559-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="29559-109">如果您未指定名稱和資源群組，此 Cmdlet 會獲得訂閱中所有工作區的資訊。</span><span class="sxs-lookup"><span data-stu-id="29559-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="29559-110">例子</span><span class="sxs-lookup"><span data-stu-id="29559-110">EXAMPLES</span></span>

### <span data-ttu-id="29559-111">範例 1：按名稱取得工作區</span><span class="sxs-lookup"><span data-stu-id="29559-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="29559-112">此命令在名為 ContosoResourceGroup 的資源群組中，會獲得名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="29559-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="29559-113">參數</span><span class="sxs-lookup"><span data-stu-id="29559-113">PARAMETERS</span></span>

### <span data-ttu-id="29559-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29559-114">-DefaultProfile</span></span>
<span data-ttu-id="29559-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="29559-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29559-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="29559-116">-Name</span></span>
<span data-ttu-id="29559-117">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="29559-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="29559-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29559-118">-ResourceGroupName</span></span>
<span data-ttu-id="29559-119">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29559-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="29559-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29559-120">CommonParameters</span></span>
<span data-ttu-id="29559-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="29559-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29559-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="29559-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29559-123">輸入</span><span class="sxs-lookup"><span data-stu-id="29559-123">INPUTS</span></span>

### <span data-ttu-id="29559-124">System.String</span><span class="sxs-lookup"><span data-stu-id="29559-124">System.String</span></span>

## <span data-ttu-id="29559-125">輸出</span><span class="sxs-lookup"><span data-stu-id="29559-125">OUTPUTS</span></span>

### <span data-ttu-id="29559-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="29559-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="29559-127">筆記</span><span class="sxs-lookup"><span data-stu-id="29559-127">NOTES</span></span>

## <span data-ttu-id="29559-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="29559-128">RELATED LINKS</span></span>

[<span data-ttu-id="29559-129">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="29559-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


